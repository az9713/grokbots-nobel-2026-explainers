# QA REPORT: nobel-physics-2026-explainer.html
Tester: Tess Tester · 7 Oct 2026 · Headless Chromium (Playwright 1.x, chromium-headless-shell 153) · HTML not modified

## Overall: **FAIL** (no blockers, 3 majors to fix before ship)
Content, numbers, citations and tags are clean. The FAIL is for one factual inconsistency (the "million times" takeaway) and figure label collisions.

| Check | Result |
|---|---|
| 1 Rendering/interactivity | PASS with issues: 0 console errors/warnings, 0 page errors, 0 external requests, 0 failed requests; all SVGs and the canvas are populated; arrow keys wrap correctly (t1→…→t8→t1, ←); sky-map clicks open the right card (TXS, NGC, plane; empty space clears it) on desktop and mobile; significance toggle works; tooltips work; footer "Sources" goes to t8. No tofu: all Greek and math glyphs render. Label overlaps listed below. |
| 2 Links | PASS with issue: all 21 citation anchors on t1–t7 resolve to ids on t8 and switch tabs. External URLs: 6 return 200; doi:10.1126/science.1242856 gives 403 (science.org bot wall/paywall, not broken). All cited papers match Crossref (see below). 8 sources have no link/DOI. |
| 3 Numbers | PASS: every number in the text and figures traces to research.md. Excluded items are absent (~4σ S2013, ~3σ TXS coincidence, Gen2 specs, KM3NeT ~220 PeV, cross-section result, dust layer). Gen2 appears only as a site name from [SB], which is allowed. One exception is issue M1. |
| 4 Diagrams vs text | PASS with issues: values agree with the prose and Sommer's spec; every figure is tagged Schematic; TXS and NGC 1068 = Evidence, the Galaxy = Established at 5.7σ, "no single point source is established". |
| 5 GAL26 status | **Preprint only.** arXiv:2607.25966 "High-energy neutrino emission from the Milky Way" (IceCube, submitted 28 Jul 2026): no journal-ref and no journal DOI (only the arXiv DataCite DOI 10.48550/arXiv.2607.25966, pending). INSPIRE 3184051 shows no publication info. Crossref and web search find no journal version. The abstract confirms 5.7σ with 12 yr. |

## Issues
| # | Sev | Location | Issue | Suggested fix |
|---|---|---|---|---|
| M1 | major | t1 Takeaway: "a million times the energy of anything from the Sun" | Contradicts Fig 1 on the same tab (MeV→PeV "×10⁹", caption "a factor of a billion"). Solar ν are MeV and IceCube's are PeV, so the factor is ~10⁹. The error also appears in narrative.md. | Change to "a billion times". |
| M2 | major | t6 Fig 6, near 1 PeV | Label "2012 events · 1.04, 1.14 PeV" overlaps "astrophysical ν ∝ E^-2.5 above ~30 TeV" and "shaded: 68% band (shape only)"; the markers sit on the text. | Move the 2012 label below the curve (or the astro label up and left); move the band note elsewhere. |
| M3 | major | t8 Sources: PRL2013, PRL2014, TXS-MM, TXS-ARCH, NGC, GAL23, TAU, SPEC26, DET | No URL or DOI, so readers can't verify them. Crossref-verified DOIs: 10.1103/PhysRevLett.111.021103 · 10.1103/PhysRevLett.113.101101 · 10.1126/science.aat1378 · 10.1126/science.aat2890 · 10.1126/science.abg3395 · 10.1126/science.adc9818 · 10.1103/PhysRevLett.132.151001 · 10.1088/1748-0221/12/03/P03012. SPEC26 (PRL 136 121002 / PRD 113 062002) not verified by Crossref here. | Add doi.org links; get the SPEC26 DOIs from Rex. |
| m1 | minor | t7 sky canvas, right edge | Marker label is clipped to "TXS 0506" (should read "TXS 0506+056"; with the toggle on, the "3.5σ" is lost too). | Right-align the label to the left of the marker when x > ~800. |
| m2 | minor | t3 Fig 3b | "ankle · few EeV" collides with "extragalactic"; "GZK · >50 EeV" sits on the curve-end marker. | Offset the labels. |
| m3 | minor | t4 Fig 4 inset | Title "86 STRINGS · TOP VIEW" is overprinted by the top row of hexagon circles. Eiffel label overlaps the right-most string. | Raise the title / shift the grid down; nudge the Eiffel label right. |
| m4 | minor | mobile 390px, all SVG figures + sky canvas + Fig 7b | Figures scale to 320px, so label text renders ~4–5px (unreadable). On mobile the sky markers and hit target are about 6 CSS px. | Add a mobile layout (larger viewBox font sizes, or horizontal scroll at min-width ~600px); enlarge the hit radius. |
| m5 | minor | mobile t3 γ–ν equation | Wider than the column (514 vs 352 px); it scrolls (overflow:auto) but "K_π ≈ 2 (pp)…" is cut off with no scroll cue. | Wrap the K_π clause onto its own line on narrow screens. |
| m6 | minor | t6 prose "1-in-3.5-million chance", Takeaway/Fig 6/Fig 6b "2012" for Bert & Ernie | Not in research.md: the 5σ p-value is standard and correct (one-sided 2.9×10⁻⁷); the dossier gives the data window May 2010–May 2012 and publication 2013, not a 2012 event date. | Keep, but have Rex add both to the dossier, or relabel as "2010–12 data". |
| m7 | minor | t8 [GAL26] "publication status being checked" | Status is now known. | Replace with "preprint, not yet journal-published (as of 7 Oct 2026)". |

## Details
- Number trace (spot list): 86×60, 5,160 (≈ our count), 17 m, 1450–2450 m, 125 m, ~1 km³/~1 Gt, 25.4 cm, 300 TeV–1 EeV, 800–1000 m, <50 cm, ~200/~50 m, 1.31/1.33/0.75c/160 MeV, θC≈40°, 3 kHz, µHz, 100,000/yr, E^-3.7/E^-2.5, ~500 Mt, 0.3°@100 TeV, ~5°>50 TeV, ~8%@100 TeV, ×2, 50 m/PeV, 2.6 PeV/11°, 1.14 PeV, 28 = 21+7 (30 TeV–1.14 PeV), 5.7σ 2014, 231,486/10,569, >4σ 5 TeV–10 PeV, ~30 TeV, 11.4 PeV 31 Mar 2019, 7 τ 20 TeV–1 PeV 5σ, 4.5σ/5.7σ, ~290 TeV, 0.06°, ~7×, 3.5σ Sep 2014–Mar 2015, 79 ν 1–10 TeV, 4.2σ, 15 M M☉, 46 Mly, >1000 GRB searches, λ≈1.8×10⁹ cm≈18,000 km, 12,742 km, 0.92×6.0e23≈5.5e23, 450/58/14, all dates. All match. Sky coordinates: TXS l=195.4°, b=−19.6°; NGC 1068 l=172.1°, b=−51.9° (both correct).
- Fig 7b bars: 5.7, 5.7, 5, 4.2, 3.5 with the 5σ line, matching the spec. Bar colours: ≥5 green, 4–5 amber, <4 red.
- Crossref titles match: S2013 "Evidence for High-Energy Extraterrestrial Neutrinos…", PRL2013 "First Observation of PeV-Energy Neutrinos", PRL2014 "…Three Years…", TXS-MM "Multimessenger observations of a flaring blazar…", TXS-ARCH "Neutrino emission from the direction of the blazar TXS 0506+056 prior to…", NGC Science 378 538, GAL23 Science 380 1338 "Observation of high-energy neutrinos from the Galactic plane", TAU PRL 132 151001, DET JINST 12 P03012. HK arXiv:2202.00694 = Halzen & Kheirandish.
- Files: desk_t1..t8.png (1280×800, full page), mob_t1..t8.png (390×844), sky_1280_{txs,ngc,gal}.png, sky_390_txs.png (click states; click logic verified with sky2.py), sky_sig_*.png (toggle), tooltip.png, results.json (raw), alltext.txt, run.py/sky2.py (harness).

---
## Retest 2 (7 Oct 2026, Tess Tester): **FAIL**, 1 new major regression plus 1 residual minor
Same harness (`retest2/run.py` = run.py, `../sky2.py`, plus new `retest2/bb.py` for SVG text-bbox overlaps and `shots.py`/`shots2.py` for targeted shots). Venv: /workspace/.qavenv. HTML not modified. Raw output: retest2/results.json, bbox.json, curl.txt, alltext.txt.

### Fix verification
| Prior | Result | Evidence |
|---|---|---|
| M1 "a billion times" | PASS | m1_t1_takeaway_{1280,390}.png. Text diff vs the previous run: million→billion only. |
| M2 Fig 6 PeV label | **PARTIAL** | The label now reads "Bert & Ernie (2010–12 data) · 1.04, 1.14 PeV" below the band, and the getBBox text-vs-text check shows 0 overlaps. But the two PeV marker circles still sit on "shaded: 68% band (shape only)" (circle/text overlap 5×9 px at 1280, 3×6 at 390). m2_fig6_*.png |
| M3 DOIs | PASS | All 15 source entries have a link. The new DOIs check out on Crossref: 10.1103/2gh9-d4q7 = "Evidence for a Spectral Break or Curvature in the Spectrum of Astrophysical Neutrinos from 5 TeV to 10 PeV", PRL 136 121002 (2026); 10.1103/4n6v-r7n4 = "Improved measurements of the TeV-PeV extragalactic neutrino spectrum from joint analyses of IceCube tracks and cascades", PRD 113 062002 (2026). Both match the citations. m3_sources_*.png |
| m1 sky labels / toggle | PASS | With the toggle ON, "TXS 0506+056  3.5σ" is flipped left and shown in full at 1280 (sky_sig_ON_1280.png). At 390 it is also full once the figure is scrolled (sky_sig_ON_390_scrolledright.png). Hit radius at 390 = 22 CSS px. Clicks: TXS/NGC/plane/empty → right card at both sizes (sky2.py). |
| m2 Fig 3b | PASS | ankle, extragalactic and GZK are separated, with 0 bbox overlaps. m2_fig3b_*.png |
| m3 Fig 4 | PASS | The inset title is clear of the hex grid, and the Eiffel label clears the strings. 0 overlaps. m3_fig4inset_*.png, fig4_*.png |
| m4 mobile figures | PASS on t1–3, t5–8 / **FAIL on t4** | The figures are 640px min with overflow-x:auto (scrollWidth 672 / clientWidth 352). See N1. mob_fig_scrolled_390.png |
| m5 eq hint | PASS | "scroll →" shows under .eq at <560px. m4_eq_hint_390.png |
| m6 1-in-3.5-million / 2012 | PASS | The phrase is removed. "2010–12 data, published 2013" appears in the prose, the t6 takeaway, Fig 6 and the timeline (dated 2013). No "2012 events" or bare-2012 Bert/Ernie label remains. "May 2010 to May 2012" stays as the data window, per research.md. |
| m7 GAL26 | PASS | [GAL26] reads "PREPRINT · no journal version as of 7 Oct 2026". The prose says "arXiv preprint". |

### Regression
| Check | Result |
|---|---|
| Console/page errors | PASS: 0 (desktop and mobile) |
| External requests | PASS: 0 external, 0 failed |
| Keyboard tabs | PASS: wraps both ways |
| Citation anchors | PASS: 21/21 resolve on t8 |
| External links (curl -IL) | PASS: 6 return 200 (nobelprize.org ×3, kva.se, arXiv ×2), and IOP JINST returns 200. 10 return 403 after a correct redirect to link.aps.org (5) or science.org (5): publisher bot walls/paywalls, not broken. |
| Number trace vs research.md | PASS: the word-level diff of all text vs Retest 1 shows only the intended edits. Everything else was already traced. SPEC26 DOIs and GAL26 status now appear in research.md (lines 16, 18). |
| Excluded items | PASS: ~4σ S2013, ~3σ TXS, Gen2 specs, KM3NeT 220 PeV, cross-section result and dust layer are still absent. Gen2 and KM3NeT appear only as site names, cross-section only as the [SB] σ~10⁻³³ input and future-work text. The dust layer is mentioned only as "not drawn". |
| Tags | PASS: unchanged (Galaxy Established, TXS/NGC Evidence, figures Schematic, GAL26 Preprint) |

### Issues
| # | Sev | Location | Issue | Fix |
|---|---|---|---|---|
| N1 | **major (new regression)** | t4 at 390px (page_t4_390.png, mob_t4.png) | Document width 692px vs a 390 viewport: the whole page scrolls sideways and the prose column grows to ~612px, so text runs off-screen. Cause: Fig 4 and the inset sit in `.grid2`. Grid items default to `min-width:auto`, so the new 640px SVG min-width pushes the track wider instead of letting the figure scroll (those figures show scrollWidth = clientWidth = 672). t5's grid2 is unaffected. | Add `.grid2>*{min-width:0}` (or `figure{min-width:0;max-width:100%}`) inside the <560px media query. |
| N2 | minor (remaining from M2) | t6 Fig 6, ~1 PeV | The Bert/Ernie marker dots overprint the start of "shaded: 68% band (shape only)". | Move the band note left (e.g. under "flattens below ~30 TeV") or below the band at ~3–10 PeV. |
| N3 | trivial | t1 Fig 1 timeline | The "1988"/"2015" year labels touch their caption lines by 1.6px vertically (bbox). Not visible. | Optional: give the timeline rows +2px. |
| N4 | trivial (docs) | research.md line 123 | Still says "I have not checked whether [GAL26] is published", which contradicts line 16. | Rex: update the note. |

Screenshots: retest2/ (desk_t1–8 and mob_t1–8 full page; targeted m1/m2/m3/fig4/eq/sky_off/sky_sig_ON at _1280 and _390; page_t*_{1280,390}).

---
## Retest 3 (7 Oct 2026, Tess Tester): **PASS** (1 trivial residual, N3)
Harness: retest3/ copies of run.py, sky2.py, bb.py, plus the new n.py (fix checks and shape-vs-text bbox). HTML not modified (mtime 07:50:18). Raw output: retest3/results.json, bbox.json, alltext.txt.

### Fix verification
| Prior | Result | Evidence |
|---|---|---|
| N1 t4 widening | PASS | The <560px rule now contains `.grid2>*{min-width:0}`. At 390×844, document.scrollWidth is 390 on all of t1–t8 (body too). The t4 figures are 672/352 with overflow-x:auto. Setting Fig 4 scrollLeft=200 leaves page docW at 390 and window scrollX at 0. n1_t4_390.png, n1_fig4_scrolled_390.png |
| N2 Fig 6 band note | PASS | The note is now top-right. At 1280: 0 shape/text bbox overlaps on t6, and the note touches no dot or label. At 390: 0 text/text overlaps, and the note has no overlap. The only remaining hits are the curve-path bboxes behind the line labels (heuristic artefacts, also in Retest 2). n2_fig6_*.png |
| N3 Fig 1 labels | **NOT FIXED (trivial)** | getBBox still reports "1988"↔"Lederman, Schwartz, Steinberger" and "2015"↔"oscillations: ν have mass" overlapping 33.8×1.6 px at 1280. Not visible. n3_fig1_*.png |
| N4 research.md L123 | PASS | It now reads "RESOLVED: [GAL26] arXiv:2607.25966 is a preprint with no journal version as of 7 Oct 2026." This matches L16. |

### Regression
| Check | Result |
|---|---|
| SVG text bbox overlaps 1280/390 | PASS apart from N3 (the only 2 hits) |
| Console/page errors | PASS: 0 |
| External requests | PASS: 0 requests, 0 failed |
| Tab keyboard nav | PASS: wraps both ways |
| Citation anchors | PASS: 21/21 resolve on t8 |
| Sky clicks 1280/390 | PASS: TXS/NGC/plane → matching card, empty/corner → none |
| Significance toggle | PASS: sky_sig.png |
| Text diff vs Retest 2 | PASS: no visible-text changes (only the trailing newline). The fixes were layout/position only, as intended. |

### Issues
| # | Sev | Location | Issue | Fix |
|---|---|---|---|---|
| N3 | trivial | t1 Fig 1, 1988 and 2015 labels | The year labels' bbox still overlaps the line above by 1.6px. The claimed fix did not land. | Move the upper caption line up 2–3px (or the year down). |

Screenshots: retest3/ (desk_t1–8, mob_t1–8, n1_*, n2_*, n3_*, sky_*, tooltip.png).
