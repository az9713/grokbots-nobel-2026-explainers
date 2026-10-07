# 2026 Nobel Prize in Physics: research dossier (Rex Research)

Audience: MIT PhDs without particle/astro background. Every number below is tagged with its source. **[SB]** = Nobel Committee Scientific Background (6 Oct 2026), the primary anchor. Tags: **FACT** (stated in a primary source), **DERIVED** (my arithmetic from sourced inputs; formula shown), **SPEC** (open question or interpretation; the committee itself hedges it). Local copies: `src/adv.pdf`, `src/adv.txt`, `src/pop.pdf`.

## 0. Primary sources
- [SB] Scientific Background: https://www.nobelprize.org/uploads/2026/10/advanced-physicsprize2026.pdf (mirror: https://www.kva.se/app/uploads/2026/10/nobel-physics-2026-scientific-background_34f71vieby.pdf)
- [PR] Press release: https://www.nobelprize.org/prizes/physics/2026/press-release/
- [POP] Popular background: https://www.nobelprize.org/uploads/2026/10/popular-physicsprize2026.pdf
- [S2013] IceCube, Science 342 (2013) 1242856, 28 events (doi:10.1126/science.1242856)
- [PRL2013] IceCube, PRL 111 (2013) 021103, the first two PeV events
- [PRL2014] IceCube, PRL 113 (2014) 101101, 5.7σ over three years
- [TXS-MM] IceCube et al., Science 361 (2018) eaat1378, IceCube-170922A + TXS 0506+056
- [TXS-ARCH] IceCube, Science 361 (2018) 147, the 2014–15 archival flare
- [NGC] IceCube, Science 378 (2022) 538, NGC 1068
- [GAL23] IceCube, Science 380 (2023) 1338, Galactic plane
- [GAL26] IceCube, arXiv:2607.25966 (preprint, no journal version as of 7 Oct 2026), Galactic plane at 5.7σ
- [TAU] IceCube, PRL 132 (2024) 151001, seven tau neutrinos
- [SPEC26] IceCube, PRL 136 (2026) 121002, doi:10.1103/2gh9-d4q7 (arXiv:2507.22233), and PRD 113 (2026) 062002, doi:10.1103/4n6v-r7n4 (arXiv:2507.22234). Combined spectrum and an 11.4 PeV event. DOIs checked on Crossref 7 Oct.
- [DET] IceCube, JINST 12 (2017) P03012, detector paper
- [HK] Halzen & Kheirandish, arXiv:2202.00694, multimessenger energy relations

## 1. The prize (all FACT)
- Awarded 6 Oct 2026 by the Royal Swedish Academy of Sciences. The full prize (1/1) goes to **Francis Halzen**, University of Wisconsin–Madison, "for decisive contributions to the IceCube Neutrino Observatory and the discovery of high-energy neutrinos of astrophysical origin." [PR]
- Halzen was born in 1944 in Tienen, Belgium, and earned his PhD at KU Leuven in 1969. The prize is 12 million SEK. [PR]
- Quote from Mark Pearce, Chair of the Nobel Committee for Physics: "His tenacity and scientific vision has paved the way for a new kind of astronomy." [PR]
- Halzen's role: IceCube PI from the 1999 NSF proposal onward, "a driving force" on AMANDA, and co-author (with J. Learned, June 1988) of the first proposal to use ice as both the target and the Cherenkov radiator. [SB]
- IceCube collaboration: about 450 people, 58 institutions, 14 countries. It is an NSF-managed facility. [SB]

## 2. Earlier neutrino Nobels, for a timeline (FACT [SB])
1930 Pauli postulates the neutrino (Nobel 1945, for the exclusion principle) · 1956 Cowan & Reines detect reactor antineutrinos (Nobel 1995, to Reines) · 1988 Nobel to Lederman, Schwartz & Steinberger for the muon neutrino · 2002 Nobel to Davis & Koshiba for MeV solar neutrinos and SN 1987A (160,000 ly away) · 2015 Nobel to Kajita & McDonald for oscillations (neutrinos have mass) · 2026 Halzen, for PeV astrophysical neutrinos.
- There are three flavours (νe, νμ, ντ), each a superposition of three mass states. The masses are sub-eV and their ordering is unknown. [SB]

## 3. Backgrounder
### 3.1 Why neutrinos are good messengers (FACT [SB])
They are neutral and feel only the weak force and gravity. That means magnetic fields don't bend them, and they escape optically thick sources and cross the universe without being absorbed by extragalactic background light or the CMB. Gamma rays fail on the second count, and gamma rays can also come from electrons (synchrotron and inverse Compton), which makes it hard to tell what is producing them. Charged cosmic rays fail on the first count.

### 3.2 Cosmic rays (FACT [SB])
- Discovered in 1912 by Hess (Nobel 1936). They are mostly protons and helium nuclei.
- The spectrum reaches about 10^20 eV, compared with 7 TeV per beam at the LHC. It is a broken power law: the **knee** sits at a few PeV (below it, sources are Galactic and probably supernovae), the **ankle** at a few EeV (above it, the flux is extragalactic, and about 1 particle reaches each km² per year). The **GZK cutoff** sets in above about 50 EeV, where cosmic rays interact with CMB photons.
- The **Hillas criterion** says the size and magnetic field of a source must be large enough to confine a particle until it reaches the required energy.
- Acceleration happens by first-order Fermi acceleration at shocks, for example at AGN jet termination shocks.

### 3.3 How a cosmic accelerator makes neutrinos (FACT [SB]; good material for a figure)
- pp: p_CR + p_target → π^0, π^± + X. pγ: p + γ → Δ⁺(1232 MeV, spin 3/2) → p π^0 or n π⁺.
- π^0 → γγ. π⁺ → μ⁺ ν_μ, followed by μ⁺ → e⁺ ν_e ν̄_μ.
- Gamma-to-neutrino energy-flux relation: $E_\gamma^2 \frac{dN_\gamma}{dE_\gamma} \approx \frac{4}{3K_\pi} E_\nu^2 \frac{dN_\nu}{dE_\nu}\Big|_{E_\nu=E_\gamma/2}$, with K_π ≈ 2 for pp and K_π ≈ 1 for pγ. [SB, HK] (The PDF's text extraction garbles the prefactor. I read it as 4/(3K_π), which matches Halzen–Kheirandish. **Tess: please check this against the PDF rendering.**)
- In photoproduction the pion carries about 20% of the proton's energy, a gamma ray about 1/10 of it, and a neutrino about 1/20. So PeV–EeV protons show up as neutrinos from tens of TeV to tens of PeV. [SB]
- **Flavour ratio** at the source is about 1:2:0 (νe:νμ:ντ). Oscillation over cosmic distances turns it into roughly 1:1:1 at Earth. (This is standard physics, but **not stated in [SB]**. It is the reason any tau neutrino above 100 GeV must be astrophysical; see §5.6.)

### 3.4 Detection: weak interaction and DIS (FACT [SB])
- Above a TeV, deep inelastic scattering on quarks dominates. In a charged-current (W) interaction, ν_l + N → l⁻ + X, so you get a lepton plus a hadronic cascade. In a neutral-current (Z) interaction, ν + N → ν + X, so you get only the cascade.
- Cross-section at a PeV: σ ~ 10^-33 cm². The astrophysical spectrum falls roughly as E^-2.5. Together these make a **km³** detector necessary.
- DERIVED, for intuition on why km³: the nucleon density of ice is ≈ 0.92 g/cm³ × 6.0×10^23 /g ≈ 5.5×10^23 cm^-3. The mean free path is λ = 1/(nσ) ≈ 1.8×10^9 cm ≈ 18,000 km. That is longer than Earth's diameter (12,742 km), which is also why PeV neutrinos coming up through the Earth get absorbed. A 1 km path has about a 1 in 18,000 chance of interacting. Label this as an order-of-magnitude estimate.

### 3.5 Cherenkov light (FACT [SB], plus DERIVED)
- A charged particle emits Cherenkov light when v > c/n. In water (n = 1.33) the threshold is 0.75c, which means 160 MeV for a muon. The light is mostly UV. [SB]
- Ice has n ≈ 1.31 and is birefringent [SB, citing The Cryosphere 18 (2024) 75].
- DERIVED: cos θ_C = 1/(nβ), so for β→1 and n = 1.31, **θ_C ≈ 40°**.
- Ice below about 2100 m: the absorption length is ~200 m and the scattering length ~50 m. [SB] Between 800 and 1000 m, 50 µm air bubbles cut the scattering length below 50 cm. This was found with AMANDA and is why IceCube was built deeper. [SB]

## 4. The detector (FACT [SB] unless tagged)
- History: Halzen & Learned's preprint, June 1988 → 1991 PMTs in Greenland boreholes prove the ice is transparent enough (Nature 353, 331) → AMANDA, 1993–2000, holes drilled with hot water, atmospheric neutrinos published in Nature 410 (2001) 441, decommissioned 2009 → IceCube proposal to NSF 1999 → funded March 2002 → construction 2004 → strings deployed 2005–2010 → complete in **2011** → uptime above 99% since.
- Before that, DUMAND (4800 m deep off Hawaii) deployed one string in 1993, which failed. It was cancelled in 1995, with ocean bioluminescence and ⁴⁰K as background problems. Water-based successors: Baikal, ANTARES, KM3NeT.
- Geometry: **86 strings × 60 optical sensors (DOMs)**. That gives **5,160** DOMs (DERIVED; [SB] says "over 5000"). Sensors sit every **17 m**, at depths of **1450–2450 m**, in a hexagonal array with **125 m** spacing. The volume is about **1 km³**, a target mass of **about 1 Gt**. Each DOM has a downward-facing 25.4 cm (10″) PMT with onboard digitization and sends data up over optical fibre.
- **IceTop** is a surface array of ice Cherenkov detectors. It measures air showers from 300 TeV to 1 EeV and acts as a veto over a limited solid angle.
- Figure inputs: strings shown as vertical lines; the instrumented depth band is 1 km tall; a dust layer is worth noting **only if verified** (I did not source a dust-layer depth, so leave it out or mark it as a placeholder).

## 5. Events and analysis
### 5.1 Topologies (FACT [SB])
| | Track (CC ν_μ) | Cascade (CC νe/ντ, NC all flavours) |
|---|---|---|
| Shape | muon crosses the array; range ~km at TeV, tens of km at EeV | shower under ~10 m long, so the light pattern looks spherical |
| Angular resolution | **0.3° at 100 TeV** | **~5° above 50 TeV** |
| Energy resolution | factor of ~2 on the muon energy (losses are stochastic) | **~8% at 100 TeV** (contained) |
| Effective volume | much larger than the instrumented volume | about the instrumented volume |
- Tau "double bang": two cascades. The tau decay length is about **50 m per PeV**, so seeing both cascades needs favourable geometry.
- Example events from [SB] Fig. 4: a cascade depositing 1.14 PeV, and a track depositing 2.6 PeV coming from 11° below the horizon. Colour encodes arrival time and blob size encodes photon count.
- Direction comes from photon arrival times; energy comes from the number of photons.

### 5.2 Backgrounds (FACT [SB])
- Atmospheric muons arrive at about **3 kHz**. Selecting up-going tracks cuts that to the **µHz** level, because the Earth acts as a filter.
- Atmospheric neutrinos: about **100,000 per year** above about 0.1 TeV, with a spectrum ~E^-3.7. The astrophysical flux goes as ~E^-2.5 and rises above the atmospheric one above a few tens of TeV. About **100 astrophysical neutrinos per year** are expected. A "prompt" charm component would have a flatter spectrum.
- Starting-event veto: the outer layer of the array serves as a veto shield around an inner volume of about **500 Mt**.

### 5.3 Discovery (FACT)
- 2013: two PeV cascades nicknamed **Bert (1.04 PeV)** and **Ernie (1.14 PeV)** were found by accident while searching for EeV GZK neutrinos in data from May 2010 to May 2012 [SB, PRL2013]. (The nicknames come from IceCube outreach, **not from [SB]**; flag them for Tess.)
- Science 2013: **28 events** (30 TeV–1.14 PeV), **21 cascades and 7 tracks** [SB, S2013]. Significance was about 4σ in that paper (**not stated in [SB]; Tess should verify in S2013 before using it**).
- PRL 2014: three years of data (2010–2013) reject a purely atmospheric origin at **5.7σ** [SB]. This is the discovery-grade result.

### 5.4 The spectrum today (FACT [SB, SPEC26])
- Combined fit using **231,486 tracks** (8.5 years live time, mostly the Northern sky) and **10,569 cascades** (10.5 years, the whole sky), May 2010 to May 2021.
- Above about 30 TeV the spectrum is well described by a power law. Below about 30 TeV it flattens. A single power law over 5 TeV–10 PeV is rejected at **>4σ**, so the best fit is a broken power law.
- **The arrival directions show no significant anisotropy**, which fits mostly extragalactic sources.
- Highest-energy event published by IceCube: **11.4 (+2.46/−2.53) PeV**, a down-going muon neutrino recorded on **31 March 2019** and published in March 2026.
- The neutrino energy flux is comparable to the gamma-ray flux at lower energies and the cosmic-ray flux at higher energies. That suggests the same sources make all three (SPEC as a conclusion; [SB] says "suggests").
- Figure spec: plot E²Φ against E, a broken power law with its 68% band, and the much smaller Galactic and NGC 1068 contributions drawn underneath. Draw the shape **schematically**. Don't invent axis values; if numbers appear, take them from [SPEC26] Fig. 6.

### 5.5 Sources (the committee's caveat: no definite point source)
- **TXS 0506+056 (blazar)**: on 22 Sep 2017, IceCube-170922A, a muon neutrino of about **290 TeV** (180 TeV deposited), arrived within **0.06°** of the blazar, which was flaring (gamma-ray flux up about 7×). The worldwide alert went out **within a minute**. The archive shows a neutrino flare from Sep 2014 to Mar 2015 at **3.5σ**. [SB, TXS-MM, TXS-ARCH] The coincidence with the flare was about 3σ in TXS-MM (**not in [SB]; verify**).
- **NGC 1068 (M77)**, a Seyfert galaxy: a search of 110 gamma-ray source positions found **79 neutrinos at 1–10 TeV**, **4.2σ**. It lies 46 million ly away in Cetus and is radio-quiet with no large jet. Its black hole is about 15 million solar masses and heavily obscured. Fermi's 0.1–30 GeV flux is ≪ the neutrino flux, and MAGIC saw no TeV emission. Together that favours production in the **corona**, where gamma rays get absorbed. [SB, NGC]
- **Galactic plane**: **4.5σ** in 2023 [GAL23], consistent with the Fermi π^0 diffuse emission. **5.7σ** with 12 years of data in 2026 [GAL26], which makes the Milky Way the first neutrino source above 5σ. **No point sources found.** It contributes only a small fraction of the total flux. [SB]
- **GRBs**: more than 1000 follow-up searches found **no** coincident neutrinos. [SB]
- Committee wording: "Time will tell if these observations confirm AGNs as sources." Present TXS and NGC 1068 as **evidence, not discovery** (both are below 5σ).

### 5.6 Tau neutrinos (FACT [SB, TAU])
Seven tau neutrinos between 20 TeV and 1 PeV were reported in 2024. Atmospheric oscillation only produces tau neutrinos below about 100 GeV, so these must be astrophysical. A zero astrophysical tau flux is excluded at **5σ**. This confirms that the flux has been mixed by oscillation.

## 6. Implications and the future
- FACT [SB]: next-generation telescopes larger than a km³ are IceCube-Gen2 (South Pole), KM3NeT (Mediterranean, off Toulon and Sicily), P-ONE (off Vancouver Island), TRIDENT (South China Sea), and Baikal-GVD.
- FACT [SB]: realtime alerts, as with TXS, go out within a minute and drive multi-wavelength follow-up. Gravitational waves are named as a possible future messenger.
- Gen2 details (target volume, roughly ~8 km³ optical plus a radio array, and the timeline) are **not in [SB]**. If Sommer wants them, source them from the Gen2 TDR (J. Phys. G 48 (2021) 060501). **I have not verified these numbers here; don't use them unless cited.**
- Particle physics at extreme energies (SPEC/application): measuring the neutrino–nucleon cross-section at center-of-mass energies beyond the LHC through Earth absorption, tests of the flavour ratio and of new physics, and the prompt charm component. IceCube has published an absorption-based cross-section measurement (Nature 551 (2017) 596); this was **not verified in this pass, so verify before citing**.
- KM3NeT reported an even higher-energy event in Nature 638 (2025) 376 ([SB] cites it only as the KM3NeT reference). I have not verified its energy, about 220 PeV, in this pass, so mark it to verify.

## 7. Fact vs speculation, for the explainer's sidebar
**Established:** there is a diffuse astrophysical flux, at 5.7σ in 2014, now far beyond that. It extends past 10 PeV. It is mostly extragalactic and isotropic. The Galactic plane contributes at 5.7σ. An astrophysical tau component is seen at 5σ. The spectrum is not a single power law (>4σ).
**Evidence but not discovery:** the blazar TXS 0506+056 (3–3.5σ) and NGC 1068 (4.2σ).
**Open:** which source populations make most of the flux, whether production happens in AGN cores or jets, whether pp or pγ dominates, whether GRBs contribute (no sign so far), the prompt charm flux, and the link to UHECRs.

## 8. Uncertainties and flags for Tess
1. RESOLVED: the prefactor 4/(3K_π) matches [SB] p. 4 (Tess checked it), and the neutrino side counts all flavours.
2. Bert and Ernie are IceCube outreach nicknames (2010–12 data, published 2013), not from [SB]. The ~4σ for Science 2013 and the ~3σ for the TXS coincidence come from the papers or outreach, not from [SB].
3. RESOLVED: [GAL26] arXiv:2607.25966 is a preprint with no journal version as of 7 Oct 2026.
4. Gen2 specs, the KM3NeT event energy, and the cross-section measurement are unverified. Use them only with citations.
5. θ_C ≈ 40°, the 5,160 DOMs, and the ~18,000 km mean free path are my arithmetic from [SB] inputs.
