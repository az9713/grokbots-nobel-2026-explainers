# QA REPORT: nobel-medicine-2026-explainer.html (Optogenetics: Deisseroth, Hegemann, Nagel)
Tester: Tess Tester · 7 Oct 2026 · Headless Chromium via Playwright (venv /workspace/.qavenv, harness copied and adapted from /workspace/nobel2026/qa/retest3) · HTML not modified · Source of truth: research.md (Rex), specs: narrative.md (Sommer)

**Viewports:** real Playwright viewports at 1280×800 and 390×844 (`innerWidth` measured as 390, so no emulation or iframe fallback was needed). The mobile context also sets `isMobile`, `hasTouch` and DPR 2, and mobile clicks are touchscreen taps.

## Overall: **FAIL** (0 blockers, 3 majors, all in the Tab 7 circuit explorer)
The content, facts, citations, DOIs and tags are clean. The FAIL comes from the Tab 7 interaction: one region opens the wrong card, empty-space clicks don't clear the card, and the line hit areas are too small on mobile.

| Check | Result |
|---|---|
| 1a Console / requests | PASS: 0 console errors or warnings and 0 page errors (desktop and mobile). 0 external requests and 0 failed requests. |
| 1b scrollWidth | PASS: docW = 1280 and 390 on all 8 tabs. Figures scroll inside themselves on mobile (figure scrollWidth 672 / clientWidth 352; SVG and canvas min-width 640). |
| 1c SVG/canvas content | PASS: every SVG is populated (11–291 drawn elements each). The Fig 5a canvas has about 18k painted pixels. |
| 1d getBBox overlap | PASS: 0 text/text overlaps and 0 SVG text outside its viewBox, on all tabs at both sizes (run.py → results.json `ov`). |
| 1e Clipping / tofu / contrast | PASS with issues: no clipped HTML (`overflow:hidden`/ellipsis) and no elements past the viewport. No tofu: all 19 non-ASCII glyphs (· “ ” ü – → − ≈ ← ✕ — ✓ ö α … ↑ ↓ ‘ ’) render in both the serif and sans stacks. Contrast: see m2. |
| 1f Tab navigation | PASS on load / **issue after load**: arrow keys move t1→…→t8→t1 (right wraps) and t1→t8→t7 (left wraps), with focus, aria and the hash all updated. Hash on load works for #t1–#t8; #src-X opens t8 and #bogus falls back to t1. Changing the hash after load does nothing (m1). |
| 2a Tab 5 canvas | PASS: at slider steps 0–3, pulses/spikes = 5/5, 7/7, 11/11, 16/16. Every spike starts 4 px after its pulse onset (pixel analysis). A real click on the slider works. Light off: 0 pulses, 0 spikes, button reads "Light pulses off" and the label reads "light off: neuron stays at rest". Neuron without ChR2: 16 pulses, 0 spikes, aria-pressed=true, label "no ChR2: light has no effect". This matches the caption and prose (pulse for pulse, low→high only, no frequency limit). The Fig 5b fibre toggle works. |
| 2b Tab 7 explorer | **FAIL**: M1, M2, M3. All 6 buttons open the correct card, and every card carries its citation(s). |
| 3a Internal anchors | PASS: 42 (tab, anchor) pairs across t1–t8. Each resolves to an id in the t8 list and switches to t8. |
| 3b DOIs vs Crossref | PASS: all 30 DOIs match Crossref on title, authors, year, journal, volume and first page (crossref.json). Every doi.org link resolves to the right publisher page. 200: nature.com/351489a0, PNAS ×4 (cookie page), Elsevier ×3, IOP, PLOS, Royal Society. **Bot-block/paywall, not broken:** 13 × 429 at nature.com (rate limit / IDP cookie wall) and 6 × 403 (science.org ×5, jneurosci.org ×1). |
| 3c nobelprize.org | PASS: [SB] PDF 200, [SB] mirror (nobelprizemedicine.org) 200, [PR] 200. |
| 3d Every source cited | PASS: all 32 list entries are cited at least once, including [Deisseroth 2015] on the t5 "optogenetics" naming line. |
| 4 Content vs dossier | PASS with minors: details below. |

## Issues
| # | Sev | Location | Issue | Suggested fix |
|---|---|---|---|---|
| M1 | **major** | t7 Fig 7, LH node (Sleep → waking) | The Anxiety group's transparent 26-wide BNST→LH hit line is drawn after the Sleep circle and ends on LH. Clicking the LH dot itself, about 34% of the Sleep circle's area (38/113 sample points), opens **Anxiety** instead of Sleep. This happens at both sizes (probe7.py; interact.json desk_hits/mob_hits row 1). | Draw the single-region circles after the link groups (append the c-sleep/c-innate/c-engram/c-loco groups last), or shorten link hit lines by r=26 at each end. |
| M2 | **major** | t7 Fig 7, empty space | Clicking empty brain or background does **not** clear the card; the previous card stays highlighted (t7_after_empty_desk.png, t7_empty_click_1280.png). The code only handles clicks on `.hit`. Also, c-reward is pre-selected on load. | In the `#brain` click handler, call `sel(null)` when `e.target.closest('.hit')` is null. Decide whether the initial `sel('c-reward')` is wanted. |
| M3 | **major** | t7 Fig 7 at 390 px | The hit areas for link lines (reward ×2, anxiety ×4) are **16.6 CSS px** wide (stroke 26 in viewBox × 0.64 scale), below the 26 px minimum. The circles are 33.3 px (pass). At 1280 the lines are 25 px and the circles 50 px. | Make the transparent hit stroke ≥ 42 viewBox units (≥ 27 px at the 640 px mobile min-width), or switch to a larger stroke under the <560px media query. |
| m1 | minor | Tab routing (script `show`) | No `hashchange` listener. Editing the URL hash, or an in-page `<a href="#t5">`, after load leaves the old tab showing (results.json `hash_samedoc`: setting #t2 kept t1, and so on). | `addEventListener('hashchange',()=>show(location.hash.slice(1),false))`. |
| m2 | minor | t7 cards (and t8 Evidence column) `cite` text | Text in #6f8293 on the card panel #101a24 gives **4.43:1**, under AA 4.5:1 for 12 px text (a11y.json). | Lighten `cite` inside `.card`/`.col` to about #7d92a5 (≈5:1). |
| m3 | minor | t8 Fig 8a label "red-shifted light reaches the inner layer first" | This claim is not in research.md or Sommer's spec. It is anatomically defensible (the retina is inverted), but it doesn't trace to the dossier. | Drop it, or ask Rex to add it as DERIVED/textbook. |
| m4 | minor | All SVG figures at 390 | With min-width 640 the figures scale to 0.64, so 11–12 px labels render at about 7–7.7 CSS px (legible on DPR 2, small). This is the same pattern accepted in the physics retest. | Optional: bump label font-size in a <560px query, or set min-width to 760. |
| m5 | minor | Terms on first use | t1 "channelrhodopsin" is bolded but not defined until t4. t2 uses "ChR2" before it's introduced. t7 abbreviations BNST, VMH, Esr1+ and MLR (expanded only as "Midbrain locomotor") are not expanded, and "hippocampal"/"dentate gyrus" are not explained. | Add `.term` defs: channelrhodopsin (t1), BNST (bed nucleus of the stria terminalis), VMH (ventromedial hypothalamus), Esr1+ (oestrogen-receptor-1-expressing). Change t2 to "the channel (channelrhodopsin-2, ChR2, see tab 4)". |
| t1 | trivial | t8 [Harz1991] descriptor "Fast photocurrents in Chlamydomonas" | Crossref title: "Rhodopsin-regulated calcium currents in Chlamydomonas". The descriptor is a paraphrase, not wrong. | Optional: use the real title. |
| t2 | trivial | t3 tab title "The problem before 2002" | The scorecard includes 2004-onward and 2005 rows (Banghart, Lima & Miesenböck). | "The problem before channelrhodopsin". |
| t3 | trivial | t6 Fig 6 ChR1 card "↑ depolarize" | Inward proton current = depolarizing is a fair DERIVED inference, but [SB] lists ChR1 only as a proton channel, not as a tool. Sommer's spec says only "ChR1 green (protons)". | Optional: drop the arrow on ChR1 or label it "(inward H⁺)". |
| t4 | trivial (docs) | src/dois.json | Zhang2007 is marked "UNVERIFIED" (Crossref confirms 10.1038/nature05744, "Multimodal fast optical interrogation of neural circuitry", Nature 446:633). Gradinaru2010 points to a Faculty Opinions DOI (10.3410/…), which is wrong but not used in the HTML. research.md says every DOI was checked, which contradicts this file. | Rex: update dois.json. |

## Content check details (all PASS unless listed above)
- **Prize facts:** laureates and affiliations (HHMI & Stanford; Humboldt Berlin; Würzburg), birth years 1971/1954/1953, exact citation wording, 5 Oct 2026, Nobel Assembly at Karolinska Institutet, 12 million SEK shared equally, and the Svenningsson quote all match §1 and are cited to [PR].
- **Years and claims:** 1971 bR · 1991 µs photocurrent → receptor = channel · 2002 ChR1 green, inward **proton**, oocytes, truncated core · 2003 ChR2 bluer, **cation**, first 315 aa, peak→plateau · 2005 lentivirus, hippocampal, no toxicity, ms spikes and trains, no added retinal · 2006 term coined (J Neurosci, Deisseroth et al.) · 2007 Aravanis fibre, freely moving rodents, whisker motor cortex (prose "rodents", takeaway "mouse", consistent with flag 3) · 2007 NpHR first two-colour control · 2011–13 circuits · **2021 Sahel: Chrimson, goggles, prolonged partial, high-contrast objects, EEG, tagged "Evidence (n = 1)"**. All match §§3–9.
- **Units:** the only physical values are "−70 mV" (×3) and "1 ms" (×2), each labelled "textbook approximation, not from [SB]", plus the t8 footnote. No nm and no other ms or kinetic values. Colours use only [SB]'s words.
- **Rat detail** is attributed to [PR], with "[SB] does not name the species" (t5).
- **Credit:** neutral throughout. "[SB] credits all three groups" (t4), and the t8 credit note names Spudich, Takahashi, Boyden, Bamberg and Miesenböck factually. No priority language.
- **Trials:** only the [SB] quote "several clinical trials… are presently underway" plus "[SB] gives no names or numbers". No trial names, NCT numbers or counts.
- **DREADD:** the card says "slow · body-wide", with no ↑/↓ arrow. The prose says only "switched on by a drug… slower… body-wide".
- **Tags:** Established on the prize, 1991, 2002, 2003, 2005, 2007, NpHR and the t7 circuits; Evidence (n = 1) on vision; Open = wider therapy (marked "Our interpretation; not discussed in [SB]") and chemogenetics "may eventually". This matches §9 exactly.
- **Figures:** 13/13 figcaptions carry "Schematic". Fig 1 ticks and colours match the spec (1991–2003 H/N, 2005 joint, 2006–07 Deisseroth, others grey). Fig 2a values are textbook-labelled. Fig 2b, 4a, 4b ("no values"), 4c (inset), 5a, 5b, 6 (no nm), 7, 7b (A/B/C protocol) and 8a (camera, grey dead rods/cones, Chrimson RGCs, arrow to cortex) all agree with the prose and narrative.md, apart from m3 and t3.
- **Takeaways:** each of the 8 tabs has one `.take` line.

## Files (in this folder)
- Full-page screenshots: desk_t1–t8.png (1280×800) and mob_t1–t8.png (390×844, DPR 2).
- Tab 5: t5_rate0–3_desk.png, t5_lightoff_*.png, t5_nochr2_*.png, t5_controls_*.png.
- Tab 7: t7_hit_mob.png, t7_after_empty_*.png, t7_empty_click_1280.png.
- Figure crops: fig1/fig2b/fig4c/fig6/fig7b/fig8a_1280.png.
- Harness: run.py (render, console, requests, docW, bbox, hash/keys, anchors), interact.py (canvas pixel analysis and hit areas), probe7.py (hit-area ownership), a11y.py (contrast and tofu), crossref.py.
- Raw output: results.json, interact.json, a11y.json, crossref.json, urls.txt, curl.txt.

---
# Retest 2 (Tess Tester · 7 Oct 2026, about 09:50–10:10 PT · HTML not modified)
Artifacts are in `qa/retest2/`. Harness: run.py, interact.py (Tab 5 part) and a11y.py were re-run unchanged. New scripts: t7sweep.py (real clicks and taps), t7sweep_iso.py (same sweep with the sticky nav made static and scrollIntoView stubbed **inside the test only**), and misc.py (hashchange, cite contrast, text dump → text_current.txt). Note: the Tab 7 section of interact.py measures the old DOM hit lines (stroke 26) and is obsolete now that the page does geometric hit-testing. Ignore its `*_hits` rows.

## Overall: **PASS** (0 blockers, 0 majors. The minors below are optional.)

| Fix | Result |
|---|---|
| M1 node hits | PASS. Hits are now resolved geometrically (`near()`: nodes r = 26 take priority; lines use the trimmed segment, ±22). Grid sweep: 522 unambiguous points per size (every node disc at 6-unit spacing, 11 positions × 5 offsets on each of the 6 lines, and 8 empty points). **0 wrong-card hits at 1280 and at 390.** The 14 "no card" results per size all lie within 0.5 viewBox units of the line-trim boundary (pixel rounding at the edge), not inside it. LH dot → **Sleep** and LHb→VTA midpoint → **Reward** at both sizes. 38 points sit inside both the LHb→VTA and BNST→VTA zones near LHb/VTA, where the nearer line wins, which is acceptable. (Without the test isolation, real clicks near the top of the viewport land on the sticky tab bar. That is expected and not a page bug.) |
| M2 empty clears | PASS. All 8 empty points clear the card (no `.card.hl`) at both sizes. c-reward is still pre-selected on load (design choice). |
| M3 ≥ 26 px | PASS. At 390 (scale 0.640), node discs are 33.3 px and line hit width (44 units) is **28.2 px**. At 1280: 50 / 42.3 px. |
| m1 hashchange | PASS. After load, #t3 → t3, #t6 → t6, #t1 → t1, and an in-page `<a href="#t5">` → t5. #src-Sahel2021 and #src-Harz1991 → t8 with the entry scrolled into view, at both sizes. |
| m2 cite contrast | PASS. #7d92a5 on card/col #101a24 = **5.46:1**, 5.80 on #0c131b and 6.13 on body. The a11y.py run no longer lists any cite. |
| m3 Fig 8a | PASS. "red-shifted… inner layer first" is gone. Fig 8a text now reads: goggles + camera, light pulses, eye, retina cross-section, ganglion cells + Chrimson, rods & cones (dead), middle layers, to visual cortex (EEG). |
| m5 terms | PASS. t1 defines channelrhodopsin ("a light-sensing protein from algae that is itself an ion channel"). t7 expands BNST, VMH (ventromedial hypothalamus), Esr1+ ("neurons that make oestrogen receptor alpha…") and MLR (mesencephalic locomotor region). t2 says only "channelrhodopsin, a light-gated channel (tab 4)", with no "ChR2". |
| t3 ChR1 arrow | PASS. The ChR1 card reads "passes protons" with no ↑ depolarize. |
| t2 Tab 3 title | PASS. The nav and h2 both read "The problem: earlier attempts". |

## Regression (1280 and 390)
| Check | Result |
|---|---|
| Console / requests | PASS: 0 errors or warnings, 0 page errors, 0 external requests, 0 failed. |
| scrollWidth | PASS: docW 1280 and 390 on all 8 tabs. Mobile figures scroll internally (672/352). |
| getBBox overlaps | PASS: 0 overlaps and 0 text outside viewBox on all tabs at both sizes. |
| Tab 5 canvas | PASS: pulses/spikes 5/5, 7/7, 11/11, 16/16, each spike +4 px after onset. Light off 0/0. No ChR2: 16 pulses, 0 spikes. Fibre toggle OK. Same at both sizes. |
| Citations | PASS: 42 (tab, anchor) pairs, all resolve and switch to t8. 32/32 sources are cited. |
| Arrow keys | PASS: right t1→…→t8→t1, left t1→t8→t7. |
| Tofu / contrast | PASS: no tofu. The only a11y.py flag is the dark "+" glyph inside green circles in Fig 4c (false positive: measured against the figure background, not the green disc; also present in the first run). |
| Text diff | **Limited.** No copy of the previous HTML or its text was kept (build/ fragments were overwritten in place), so a literal diff was not possible. Instead I diffed the content against the first run's REPORT findings: the changed strings are exactly the m3/m5/t2/t3 items above, plus the cite colour. Facts re-verified: 12 million SEK, 5 Oct, 315 amino acids, "−70 mV" ×4 and "1 ms" ×3 (including the t8 footnote, same as before), the tag set (9 Established, 1 Evidence n = 1, 1 Open) and 13 "Schematic" figures. The full current text is saved as `retest2/text_current.txt` to serve as the baseline for any later diff. |

## Remaining issues (all minor/trivial, not blocking)
| # | Sev | Location | Issue | Fix |
|---|---|---|---|---|
| r1 | minor | t7 Fig 7, endpoint dots without their own card (VTA, BNST, BLA, CeA, vHPC, LDT, LHb) | Line hit zones are trimmed 34 units from each end, so clicking these dots, or the 8-unit ring between a node disc and a line start, hits nothing and **clears** the card. | Optional: don't clear on clicks within about 34 units of a link endpoint, or map an endpoint dot to its link's circuit. |
| r2 | minor | t7 BLA→CeA link | After trimming, the hit segment is only about 17 units long (about 11 px at 390, 16 px at 1280). It is wide enough (28 px) but short. | Reduce the trim to 26 (the node r) for links whose endpoints have no disc. |
| m4 | minor (carried over) | SVG labels at 390 | About 7–7.7 CSS px labels (unchanged, accepted previously). | Optional. |
| t1, t4 | trivial (carried over) | Harz1991 descriptor; dois.json | Not re-checked as fixed. | As before. |

Screenshots: retest2/desk_t1–8.png, mob_t1–8.png, t5_*.png, t7_sweep_iso_1280/390.png. (t7_after_empty_*.png and t7_hit_*.png come from the obsolete interact.py Tab 7 section: its corner "empty" click lands under the sticky tab bar, so the last card (c-loco) stays. Ignore them; M2 is verified by t7sweep.)
