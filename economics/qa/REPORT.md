# QA REPORT: economics/index.html
12 Oct 2026 · Playwright 1.63 driving installed Chrome, headless, 1280×800 and 390×844 · harness `qa.py` (session scratchpad) · after 4 runs

## Overall: **PASS**
Run 1 found two defects (one figure label collision, one 9 px mobile overflow). Both are fixed. Runs 2–4 are clean (run 4 after adding the fourth erratum note).

| Check | Result |
|---|---|
| 1 Rendering | PASS: 0 console errors or warnings, 0 page errors, 0 external requests at both widths. 423 MathML formulas, 0 `temml-error` nodes. All 8 SVG figures populated. |
| 2 Layout | PASS: on all 8 tabs at both widths, 0 polyline-over-label hits (sampled every 2 px along each polyline), 0 label-on-label overlaps, 0 figures clipped past the viewBox, 0 px horizontal page overflow at 390. Re-checked on t6 with the energy shock selected and with the indeterminate rule (φπ = 0.8). |
| 3 Navigation | PASS: ← from tab 1 goes to tab 8, → from tab 8 goes to tab 1. Prev / Sources / next footer on every tab. |
| 4 Citations | PASS: 117 `#src-` anchors, 0 unresolved. Paper DOIs checked on Crossref (research.md §0). |
| 5 Interactivity | PASS: see the readouts below. |
| 6 Numbers | PASS: 198 distinct numbers in the visible text; every one traces to research.md (11 slider defaults, annualised values and dates were added to the dossier after the first trace). |
| 7 Math source | PASS: rigorous-explainer `checktex` (423 segments, 0 issues), `checklt` 0, `check_links` 0 broken, `check_prose` 0 flags, `check_proofs` 0 propositions without a proof. |

## Interactive readouts (default settings, 1280)
| Figure | Readout | Expected (research.md §7) |
|---|---|---|
| Fig 3 news, ρw = 0.9 | Δc = 0.167 | r/(1+r−ρw) = 0.167 |
| Fig 3 layoff | fall 0.820 at period 5, none at 15 | (1.02)^−10 = 0.820 |
| Fig 4 seed 2026 | slope −0.0372, t = −3.02, reject | true slope −0.020; approx. t ≈ 2.1 in expectation |
| Fig 4 resample | slope −0.0101, t = −1.37, do not reject | shows the test's limited power at N = 120 |
| Fig 5 θ = 0.75 | κ = 0.1717, printed form 0.0069, ratio 25.0 | 0.1717 / 0.00687 |
| Fig 6 policy shock | gap −0.259%, π −0.352 pp/yr, i +0.342, real +0.518 | −0.259, −0.088×4, 0.0855×4, 0.1295×4 |
| Fig 6 energy shock | gap +0.085%, output −0.915%, natural −1.000%, π +0.538, i +0.850 | same |
| Fig 6 φπ = 0.8 | “indeterminate”, lines faded | κ(φπ−1)+(1−β)φy = −0.033 < 0 |
| Fig 7 k = 8 | gap +0.25%, π +1.48 pp/yr (8.6× a cut now) | 4 × 0.371 |

## Issues
| # | Sev | Location | Issue | Status |
|---|---|---|---|---|
| m1 | minor | t2 Fig 2 | The two lines of the green annotation overlapped by 2 px. | Fixed (spacing). Run 2: 0 overlaps. |
| m2 | minor | t5 at 390 px | A display formula inside a result box widened the page by 9 px. | Fixed (`.res`, `.deriv` scroll horizontally). Run 2: 0 px. |
| m3 | trivial | t6 lower panel | The determinacy plane scaled to 1.5× the IRF text size at 1280. | Fixed (max-width 640 px). |

## Not tested
Screen readers; Firefox and Safari MathML rendering (Chrome only); browsers older than Chromium 109, which lack MathML Core.

## Content checks against the committee documents
- Four printed problems in [SB] are flagged on the page, not silently corrected: κ on p. 36 (derived form used; the printed form fails the θ → 1 limit), the π timing in the Euler equation on p. 31, the 2025/2021 date conflict on p. 47–48, and the hours sign on p. 28.
- Claims from outside the committee documents are labelled: Hall (2005) on wage stickiness (tag “not part of the citation”), Bullard & Mitra (2002) for the determinacy condition, Woodford (2003) ch. 6 for the welfare loss (stated, not derived), RePEc Genealogy for Hall's BA and adviser.
- No currency conversion of the prize and no age for Hall: the sources do not give them.
