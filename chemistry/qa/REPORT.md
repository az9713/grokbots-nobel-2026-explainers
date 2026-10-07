# QA REPORT: nobel-chemistry-2026-explainer.html (rebuild 10:13:30 PT, 139,393 B)
Harness: Playwright headless Chromium (/workspace/.qavenv). Scripts: scripts/run.py, interact.py, crossref.py. Data: results.json, interact.json, crossref.json/.txt, alltext.txt, fig4a_check.txt. Screenshots: shots/{desk,mob}_t1..t8.png and figure close-ups.

## Overall: FAIL (1 major, 5 minor). The major is a one-line fix: Fig 7b alt text.

## PASS checks
1. Network/JS: 0 non-file requests at both widths, 0 failed requests, 0 console messages or page errors. Tabs: clicks, hash set, `hashchange` (#t5, #t2, #t8, #t1), deep link on load (#t6), pager buttons, the Sources button and ArrowLeft/Right with wrap all work. All 115 `#` anchors resolve; citation click goes to t8 and highlights the entry.
2. Layout: document scrollWidth equals the viewport on every tab at 1280, 390, 360 and 320. Nothing outside a scroll container is wider than the viewport. `.grid2/.cards/.cols>*{min-width:0}` is present.
3. SVG: 0 text bbox overlaps (>5%) and 0 text clipped by the viewBox, for all 15 SVGs at both widths. Fig 1 swap: fig1 is shown at ≥561px and fig1n at ≤560px (tested 1280/600/561/560/559/390/320/700/1280; it swaps back). No duplicate ids.
4. Contrast: every HTML text and SVG `<text>` element is ≥4.5:1, apart from the detector false positives in fig2c (Ar/H/O sit on a dark plane; checked visually in shots/fig2c_1280.png). fig4b R/S labels come out at exactly ≈4.5:1, which is borderline but passes.
5. Captions: Fig 5b ("Measured…") and Fig 6a are the only figures not tagged Schematic. Fig 4a carries "Computed from Eqs. 2–3, random pairing assumed". The Fig 7b SVG text has "+ aldehyde, i-Pr₂Zn → alkyl transfer". Fig 4a recompute: all 4×201 polyline points match y=x(1+β)/(1+gβ) with β=(1−x²)/(1+x²) to within 1e-4. Spec values g0@.5=0.80, g0@.25=0.471, g.25@.5=0.696, g4@.5=0.235 are all met, and the dot is at (50,80).
6. Rex §10: handedness is described by configuration, and the page notes that L-alanine rotates light to the right in acid. No claim that molecules always bend light left. 1995: 5→55→87→90 (no 2%). 2003: >99.5% (no 99.99). 0.00005%. 18 R / 19 S of 37, 15–91%. "630,000" is quoted from [SB] and not recomputed. Singleton/Soai credit is described as "independently". No Hajos–Parrish, thalidomide or Marckwald. The ODE dee/dt=(μ/2)(R+S)·ee·(1−ee²) is labelled "Our illustration". Laureates are Kagan & Soai, the citation is verbatim, 12 MSEK, and bio data match. Wynberg & Feringa 1976 "antipodal interaction" is cited [SB pp. 4–5]. Other numbers match research.md: 15%→98% DAIB, 70→95 Merck, 53%@5%→16% hyperpositive ((–)-NBE = N-benzylephedrine per SB), 86→35 (1990), 70→32 (Alberts), 90/81 erosion, 56.25/37.5/6.25, β=0.6, f=1.6, 3.5–4 Gyr. "≈10⁴× smaller than 0.00005%" checks: 5e-7/4e-11≈1.25e4.
7. Sources: 41 `<li>` entries = 3 nobelprize.org (PR, SB, POP) + 38 paper entries carrying **40 DOI links**. Athavale2020 (10.1038/s41557-020-0421-8 and 10.1021/jacs.0c05994) and Geiger2020 (10.1038/s41929-020-0441-1 and 10.1039/d0sc04724d) each hold two DOIs. research.md lists 41 unique DOIs. The only dossier DOI missing from the page is Hoang 2003 (10.1021/ja028634o), which was dropped on purpose. The page has no DOIs that aren't in the dossier. So Frank (41 entries) and Rex (40 dossier papers excluding Hoang, all present) are both right. One correction to the steering note: the page has 40 DOI links (in 38 entries), not 38. All 40 DOIs resolve on Crossref (0 errors). First author, year, journal, volume and first page match the listed metadata for every one. doi.org returns 302 for all four paired DOIs and for the re-encoded Girard 1998 SICI DOI (%3C/%3E), which goes to Wiley. All 41 sources are cited in the text at least once.
8. Interaction: 26 `.term` tooltips at each width show on focus and stay inside the viewport (left≥18, right≤370 at 390). The tabs follow the roving-tabindex tablist pattern.

## Findings
| ID | Sev | Owner | Repro | Expected | Actual |
|---|---|---|---|---|---|
| C-1 | major | Ivy (figs) / Frank | `#fig7b` aria-label | alt contains "+ aldehyde, i-Pr₂Zn → alkyl transfer" | alt paraphrases it: "takes up another aldehyde and diisopropylzinc and alkyl transfer follows" (the SVG text itself is correct) |
| C-2 | minor | Frank/Ivy | Fig 4a caption tag | labelled computed | tag reads "Schematic · Computed from Eqs. 2–3, random pairing assumed". "Schematic" contradicts "computed"; drop the word |
| C-3 | minor | Cleo/Frank | t1 text | announcement date 7 Oct 2026 shown in the prize section | the date only appears in the source list ("press release, 7 Oct 2026") |
| A-1 | minor | Frank | 390px, any tab footer | targets ≥24px (WCAG 2.5.8) | footer buttons (← prev / Sources / next →) are 15px tall. Inline citation links are 16px tall but fall under the inline exemption |
| A-2 | minor | Frank | focus a tab, press Home/End | first/last tab (APG) | no-op. Tabs also lack `aria-controls`/`id` linkage, and panels lack `aria-labelledby` |
| A-3 | minor | Frank | Tab key | clearly visible focus ring | only the UA default `outline:auto` (no custom :focus-visible style); visible but thin on the dark theme |
| V-1 | cosmetic | Ivy | shots/fig2c_1280.png | the right "alcohol" label sits under its molecule like the left one | the right label is pushed to the far right edge, away from its molecule |

---
## Retest round 2 (10:18:57 PT build): FAIL, 1 item. Details in retest2/REPORT.md
C-1, C-2, C-3, A-1, A-2 and V-1 are fixed. A-3 is partial: the new A-4 (major, Frank) is that footer prev/Sources/next buttons show no focus ring because `.tabfoot button{all:unset}` overrides `:focus-visible`. Full regression at 1280/390/360/320 is otherwise clean, and the text diff shows only the intended changes.

---
## Retest round 3 (10:22:26 PT build): PASS. Details in retest3/REPORT.md
A-4 fixed: all 22 footer buttons per width (1280/390) show a 3px #ffd166 focus-visible ring (13.68:1, not clipped, no ring on mouse focus). A Tab sweep of 144–147 focus stops found every one with a visible ring. Full regression at 1280/390/360/320 is clean, the DOI list is unchanged, and the text diff vs round 2 is empty. No open findings; the only remaining notes are fig4b R/S labels borderline at ≈4.5:1.
