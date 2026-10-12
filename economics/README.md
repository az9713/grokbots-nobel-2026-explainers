# The 2026 Prize in Economic Sciences: building macroeconomics from the bottom up

[![View live explainer](https://img.shields.io/badge/View_live_explainer-az9713.github.io-f5a623?style=for-the-badge)](https://az9713.github.io/grokbots-nobel-2026-explainers/economics/)

**Live page: https://az9713.github.io/grokbots-nobel-2026-explainers/economics/**

[![Screenshot of the explainer's first tab](docs/screenshot.png)](https://az9713.github.io/grokbots-nobel-2026-explainers/economics/)

## Summary

This is an interactive, single-page explainer of the 2026 Sveriges Riksbank Prize in Economic Sciences in Memory of Alfred Nobel. The prize is shared equally by Robert E. Hall and Michael Woodford "for microeconomic foundations of macroeconomic stabilisation". Hall showed that a rational, forward-looking consumer makes future changes in consumption unpredictable, and turned that into a test that aggregate data largely passed. Woodford built on it the New Keynesian model that central banks use to set interest rates. It is written for technically trained readers with no macroeconomics background. Every result tagged “Our derivation” is derived on the page; the one stated result (Woodford's welfare loss) is labelled as such. The figures run the model in the browser, and claims are tagged by strength of evidence.

## The 8 tabs

1. The prize
2. The old model breaks (multiplier, Lucas critique)
3. Hall: the consumer (Euler equation, permanent income, MPC out of news)
4. Hall: the test (random walk, hand-to-mouth households, evidence)
5. Woodford: sticky prices (Dixit–Stiglitz, natural rate, Calvo, Phillips curve)
6. The three equations (IS curve, Taylor rule, determinacy, impulse responses)
7. Policy (supply vs demand shocks, divine coincidence, welfare, forward guidance)
8. Limits & sources

## Files

| File | What it is |
| --- | --- |
| `index.html` | The explainer that GitHub Pages serves (self-contained HTML, CSS, JS, inline SVG and native MathML) |
| `nobel-economics-2026-explainer.html` | The same page under a filename that matches the other three folders |
| `research.md` | Source research with DOIs, claim tags and the derived results |
| `narrative.md` | The narrative and figure specs the page was built from |
| `qa/REPORT.md` | The QA report at 1280 and 390 px |

## How it was made

A single Claude Code session (not the GrokBots agent team that built the other three explainers) read the committee's 57-page scientific background in full, derived and numerically checked every result, wrote the page in LaTeX, compiled the formulas to native MathML with Temml so the page loads nothing from the network, and ran the QA in headless Chrome.

## Sources

The main source is the committee's [scientific background](https://www.nobelprize.org/uploads/2026/10/advanced-economicsciencesprize2026.pdf), together with the [popular science background](https://www.nobelprize.org/uploads/2026/10/popular-economicsciencesprize2026.pdf), the [press release](https://www.nobelprize.org/prizes/economic-sciences/2026/press-release/) and the papers they cite. The page flags four printed errors in the scientific background, including the Phillips-curve slope on p. 36. The full citations with DOIs are in `research.md` and on the page's last tab.
