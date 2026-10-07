# Nobel Physics 2026 explainer: narrative + figure specs (Sommer → Frank)

Source of every number: `/workspace/nobel2026/research.md` (Rex). Citation keys in [brackets] match Rex's §0. Tags shown to the reader: a small pill **Established**, **Evidence**, or **Open** on claims where it matters, and "≈ (our estimate)" on DERIVED numbers. Frank: don't add numbers that aren't here.

## Global layout
- Dark mode. Horizontal tab bar, 8 tabs, each tab fits about 1–2 screens. No long scroll.
- Persistent header: "The 2026 Nobel Prize in Physics: IceCube and the high-energy neutrino sky". Subline: "Francis Halzen, sole laureate, 6 Oct 2026".
- Each tab opens with a one-sentence **Takeaway** box, then prose, then its figure(s).
- Jargon: first use of each term is bold with a one-line definition right there (and a hover tooltip if you like). The definitions are written inline below.
- Footer on every tab: "Sources" link that jumps to tab 8.

---

## Tab 1. The prize
**Takeaway:** Halzen won for turning a cubic kilometre of Antarctic ice into a telescope and using it to prove that the universe sends us neutrinos with a billion times the energy of anything from the Sun.

The Royal Swedish Academy of Sciences awarded the whole prize to Francis Halzen (University of Wisconsin–Madison) "for decisive contributions to the IceCube Neutrino Observatory and the discovery of high-energy neutrinos of astrophysical origin" [PR]. Halzen, born 1944 in Tienen, Belgium (PhD KU Leuven 1969), co-wrote the first proposal to use ice as both target and light medium (with J. Learned, June 1988), drove the AMANDA prototype, and led IceCube as principal investigator from its 1999 NSF proposal [SB]. IceCube itself is about 450 people at 58 institutions in 14 countries [SB].

The committee was careful about what has *not* been found: no single point source is established. A small fraction of the flux comes from our own Milky Way; most comes from extragalactic sources nobody has yet pinned down [SB].

**Fig 1, Neutrino Nobel timeline** (horizontal SVG): 1930 Pauli postulates ν · 1956 Cowan & Reines detect reactor ν (Nobel 1995) · 1988 Nobel for the muon neutrino (Lederman, Schwartz, Steinberger) · 2002 Davis & Koshiba, solar ν and SN 1987A · 2015 Kajita & McDonald, oscillations, ν have mass · 2026 Halzen, PeV astrophysical ν. Put an energy scale under it: MeV (Sun, supernova) → PeV (IceCube), labelled "×10⁹". Highlight 2026 in the accent colour.

---

## Tab 2. Neutrinos 101
**Takeaway:** neutrinos are almost interaction-free, which makes them perfect messengers and terrible to catch.

A **neutrino** is an electrically neutral elementary particle with sub-eV mass. It feels only the **weak interaction** (the force behind radioactive beta decay, carried by the heavy W and Z bosons) and gravity. There are three **flavours**, νₑ, ν_μ, ν_τ, named for the charged lepton (electron, muon, tau) each one produces when it interacts. Each flavour is a quantum superposition of three mass states, so a neutrino changes flavour as it travels: **oscillation** [SB].

*Why that makes a great messenger.* Astronomy has three other carriers from the high-energy sky, and each has a flaw [SB]:
- **Charged cosmic rays** get bent by magnetic fields, so they no longer point back to where they came from.
- **Gamma rays** get absorbed in dense sources and, over cosmic distances, by background light (the CMB and the extragalactic background light). They can also be made by electrons, so seeing gamma rays doesn't prove protons are being accelerated.
- Neutrinos are neutral and almost never absorbed, so they point straight back and escape from the densest places. A neutrino detection means hadrons (protons, nuclei) were accelerated.

*Why it's hard to catch.* At 1 PeV (10¹⁵ eV) the neutrino–nucleon **cross-section** (effective target area per nucleon) is about σ ~ 10⁻³³ cm² [SB]. With ice's nucleon density n ≈ 5.5×10²³ cm⁻³, the mean free path is

$$\lambda = \frac{1}{n\sigma} \approx 1.8\times10^{9}\ \text{cm} \approx 18{,}000\ \text{km}\quad(\text{our estimate})$$

That's longer than Earth's diameter, so a PeV neutrino crossing 1 km of ice has roughly a 1-in-18,000 chance of interacting. Add a flux that falls steeply with energy (∝ E^-2.5) and a source rate of order 100 events a year needs a **cubic kilometre** of detector [SB].

**Fig 2, Messenger comparison** (SVG): a source on the left, Earth on the right. Three paths: a cosmic ray (wiggly, deflected by drawn field lines, misses the direction), a gamma ray (stopped by a fog of CMB/background photons, marked ✕), a neutrino (straight line through everything). Label each with its flaw in one line.

---

## Tab 3. Cosmic accelerators
**Takeaway:** neutrinos are the by-product that proves a source accelerates protons, and their energy ties them to gamma rays and cosmic rays.

**Cosmic rays** (found by Hess in 1912) are mostly protons and helium nuclei, reaching about 10²⁰ eV, versus 7 TeV per beam at the LHC [SB]. Their energy spectrum is a broken power law: a **knee** at a few PeV (below it, Galactic sources, probably supernova remnants), an **ankle** at a few EeV (above it, extragalactic; about one particle per km² per year), and the **GZK cutoff** above ~50 EeV, where cosmic rays lose energy on CMB photons [SB]. Particles gain energy by bouncing across shock fronts (**first-order Fermi acceleration**), and the **Hillas criterion** says a source must be big and magnetised enough to hold a particle until it gets that energy.

When those protons hit gas (pp) or photons (pγ), they make pions [SB]:

$$p + p \to \pi^0,\pi^\pm + X \qquad p + \gamma \to \Delta^+(1232) \to p\,\pi^0 \ \text{or}\ n\,\pi^+$$
$$\pi^0\to\gamma\gamma \qquad \pi^+\to\mu^+\nu_\mu,\quad \mu^+\to e^+\nu_e\bar\nu_\mu$$

So every hadronic accelerator makes gamma rays and neutrinos together. Their energy fluxes are linked [SB, HK]:

$$E_\gamma^2\frac{dN_\gamma}{dE_\gamma}\approx\frac{4}{3K_\pi}\,E_\nu^2\frac{dN_\nu}{dE_\nu}\Big|_{E_\nu=E_\gamma/2},\qquad K_\pi\approx2\ (pp),\ \approx1\ (p\gamma)$$

(Rex flagged this prefactor as reconstructed from garbled text. Tess verifies before ship.)

Rule of thumb: a neutrino carries about 1/20 of the parent proton's energy, so PeV–EeV protons give tens-of-TeV to tens-of-PeV neutrinos, exactly IceCube's range [SB]. Pion decay produces flavours in the ratio νₑ:ν_μ:ν_τ ≈ 1:2:0; oscillation over cosmic distances evens that to about 1:1:1 by the time they reach Earth (standard physics; not in [SB]).

**Fig 3, Source mechanism** (SVG, the centrepiece): a proton enters from the left and hits a target photon or proton; branches to π⁰ → two γ arrows (labelled "gamma rays, ~E/10") and π⁺ → μ⁺ + ν_μ, μ⁺ → e⁺ + νₑ + ν̄_μ (neutrinos labelled "~E/20"). A small inset: flavour pie 1:2:0 at source → 1:1:1 at Earth.
**Fig 3b, Cosmic-ray spectrum** (small SVG, schematic, log-log): falling line with labelled knee, ankle, GZK cutoff and a marker "LHC beam 7 TeV". No other axis values.

---

## Tab 4. The detector
**Takeaway:** IceCube is 5,160 light sensors frozen into a cubic kilometre of the clearest ice on Earth, 1.5–2.5 km under the South Pole.

Seawater detectors had trouble: DUMAND off Hawaii deployed one string in 1993, it failed, and the project was cancelled in 1995 (bioluminescence and radioactive ⁴⁰K were background problems) [SB]. Halzen's bet was ice. Sensors in Greenland boreholes in 1991 showed it was transparent enough; the AMANDA prototype (1993–2000) found that air bubbles at 800–1000 m ruin the light (scattering length under 50 cm), so IceCube went deeper, where the absorption length is ~200 m and the scattering length ~50 m [SB].

The build: proposed 1999, funded March 2002, strings deployed 2005–2010, complete in 2011, over 99% uptime since [SB]. Holes are melted with hot water.

The geometry [SB]: 86 vertical **strings**, each holding 60 **DOMs** (digital optical modules: a pressure sphere with a downward-facing 25.4 cm photomultiplier tube that digitises its own signals). DOMs sit every 17 m between 1450 and 2450 m depth; strings sit on a hexagonal grid 125 m apart. That's 5,160 DOMs (our count; [SB] says "over 5000") watching about 1 km³, roughly 1 gigatonne of ice. **IceTop**, on the surface, catches air showers (300 TeV–1 EeV) and helps veto them.

**Cherenkov light** is how IceCube sees. A charged particle moving faster than light does *in the medium* (v > c/n) emits a cone of mostly UV light, like a sonic boom. With n ≈ 1.31 for ice:

$$\cos\theta_C=\frac{1}{n\beta}\ \Rightarrow\ \theta_C\approx40^\circ\ (\beta\to1;\ \text{our estimate})$$

**Fig 4, Detector geometry** (SVG, cutaway side view, to scale vertically): ice surface with IceTop tanks and a lab building; a 1 km instrumented band from 1450 to 2450 m with ~10 representative strings and dots for DOMs; the bubble zone 800–1000 m shaded and labelled "too bubbly (AMANDA lesson)". Scale reference: Eiffel Tower (330 m) silhouette next to the band. Top-down inset: hexagonal grid, 125 m spacing. **No dust-layer band** (unsourced).
**Fig 4b, Cherenkov cone** (small SVG): a particle track with the 40° cone and wavefront.

---

## Tab 5. Reading an event
**Takeaway:** a muon track gives you direction; a cascade gives you energy. Picking which events to trust is the whole game.

A neutrino interacts by **deep inelastic scattering** (it smashes into a quark inside a nucleon) [SB]. In a **charged-current** interaction (W exchange) it turns into its charged lepton plus a spray of hadrons; in a **neutral-current** one (Z exchange) it just leaves the hadron spray. Two shapes come out [SB]:

| | Track | Cascade |
|---|---|---|
| Made by | CC ν_μ (a muon) | CC νₑ, ν_τ and NC of all flavours |
| Looks like | a line crossing the array (km long at TeV) | a near-spherical blob (shower < 10 m) |
| Direction | **0.3°** at 100 TeV | **~5°** above 50 TeV |
| Energy | within a factor ~2 | **~8%** at 100 TeV |

A ν_τ can make a **double bang**: one cascade where it interacts, a second where the tau decays, about 50 m apart per PeV [SB].

*Backgrounds* [SB]. Cosmic-ray air showers send down **atmospheric muons** at about 3 kHz. Two tricks remove them: look only at **up-going** tracks (the Earth stops muons, cutting the rate to µHz), or use the outer layer of sensors as a **veto** and keep only events that start inside a ~500 Mt inner volume. Then come about 100,000 **atmospheric neutrinos** a year, with a steep spectrum ∝ E^-3.7, against an astrophysical spectrum ∝ E^-2.5 that wins above a few tens of TeV and gives about 100 events a year.

**Fig 5, Track vs cascade** (two side-by-side event displays, SVG): grid of DOM dots; lit DOMs drawn as circles sized by photon count and coloured by arrival time (red early → blue late, with a legend). Left: a straight track; right: a spherical cascade. Captions from [SB] Fig. 4: "track depositing 2.6 PeV, from 11° below horizon" and "cascade depositing 1.14 PeV". Optional third mini panel: double bang.
**Fig 5b, Veto concept** (small): array outline, outer shell shaded "veto", an incoming muon tagged in the shell, a starting event inside.

---

## Tab 6. The discovery
**Takeaway:** two accidental PeV events in 2010–12 data (published 2013) opened the door; by 2014 the astrophysical signal was 5.7σ, and it now spans 5 TeV to beyond 10 PeV.

While searching May 2010–May 2012 data for much higher-energy (EeV) neutrinos, IceCube found two cascades at about 1.04 and 1.14 PeV, nicknamed Bert and Ernie [SB, PRL2013; nicknames from outreach]. A dedicated search with the veto gave 28 events from 30 TeV to 1.14 PeV, 21 cascades and 7 tracks [S2013]. Three years of data then excluded a purely atmospheric origin at **5.7σ** (σ = standard deviations; 5σ is physics' discovery bar) [PRL2014]. ***Established.***

The picture today [SB, SPEC26]: a combined fit of 231,486 tracks and 10,569 cascades (May 2010–May 2021). Above ~30 TeV it's a power law, below it flattens, and a single power law from 5 TeV to 10 PeV is rejected at >4σ. The directions are isotropic, as expected if most sources are far outside the Galaxy. The highest-energy IceCube event is **11.4 PeV** (31 March 2019, published 2026). The neutrino energy flux is comparable to the gamma-ray and cosmic-ray fluxes, which *suggests* common sources ***Open***. Seven tau neutrinos (20 TeV–1 PeV) exclude a zero astrophysical tau flux at 5σ, confirming the flux has oscillated across cosmic distances [TAU] ***Established***.

**Fig 6, Energy spectrum** (SVG, schematic, log-log, E²Φ vs E): falling atmospheric curve (steep), astrophysical broken power law with a shaded 68% band crossing above it at "few tens of TeV", and two much smaller curves underneath labelled "Milky Way" and "NGC 1068". Mark points at 1.04/1.14 PeV ("2010–12 data, published 2013") and 11.4 PeV ("highest"). Axis tick labels only on E (1 TeV, 10 TeV, 100 TeV, 1 PeV, 10 PeV); no invented flux values.
**Fig 6b, Discovery timeline strip**: 2013 two PeV events published (2010–12 data) → 2013 28 events → 2014 5.7σ → 2024 tau 5σ → 2026 11.4 PeV + spectrum.

---

## Tab 7. Where they come from
**Takeaway:** the Milky Way is a confirmed but small source; two active galaxies are strong evidence; most of the flux is still unexplained.

**Interactive Fig 7, Sky map** (canvas, Mollweide-style schematic, Galactic coordinates): faint band for the Galactic plane; markers for TXS 0506+056 and NGC 1068; scatter of faint isotropic dots labelled "illustrative, not real event positions". Clicking a marker or the band opens its card below. A toggle "show significance" colours markers by σ against a 5σ line.

Cards:
- **The Milky Way** ***Established***: 4.5σ in 2023 [GAL23], 5.7σ with 12 years in 2026 [GAL26, preprint], matching the gamma-ray glow cosmic rays make on interstellar gas. First neutrino source above 5σ, but diffuse: no point sources, and a small fraction of the total [SB].
- **TXS 0506+056, a blazar** (an active galaxy whose jet points at us) ***Evidence***: on 22 Sep 2017 a ~290 TeV neutrino (IceCube-170922A) landed within 0.06° of it while it was flaring in gamma rays (~7× brighter). The alert went out within a minute and telescopes worldwide followed up. The archive then showed a neutrino flare in Sep 2014–Mar 2015 at 3.5σ [SB, TXS-MM, TXS-ARCH].
- **NGC 1068, a Seyfert galaxy** (an active galaxy with a buried, jetless black hole of ~15 million solar masses, 46 million light-years away) ***Evidence***: 79 neutrinos at 1–10 TeV, 4.2σ. Gamma rays are far weaker than neutrinos here, so the neutrinos likely come from the hot **corona** near the black hole, where gamma rays get absorbed [SB, NGC].
- **Gamma-ray bursts** ***Ruled out as dominant***: more than 1000 searches, no coincident neutrinos [SB].

Committee wording to quote: "Time will tell if these observations confirm AGNs as sources."

**Fig 7b, Significance bar chart**: horizontal bars, diffuse flux 5.7σ (2014), Milky Way 5.7σ, tau 5σ, NGC 1068 4.2σ, TXS archival 3.5σ; vertical dashed line at 5σ labelled "discovery threshold".

---

## Tab 8. What it means, what's next, sources
**Takeaway:** a new kind of astronomy exists; the next decade is about finding its sources and using it as a particle collider nature runs for free.

*Established vs open* (two-column panel, straight from Rex §7):
- Established: a diffuse astrophysical flux; extends past 10 PeV; mostly extragalactic and isotropic; Galactic contribution at 5.7σ; astrophysical tau at 5σ; spectrum not a single power law.
- Evidence: TXS 0506+056, NGC 1068.
- Open: which populations dominate; AGN core vs jet; pp vs pγ; GRB contribution (none seen); prompt charm flux; link to ultra-high-energy cosmic rays.

*What's next* [SB]: bigger-than-km³ telescopes: IceCube-Gen2 (South Pole), KM3NeT (Mediterranean), P-ONE (off Vancouver Island), TRIDENT (South China Sea), Baikal-GVD. Real-time alerts sent within a minute make IceCube a trigger for **multi-messenger astronomy** (observing one event with neutrinos, light and possibly gravitational waves). ***Open***: using Earth's absorption of high-energy neutrinos to measure cross-sections at collision energies beyond the LHC, testing flavour ratios for new physics. Gen2 size, the KM3NeT ~220 PeV event and IceCube's 2017 cross-section result stay **out** unless Tess confirms citations.

**Fig 8, Global map of neutrino telescopes** (simple SVG world outline): pins for the five sites, IceCube highlighted.

*Sources list*: all keys from Rex §0 with links, plus a note "Numbers marked ≈ (our estimate) are arithmetic from these sources."

---

## Notes for Frank and Tess
- Every figure is schematic unless it says otherwise; caption each "Schematic" where values aren't real.
- Pending verification (Rex §8): the 4/(3K_π) prefactor, Bert/Ernie nicknames, GAL26 is a preprint (no journal version as of 7 Oct). Don't show the ~4σ (Science 2013) or ~3σ (TXS coincidence) figures; I left them out.
- Fig 1: I used only years in the dossier.
