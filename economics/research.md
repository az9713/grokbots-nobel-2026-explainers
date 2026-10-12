# 2026 Prize in Economic Sciences: research dossier

Audience: technically trained readers without a macroeconomics background. Every number on the page traces to this file. **[SB]** = the committee's Scientific Background (12 Oct 2026, 57 pp.), the primary anchor; page numbers are the printed page numbers. Tags: **FACT** (stated in a primary source), **DERIVED** (our algebra or arithmetic from sourced inputs; the steps are on the page), **SPEC** (open question, or the committee itself hedges it). Local copies were read in full (PyMuPDF text extraction, symbols checked against the rendered PDF).

## 0. Primary sources
- [PR] Press release, 12 Oct 2026: https://www.nobelprize.org/prizes/economic-sciences/2026/press-release/
- [POP] Popular science background, "Microfoundations deliver macro insights": https://www.nobelprize.org/uploads/2026/10/popular-economicsciencesprize2026.pdf
- [SB] Scientific background, "Microeconomic foundations of macroeconomic stabilization": https://www.nobelprize.org/uploads/2026/10/advanced-economicsciencesprize2026.pdf

Papers (DOIs checked on Crossref, 12 Oct 2026):
- [Hall1978] Hall, JPE 86(6) 971–987, doi:10.1086/260724
- [HM1982] Hall & Mishkin, Econometrica 50(2) 461, doi:10.2307/1912638
- [Hall1988] Hall, JPE 96(2) 339–357, doi:10.1086/261539
- [Flavin1981] Flavin, JPE 89(5) 974–1009, doi:10.1086/261016
- [CM1989] Campbell & Mankiw, NBER Macro Annual 4 185–216, doi:10.1086/654107
- [Lucas1976] Lucas, Carnegie-Rochester 1 19–46, doi:10.1016/S0167-2231(76)80003-6
- [Calvo1983] Calvo, JME 12(3) 383–398, doi:10.1016/0304-3932(83)90060-0
- [Taylor1993] Taylor, Carnegie-Rochester 39 195–214, doi:10.1016/0167-2231(93)90009-L
- [RW1997] Rotemberg & Woodford, NBER Macro Annual 12 297–346, doi:10.1086/654340
- [W1998] Woodford, Review of Economic Dynamics 1 173–219, doi:10.1006/redy.1997.0006
- [CGG1999] Clarida, Galí & Gertler, JEL 37(4) 1661–1707, doi:10.1257/jel.37.4.1661
- [W2003] Woodford, *Interest and Prices*, Princeton UP 2003, doi:10.2307/j.ctv30pnvmf
- [BM2002] Bullard & Mitra, JME 49 1105–1129, doi:10.1016/S0304-3932(02)00144-7 (not cited by [SB]; source of the determinacy condition)
- [DGP2023] Del Negro, Giannoni & Patterson, JPE Macro 1(1) 43–79, doi:10.1086/724214
- [JPS2006] Johnson, Parker & Souleles, AER 96(5) 1589–1610, doi:10.1257/aer.96.5.1589
- [P2013] Parker, Souleles, Johnson & McClelland, AER 103(6) 2530–2553, doi:10.1257/aer.103.6.2530
- [BFJ2025] Boehm, Fize & Jaravel, AER 115(1) 1–42, doi:10.1257/aer.20240138
- [HS2020] Havranek & Sokolova, RED 35 97–122, doi:10.1016/j.red.2019.05.004
- [SW2007] Smets & Wouters, AER 97(3) 586–606, doi:10.1257/aer.97.3.586
- [KP1982] Kydland & Prescott, Econometrica 50 1345, doi:10.2307/1913386
- [Zeldes1989] Zeldes, QJE 104(2) 275, doi:10.2307/2937848
- [Hall2005] Hall, "Employment fluctuations with equilibrium wage stickiness", AER 95(1) 50–65, doi:10.1257/0002828053828482 (**not cited by [SB] or [PR]**; see §6)

## 1. The prize (FACT [PR], [POP])
- Announced 12 Oct 2026. Sveriges Riksbank Prize in Economic Sciences in Memory of Alfred Nobel 2026 to **Robert E. Hall** (Stanford University) and **Michael Woodford** (Columbia University), "for microeconomic foundations of macroeconomic stabilisation". 12 million SEK, shared equally.
- Hall: born 1943, Palo Alto, CA. PhD 1967, MIT. Woodford: born 1955, Chicopee, MA. PhD 1983, MIT. [PR]
- Chair John Hassler quote: "The laureates' work has provided us with a stable theoretical foundation for the models that are now used by central banks and governments around the world. With them, we are better equipped to deal with shocks in the economy, such as energy crises or sudden changes in how much households consume." [PR]
- Secondary (not in committee documents; RePEc Genealogy, Mathematics Genealogy, Wikipedia): Hall's BA is from UC Berkeley (1964); his MIT thesis "Essays on the Theory of Wealth" was supervised by Robert Solow. Used on the page only as a tagged aside.

## 2. Background: the Keynesian framework and why it broke (FACT [SB] §2, pp. 6–10)
- Keynesian consumption function C = α + γ(Y − T), γ ∈ (0,1) the marginal propensity to consume (MPC). With Y = C + I + G: Y = (α + I + G − γT)/(1 − γ), eq. (1). [SB p. 7]
- γ ≈ 2/3 gives a spending multiplier 1/(1 − γ) ≈ 3 and a transfer ("check") multiplier γ/(1 − γ) = 2. [SB p. 7 and fn. 7] (CARES Act 2020 checks as the example.)
- LM: M/P = L(Y, i). IS-LM by Hicks (1972 laureate). Phillips (1958) curve; AS-AD. [SB pp. 7–8]
- 1970s stagflation: the Phillips curve appeared to shift outward. Lucas critique (Lucas 1976; 1995 laureate): reduced-form coefficients change when policy changes. Kydland & Prescott (1982) RBC model (2004 laureates). [SB pp. 9–10]
- Phelps (2006 laureate) expectations-augmented Phillips curve as an intermediate case. [SB fn. 9, fn. 30]

## 3. Hall (FACT [SB] §3, pp. 11–25 unless tagged)
- Household problem (3)–(6): max E_t Σ_{τ=0}^{T} β^τ u(c_{t+τ}), a_{t+τ+1} = (1 + r)(a_{t+τ} − c_{t+τ} + w_{t+τ}), c ≥ 0, a_{t+T+1} ≥ 0. β ∈ (0,1). u strictly increasing, strictly concave. r > 0 constant; earnings w stochastic.
- Consolidated budget: Σ_{τ=0}^{T} (c_{t+τ} − w_{t+τ})/(1 + r)^τ = a_t. (7)
- Euler equation (8): u′(c_t) = (1 + r)^τ β^τ E_t u′(c_{t+τ}).
- β(1 + r) = 1 and quadratic u = −½(φ − c)² give closed form (9): c_t = [r/(1 + r − (1 + r)^{−T})] (a_t + w_t + E_t Σ_{τ=1}^{T} w_{t+τ}/(1 + r)^τ). As T → ∞ the propensity is r/(1 + r). At r ≈ 2%/yr the MPC is ≈ 1/50, against 2/3 in the Keynesian function. [SB p. 16]
- Test (10): u′(c_{t+1}) = ((1 + r)β)^{−1} u′(c_t) + ε_{t+1}, E_t ε_{t+1} = 0. Quadratic: (11) c_{t+1} = φ(1 − ((1 + r)β)^{−1}) + ((1 + r)β)^{−1} c_t − ε_{t+1}. β(1 + r) = 1: (12) E_t c_{t+1} = c_t, a martingale. [SB pp. 16–17]
- Rule of thumb (13): fraction μ hand-to-mouth: c_{t+1} − c_t = μ(y_{t+1} − y_t) − (1 − μ)ε_{t+1}. [SB p. 17]
- Result: after controlling for current consumption, disposable income and its lags have minimal predictive power for future nondurable consumption, quarterly aggregate US data. Asset-market valuation (stock prices) had some, though moderate, predictive power. [SB pp. 18–19]
- Before Hall: distributed-lag proxies for permanent income; Muth (1960) showed geometric lags are the rational forecast only for a specific income process. [SB p. 12]
- Follow-ups: Flavin (1981) excess sensitivity ≈ 0.36, MPC out of current income 16.75%. [SB p. 20] Campbell & Mankiw (1989) hand-to-mouth share ≈ 0.5 in aggregate data for Canada, France, Germany, Italy, Japan, US, using lagged consumption changes as instruments. [SB p. 21] Hall (1988a) CRRA u = (c^{1−σ} − 1)/(1 − σ), IES = 1/σ ≈ 0.1; Yogo (2004) confirms after weak-instrument correction. [SB pp. 21–22] Deaton & Campbell (1989) "excess smoothness". Zeldes (1989b): with CRRA the martingale holds for marginal utility, not for consumption; deviations from certainty equivalence can explain excess sensitivity. [SB p. 20]
- Hall & Mishkin (1982): PSID food consumption, **2,309 families, 1969–1975**; hand-to-mouth fraction **20%**, the other **80%** follow the rational-expectations PIH. [SB pp. 22–23; POP p. 4 "around 80 per cent"]
- Modern MPC evidence: Johnson et al. (2006) 2001 rebates **20–40% over three months**; Parker et al. (2013) 2008 payments **12–30%**; Boehm et al. (2025) France experiment **23% over a month**; Havranek & Sokolova (2020) meta-analysis mean **21%**, **11%** after publication-bias correction. [SB p. 24]
- Hall's "rule of thumb" precursor of Huggett (1993), Aiyagari (1994) heterogeneous-agent models; HANK. [SB pp. 25, 41]

## 4. Woodford and the New Keynesian model (FACT [SB] §4, pp. 25–46 unless tagged)
- Woodford's papers building the model date from the 1990s (1991–1999), summarised in the 2003 book. [SB p. 4]
- Prerequisites by others: Taylor (1979), Rotemberg (1982a,b), Calvo (1983), Blanchard & Kiyotaki (1987). Woodford's own steps: Rotemberg & Woodford (1992), Woodford (1994, 1995a), RW (1996a,b, 1997, 1999), Woodford (1996a, 1998, 1999b). Julio Rotemberg died in 2017. First version of the NK model as described: Woodford (1996b); natural-output definition in Woodford (1999b). Yun (1996) close precedent. [SB pp. 4, 26]
- NK IS (14): ỹ_t = E_t ỹ_{t+1} − (1/σ)(i_t − E_t π_{t+1} − r^n_t). NKPC (15): π_t = β E_t π_{t+1} + κ ỹ_t. Rule (16): i_t = ρ + φ_π π_t + φ_y ỹ_t + v_t, φ_π > 1; ρ = 1/β − 1. [SB pp. 27–29, 36]
- Household with hours: u(C, H) = (C^{1−σ} − 1)/(1 − σ) − χ H^{1+1/ψ}/(1 + 1/ψ). Budget P_t C_t + Q_t B_{t+1} = B_t + W_t H_t + Π_t, 1/Q_t − 1 ≡ i_t. FOCs: C_t^{−σ} = β E_t[(1 + i_t)/(1 + π_{t+1}) C_{t+1}^{−σ}] (the [SB] prints π_t in the denominator on p. 31 but π_{t+1} on p. 35; we use π_{t+1}, consistent with its definition π_{t+1} ≡ (P_{t+1} − P_t)/P_t), C^{−σ} W/P = χ H^{1/ψ}. [SB pp. 30–31]
- Dixit–Stiglitz aggregator C = (∫ C(i)^{(ε−1)/ε} di)^{ε/(ε−1)}; price index (17) P = (∫ P(i)^{1−ε} di)^{1/(1−ε)}; demand C(i) = C (P(i)/P)^{−ε}; production Y(i) = A H(i); flexible price P(i) = [ε/(ε − 1)] W/A, markup μ = ε/(ε − 1), needs ε > 1. [SB pp. 31–32]
- Natural output (fn. 35): Y^n = μ^{−ψ/(ψσ+1)} A^{(ψ+1)/(ψσ+1)} (χ = 1). Natural rate: 1 = β(1 + r^n_t)(A_{t+1}/A_t)^{−σ(ψ+1)/(ψσ+1)}. [SB p. 33] DERIVED: we re-derived both from the labour FOC, W/P = A/μ and Y = AH; they match.
- Calvo: reset probability 1 − θ; index recursion (18) P_t^{1−ε} = (1 − θ)(P*_t)^{1−ε} + θ P_{t−1}^{1−ε}. Reset-price problem with Q_{t,t+s} = β^s (C_{t+s}/C_t)^{−σ} P_t/P_{t+s}. [SB pp. 33–34]
- κ: [SB p. 36] prints **(1 − β)(1 − βθ)(1/ψ + σ)/θ**. DERIVED: the standard Calvo derivation (ours, on the page; also [W2003] ch. 3, [CGG1999]) gives **κ = (1 − θ)(1 − βθ)(σ + 1/ψ)/θ**. Discriminating check: as θ → 1 (prices never reset) the slope must go to 0. (1 − θ) does; the printed (1 − β) gives (1 − β)²(σ + 1/ψ) ≠ 0. At β = 0.99, θ = 0.75, σ = 1, 1/ψ = 1: derived κ = 0.1717, printed form 0.00687, a factor of 25. We treat the printed form as a typo.
- [SB p. 28] says “a higher output gap means lower hours worked relative to their natural level”. DERIVED: with Y = AH, ỹ = h − hⁿ, so a higher gap means more hours; we read this as a slip and flag it on the page.
- One-off policy shock: ỹ_t = −(1/σ)(φ_π κ ỹ_t + φ_y ỹ_t + v_t) ⇒ ỹ_t = −v_t/(σ + φ_π κ + φ_y). [SB p. 37] One-off productivity rise lowers the gap. [SB p. 37]
- Energy shock (lower A, persistent): actual output falls, natural output falls more, gap positive, central bank raises rates. [SB pp. 37–38; POP p. 5]
- Forward guidance; US ZLB usually dated **2008–2015**. [SB p. 38]
- Cashless limit (Woodford 1998): M/P → 0 with finite P. φ_π > 1 gives local determinacy, not global (Benhabib et al. 2001). Fiscal theory of the price level (Woodford 1995b). [SB pp. 38–40]
- Divine coincidence: replace ρ with r^n_t; π = ỹ = 0 for any φ (Blanchard & Galí 2007 name). Lost with sticky wages or cost-push shocks. [SB pp. 41–42 and fn. 52–53]
- Timeless perspective (Woodford 1999a); time inconsistency (Kydland & Prescott 1977, Barro & Gordon 1983). [SB p. 42]
- Smets–Wouters: 7 shocks [SB fn. 47]. DYNARE by Michel Juillard, 1994 [SB fn. 55]. Riksbank MAJA (Corbo & Strid 2020): **29 exogenous shocks, 16 domestic**; Sweden: about half of demand from exports. [SB pp. 43–44]
- Challenges: linearization misses the ZLB nonlinearity; rational expectations and anchoring; Calvo/Rotemberg ad hoc (Golosov & Lucas 2007); forward guidance puzzle (Del Negro et al. 2023). [SB pp. 45–46] SPEC: "no single explanation has emerged as a consensus".

## 5. Policy evaluation (SPEC: the committee hedges, [SB] pp. 46–48)
- Faster rebound after the Great Recession than after the Great Depression (Eichengreen & O'Rourke 2010); Covid (De Grauwe & Ji 2020). [SB] compares the recent shock with the 1973 oil-price shock. Recent inflation burst not followed by 1970s-style stagflation (Ari et al. 2023; Forbes et al. 2024; Blanchard & Bernanke 2024; Forbes et al. 2025).
- The [SB] dates this inflation burst "beginning in 2021" (p. 47) and, two pages later, as "the recent inflation shock that began in 2025" (p. 48). The cited studies date from 2023–2025, so they cannot evaluate a shock that began in 2025; we use 2021 and flag the inconsistency.
- Verdict quoted: "it is hard to prove beyond reasonable doubt that the relatively quick rebound ... [is] due to better monetary and fiscal stabilization policy, there does seem to be a consensus that they have played a very important role." [SB p. 48]

## 6. Items in the user's brief that the committee documents do not support
- "Hall analyzed how wage rigidity amplifies recessions and unemployment." Hall did publish on this ([Hall2005]), but neither [SB] nor [PR] cites it. Page: one sentence, tagged "not part of the citation".
- "about $1.2M": no currency conversion in the sources. Page uses 12 million SEK only.
- "Hall, now 82": [PR] gives only the birth year (1943). Page gives the year only.

## 7. DERIVED results on the page (all our algebra, checked numerically in `model_check.py`, scratchpad)
- MPC out of an AR(1) earnings innovation (persistence ρ_w), β(1 + r) = 1, quadratic u, T → ∞: Δc_{t+1} = r/(1 + r − ρ_w) · e_{t+1}. r = 0.02: ρ_w = 0 → 0.0196; 0.9 → 0.167; 0.95 → 0.286; 1 → 1.
- NK model, AR(1) policy shock persistence ρ_v: ỹ = −(1 − βρ_v)Λ v, π = −κΛ v, Λ = 1/[(1 − βρ_v)(σ(1 − ρ_v) + φ_y) + κ(φ_π − ρ_v)]. Checked against a numerical fixed-point solve (agreement 1e−12). ρ_v = 0 reproduces the [SB] one-off formula.
- Multipliers at the permanent-income MPC γ = 0.0196: spending 1/(1 − γ) = 1.02, cheques γ/(1 − γ) = 0.02. Printed-κ value 0.00687 is shown rounded as 0.0069.
- Calibration used in figures (ours, labelled as such): β = 0.99, σ = 1, 1/ψ = 1, θ = 0.75 (mean price duration 1/(1 − θ) = 4 quarters), φ_π = 1.5, φ_y = 0.125, ρ_v = 0.5, v_0 = 0.25. Impact: ỹ_0 = −0.259, π_0 = −0.088 (quarterly), i_0 − ρ = +0.086, real rate +0.130.
- Determinacy ([BM2002], [W2003] ch. 4): unique bounded solution iff κ(φ_π − 1) + (1 − β)φ_y > 0 (for φ ≥ 0). Checked against eigenvalues on a 61 × 41 grid: 0 mismatches.
- Energy shock: a_0 = −0.01, ρ_a = 0.9, ψ_ya = (1 + ψ)/(1 + σψ) = 1: y^n_0 = −1.00%, r̂^n_0 = +0.10 pp, gap +0.085%, output −0.915%, π_0 = +0.13 pp, i_0 − ρ = +0.21 pp (annualised ×4: 0.54 and 0.85).
- Forward guidance (real-rate path set directly): a one-quarter real-rate cut x at horizon k raises today's gap by x/σ for every k and today's inflation by κ(x/σ)(1 − β^{k+1})/(1 − β). x = 0.25: k = 0 → 0.043; 4 → 0.210; 20 → 0.817; 40 → 1.449.
- Welfare: second-order loss ∝ Σ β^t [π_t² + (κ/ε) ỹ_t²] ([W2003] ch. 6; not derived in [SB]). ε = 6: weight 0.029.
- Hall test simulation: stylized, not Hall's data. Approximate t-statistic for μ = 0.2, ρ_w = 0.9, N = 120 quarters, quarterly r = 0.005: ≈ 2.1.
