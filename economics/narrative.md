# Economics 2026 explainer: narrative and figure specs

Source of every number: `research.md`. Citation keys in [brackets] match its §0. Tags shown to the reader: **Established**, **Evidence**, **Open**, and **Our derivation** on DERIVED results. Math is written in LaTeX and compiled to native MathML at build time (Temml), so the page makes 0 external requests.

## Global layout
Same shell as `chemistry/`: dark mode, sticky masthead, 8 tabs, a Takeaway box at the top of each tab, terms bold on first use with a hover definition, a footer with prev / Sources / next. Every derivation is numbered and every interactive figure states the model and calibration it runs.

## Spine
A recession or an energy shock hits. What should the central bank and the treasury do, and how do we know? The old answer used stable correlations (IS-LM, the Phillips curve). The 1970s broke them. Hall gave the demand side a testable, forward-looking foundation. Woodford built the full model on it. Each tab changes one part of that model.

## Tabs
1. **The prize.** Citation, laureates, what each contributed, the one-paragraph version, a timeline from Keynes (1936) to forward guidance (2008–2015).
2. **The old model and the Lucas critique.** Keynesian consumption function, multiplier derivation (eq. 1), γ = 2/3 → 3 and 2. LM. Phillips curve. Stagflation. Lucas critique stated formally: reduced-form coefficients are functions of policy parameters. Fig 2: multiplier against MPC, with the PIH MPC marked.
3. **Hall I: the forward-looking consumer.** Problem (3)–(6), consolidated budget (7), Euler equation (8) derived by a perturbation argument, consumption smoothing, quadratic closed form (9), MPC r/(1 + r). Our derivation: MPC out of AR(1) news r/(1 + r − ρ_w). Interactive Fig 3: persistence slider, consumption and income paths; anticipated versus unanticipated layoff.
4. **Hall II: the random-walk test and what it found.** Expectational error (10), linear form (11), martingale (12), the test logic (orthogonality), hand-to-mouth (13), evidence table (Flavin, Hall & Mishkin, Campbell & Mankiw, Hall 1988a, modern MPCs). Interactive Fig 4: Monte Carlo of the test with μ and N sliders.
5. **Woodford I: firms that set prices.** Dixit–Stiglitz, price index, markup, natural output and natural rate (fn. 35), Calvo, derivation of the NKPC, κ formula with the SB typo noted. Interactive Fig 5: θ slider → duration and κ.
6. **Woodford II: the three-equation model.** NK IS derived from the Euler equation, NKPC, Taylor rule, cashless limit, determinacy (Taylor principle) with the Bullard–Mitra condition. Interactive Fig 6: IRF lab (policy shock / energy shock), sliders σ, θ, φ_π, φ_y, ρ; determinacy readout. Fig 6b: determinacy region.
7. **Policy: what the model changed.** Supply versus demand shocks need opposite responses; divine coincidence; welfare loss; forward guidance and the puzzle (interactive Fig 7: horizon k); fiscal transfers and the central-bank offset; MAJA; the committee's hedged evaluation.
8. **Limits, open questions, sources.** Challenges list; Established / Evidence / Open columns; credit note; notes on the SB's printed typos; sources with DOIs.

## Excluded (not supported by the committee documents)
Dollar conversion of the prize; Hall's age; any claim that the 2025 shock is evaluated by the cited studies.
