# Nobel Chemistry 2026 explainer: narrative + figure specs (Cleo → Ivy, Frank)

Source of every number: `/workspace/nobel2026-chemistry/research.md` (Rex). Citation keys in [brackets] match Rex's §0: [PR] press release, [SB] committee scientific background, [POP] popular background, plus paper keys (Kagan1986, Soai1995, Sato2003, etc.). Frank: don't add numbers that aren't here.

Reader-facing tags: a small pill **Established**, **Evidence** or **Open** on claims where it matters. Numbers I computed are marked "≈ (our estimate)". Two equations are **our illustrations** (not in [SB]) and must carry that label on the page: the Frank-type rate equations in Tab 3 and the √N estimate in Tab 6.

## Global layout
- Dark mode, horizontal tab bar, 8 tabs, each about 1–2 screens. Same chrome as the physics page.
- Persistent header: "The 2026 Nobel Prize in Chemistry: how chemistry learned to choose a mirror image". Subline: "Henri B. Kagan and Kenso Soai, shared equally, 7 Oct 2026".
- Each tab opens with a one-sentence **Takeaway** box, then prose, then figure(s).
- First use of each term: bold, with its one-line definition right there (tooltip optional). Definitions are written inline below.
- Footer on every tab: "Sources" link to Tab 8.
- Molecule drawings: skeletal style is fine, but every drawn structure must match the text below. Don't draw a specific 2-substituent on the 1995 compound (see Notes).

---

## Tab 1. The prize
**Takeaway:** Kagan showed that a catalyst's handedness can be amplified rather than diluted, and Soai built a molecule that copies its own handedness until one mirror form takes over, the first lab demonstration of a 1953 idea about how life became one-handed.

On 7 October 2026 the Royal Swedish Academy of Sciences split the prize equally between Henri B. Kagan (born 1930, Boulogne-Billancourt; Professor Emeritus, then Université Paris-Sud) and Kenso Soai (born 1950, Hiroshima; Professor Emeritus, Tokyo University of Science) "for the discovery of non-linear effects and autocatalysis in asymmetric organic synthesis" [PR]. Use that citation word for word.

Committee chair Heiner Linke: "Henri Kagan and Kenso Soai have provided a solution to a chemical mystery that is over a century old: how homochirality can emerge spontaneously. The chemical reactions they have developed are spectacular." [PR]

The one-paragraph version: many molecules come in left- and right-handed forms, and life uses only one of each. Ordinary chemistry from non-handed ingredients always gives a 50:50 mix. Kagan (1986) found that when a catalyst is built from two handed pieces, a slightly lopsided supply of those pieces can give a product far more lopsided than the supply. Soai (1995) found a reaction whose product is its own catalyst and does exactly that, so a 5% lean grows to 90% in a few rounds; by 2003 a lean of 0.00005% grew to more than 99.5% in three rounds [SB]. **Established.**

**Fig 1, Timeline** (horizontal SVG): 1953 Frank's theory · 1986 Kagan, non-linear effects · 1990 Soai, first asymmetric autocatalysis (purity erodes) · 1995 Soai, autocatalysis with amplification · 2002–03 Singleton and Soai, independently, handedness with no chiral input · 2015 X-ray structures of the zinc tetramers · 2020 two rival mechanisms (Denmark; Trapp) · 2026 Nobel. Above the line, two grey markers for related prizes: 2001 (asymmetric catalysis) and 2021 (asymmetric organocatalysis) [SB p. 3]. Highlight 1986, 1995 and 2026 in the accent colour.

---

## Tab 2. Chemistry backgrounder
**Takeaway:** a chiral molecule is one that can't be overlaid on its mirror image, and chemists measure how lopsided a mixture of the two mirror forms is with one number, the enantiomeric excess.

A molecule is **chiral** when it can't be superimposed on its mirror image, the way a left hand can't be laid exactly over a right hand [SB fn 4]. The commonest cause is a **stereocentre**: a carbon carrying four different groups. The two mirror forms are **enantiomers**. In a non-chiral setting they have identical melting points, energies and reaction rates; they differ only when they meet something else that is chiral, such as an enzyme, a receptor, polarised light or another chiral molecule. **Established.**

Labels, briefly. **R/S** names the 3D arrangement at a stereocentre by a fixed priority rule [SB fn 16]. **D/L** is the older convention still used for sugars and amino acids. Life builds proteins from **L-amino acids** (glycine, the simplest, isn't chiral) and nucleic acids from **D-sugars** [SB p. 2]. A separate label, **(+)/(–)**, records which way a sample rotates polarised light, and that sign is *not* fixed by the D/L or R/S label: L-alanine, for instance, rotates light to the right in acid. So we describe life's handedness by configuration, never as "left-turning".

A **racemate** is an exact 50:50 mixture of enantiomers; any other mixture is **scalemic** [SB fn 34]; **homochiral** means every molecule has the same handedness [SB fn 2]. The purity measure is the **enantiomeric excess**:

$$ee = \frac{|R - S|}{R + S}\times 100\%,\qquad \text{fraction of the major form} = \frac{1 + ee}{2}$$

So 90% ee is a 95:5 mixture and 50% ee is 75:25 (our arithmetic) [SB fn 1].

**Diastereomers** are stereoisomers that are *not* mirror images, for example a pair built R+R versus R+S. Unlike enantiomers, diastereomers have different energies, stabilities and reactivities. This one fact is the engine of the whole prize. **Established.**

**Catalysis** speeds a reaction without the catalyst being used up. **Asymmetric catalysis** uses a chiral catalyst, typically a metal M bound to a chiral **ligand** L* (an organic molecule that binds the metal), to make one enantiomer faster than the other [SB p. 3]. **Autocatalysis** is when a product catalyses its own formation, so the reaction speeds up as it goes [SB].

How a chiral product comes from non-chiral ingredients: the reactions in this story add a zinc–carbon group across an **aldehyde** (a C=O group at the end of a molecule). The C=O carbon is flat, so the incoming group can attack from the top face or the bottom face. One face gives one enantiomer of the alcohol product, the other face its mirror image. With nothing chiral nearby the two faces are hit equally and you get a racemate; a chiral catalyst works by shielding one face [SB p. 2]. **Established.**

Why chemists care: in drugs, often only one enantiomer has the wanted effect [PR; POP p. 1].

**Fig 2a, Hands and mirror** (SVG): left, a generic stereocentre (C with four coloured balls) and its mirror image across a dashed mirror line, labelled "enantiomers: same atoms, same bonds, not superimposable". Right, L-alanine and D-alanine as wedge/dash structures, labelled "L-alanine (in proteins)" and "D-alanine". Schematic.
**Fig 2b, The ee scale** (SVG number line): from 0% ee (50:50) to 100% ee (100:0), ticks at 0, 50, 90, 99.5 with the ratio under each: 50:50, 75:25, 95:5, 99.75:0.25. Real definitions, not data.
**Fig 2c, Two faces of an aldehyde** (SVG): a flat C=O drawn in perspective (aryl group, H, O around the carbon), an R–Zn reagent approaching from above and another from below, each arrow leading to one mirror-image alcohol. Label "top face → one enantiomer", "bottom face → its mirror image". Don't assign R or S to a face. Schematic.

---

## Tab 3. The puzzle: why is life one-handed?
**Takeaway:** in 1953 the physicist Charles Frank showed on paper that a molecule which copies itself and sabotages its mirror image will turn a tiny random imbalance into total dominance; nobody could build one for forty years.

Abiotic chemistry without any chiral influence "invariably" gives racemates [SB p. 2], yet biology is homochiral. Something had to create an initial imbalance and something had to amplify it. **Open** for the actual history of life.

F. Charles Frank, a theoretical physicist at Bristol, proposed "a chemical substance which is a catalyst for its own production and an anti-catalyst for the production of its optical antimer" [Frank1953; SB p. 3]. Three ingredients:
1. **Autocatalysis**: the product makes more of itself.
2. **Enantioselective catalysis**: it makes its own handedness preferentially.
3. **Mutual antagonism**: the two mirror forms suppress each other.

He ended: "A laboratory demonstration may not be impossible." Before Kagan and Soai, (1) and (2) were each known, but (3), and (1) and (2) together, had never been shown [SB p. 3].

*Why all three are needed* (our illustration, a minimal Frank-type model; not Frank's notation and not in [SB]). Feed an achiral starting material A; let each enantiomer copy itself perfectly with rate constant k, and let R and S remove each other with rate constant μ:

$$\dot R = kAR - \mu RS,\qquad \dot S = kAS - \mu RS$$

Rewriting for the enantiomeric excess (our derivation):

$$\frac{d\,ee}{dt} = \frac{\mu}{2}\,(R+S)\;ee\,(1 - ee^2)$$

Read it like a physicist: the copying term k drops out entirely. Perfect self-copying alone only *preserves* the ee, and imperfect copying erodes it: a catalyst giving 90% ee makes 90%, then 81%, and so on [SB p. 10]. Amplification comes only from the antagonism term μ. Then ee = 0 is an unstable fixed point and ee = ±1 are the stable ones, so any seed, however small, runs to one hand or the other. That is the symmetry breaking Soai later saw (Tab 6).

Caveat in the committee's words: the Frank model "is not an answer to the origin of biological homochirality"; it is one possible route among several for an event 3.5–4 billion years ago [SB p. 4]. **Open.**

**Fig 3a, Frank's loop** (SVG): R and S as two nodes. Each has a self-arrow labelled "makes more of itself (autocatalysis, selective)". A blunt-ended inhibition arrow runs both ways between them, labelled "mutual antagonism". Achiral A feeds both. Schematic.
**Fig 3b, ee phase line** (small SVG, our model): horizontal axis ee from −1 to +1; open circle at 0 labelled "unstable", filled circles at ±1 labelled "stable", flow arrows pointing away from 0 toward ±1. Caption: "Illustrative model, not data."

---

## Tab 4. Kagan 1986: when purity stops adding up
**Takeaway:** if the active catalyst carries two chiral ligands, the mismatched left–right pairs behave differently from the matched pairs, so product purity can be far above (or below) what the ligand's purity predicts.

Before 1986 chemists assumed product purity scaled linearly with catalyst purity [SB p. 5, Eq. 1]:

$$ee_{prod} = ee_{max}\times ee_{ligand}$$

where \(ee_{max}\) is the product ee from enantiopure ligand. That holds when the catalyst carries one chiral ligand (ML*). Kagan's group (Puchot, Samuel, Duñach, Zhao, Agami, Kagan) asked what happens when it carries two (ML*₂) [Kagan1986; SB p. 6]. Mix R and S ligands and three catalysts form: the matched pairs M(L_R)(L_R) and M(L_S)(L_S), which are mirror images and cancel each other out, and the mismatched **heterochiral** pair M(L_R)(L_S). The mismatched pair is a diastereomer of the matched ones; it contains one ligand of each hand (meso-like), and in Kagan's model whatever it makes is racemic.
- If the mismatched pair is **less** reactive, the leftover matched catalyst is purer than the ligand pool: a **positive non-linear effect (+NLE)**, or **asymmetric amplification**.
- If it is **more** reactive, it floods the product with racemate: a **negative non-linear effect (–NLE)**. **Established.**

Kagan's model [SB Eqs. 2–3]:

$$ee_{prod} = ee_{max}\cdot ee_{ligand}\cdot f,\qquad f = \frac{1+\beta}{1+g\beta}$$

Here β is the ratio of heterochiral to homochiral catalyst and g is the reactivity of the heterochiral catalyst relative to the homochiral one. g = 1 gives the straight line, g < 1 bends it up (+NLE), g > 1 bends it down (–NLE) (our reading of Eq. 3). If ligands pair at random, β depends only on the ligand ee (our derivation, consistent with [POP] Fig. 4):

$$\beta = \frac{1 - ee_{ligand}^2}{1 + ee_{ligand}^2}$$

*Worked example* [POP Fig. 4; arithmetic checked by Rex]: ligand 75:25 (50% ee). Random pairs: R·R 56.25%, R·S 37.5%, S·S 6.25%. If R·S barely works (g ≈ 0), the working catalyst is 56.25 : 6.25 = 90 : 10, so 80% ee from a 50% ee ligand. In Kagan's terms β = 0.6 and f = 1.6.

A limiting case the authors noted: if the inert mismatched complex forms irreversibly, product ee equals \(ee_{max}\) whatever the ligand ee [SB p. 7]. In the ML*₂ picture product ee can't exceed \(ee_{max}\) [SB p. 8].

*The 1986 experiments* [SB p. 6]: a titanium/tartrate sulfide oxidation gave –NLE; the Sharpless epoxidation of geraniol gave +NLE.

*Showcase numbers* [SB]:
- Noyori's DAIB ligand in diethylzinc addition to benzaldehyde: 15% ee ligand gives 98% ee product. Here the mismatched zinc dimer is the most stable species and locks away the minor enantiomer, while monomers do the catalysis, a **reservoir effect**.
- Merck, leukotriene antagonist L-699,392: α-pinene of 70% optical purity gave a reduction product of 95% ee.
- Jacobsen's chromium–salen epoxide opening: the NLE showed that two metal centres act together in the selectivity-setting step, which helped establish cooperative catalysis.

Later extensions [SB]: ML*₃ and ML*₄ models; a **hyperpositive NLE**, where product ee exceeds \(ee_{max}\), seen so far in one system only (dimethylzinc plus benzaldehyde with N-benzylephedrine: 53% ee product at 5% ee ligand, falling to 16% at 100% ee ligand, because a mismatched dimer precipitates); and Blackmond's demonstration that phase behaviour alone can do it: proline's racemate crystallises out, leaving a solution near 50% ee, so a +NLE appears below 50% ligand ee and a –NLE above.

**Fig 4a, The Kagan plot** (SVG line chart, the one honest computed figure): x = ligand ee 0–100%, y = \(ee_{prod}/ee_{max}\) 0–100%. Compute from \(y = x\,(1+\beta)/(1+g\beta)\) with \(\beta = (1-x^2)/(1+x^2)\), x as a fraction. Curves for g = 0, 0.25, 1, 4; label g = 1 "linear (pre-1986 expectation)", g < 1 "+NLE, amplification", g > 1 "–NLE". Mark the worked example point (50%, 80%) on the g = 0 curve. Check values: g = 0 at x = 0.5 gives 0.80, at x = 0.25 gives 0.47; g = 0.25 at x = 0.5 gives 0.70; g = 4 at x = 0.5 gives 0.235. Caption: "Model curves from Kagan's Eqs. 2–3 assuming random ligand pairing; parameters illustrative, not fitted to data."
**Fig 4b, Pairing diagram** (SVG): a 75:25 pool of R (accent) and S (contrast) ligand tokens → three catalyst types in a 56.25 / 37.5 / 6.25 split, with the R·S pair greyed and labelled "barely active" → working catalyst 90:10 → product 80% ee. Numbers from [POP] Fig. 4. Schematic.

---

## Tab 5. Soai: a molecule that copies its own handedness
**Takeaway:** Soai found a reaction whose chiral product is the catalyst for making more of itself and also obeys Kagan's amplification, so each round makes the product purer: 5% ee became 90%, and later 0.00005% became more than 99.5%.

Autocatalysis alone isn't enough. Each round of imperfect copying erodes purity (90%, then 81% …); to amplify, the catalyst must also act as Frank's "anti-catalyst" for its mirror image, which in Kagan's language means a +NLE [SB p. 10].

*1990, autocatalysis but erosion* [Soai1990; SB]: diisopropylzinc (i-Pr₂Zn) added to pyridine-3-carbaldehyde, catalysed by the zinc salt of the product alcohol itself. Catalyst at 86% ee gave product at 35% ee, same handedness. Autocatalytic and selective, but purity fell. Two of Frank's three criteria.

*1995, amplification* [Soai1995; SB Fig. 7]: switch to pyrimidine-5-carbaldehyde (a six-membered ring with two nitrogens). The product, a pyrimidyl alcohol, now amplifies. Starting from 5% ee: run 1 gave 55%, run 2 gave 87%, and runs 3–5 held at a 90% plateau. All three of Frank's criteria in one flask. This is now called the **Soai reaction**. **Established.**

*2003, from almost nothing* [Sato2003; SB]: with a 2-alkynyl pyrimidine (a tert-butyl-capped carbon–carbon triple bond on the ring), a seed of 0.00005% ee reached >99.5% ee in three consecutive runs. [POP] Fig. 6 gives the steps as 0.00005% → 57% → 99% → >99.5%. The committee calls this "an amplification of the stereoisomeric ratio by a factor of 630,000" [SB]. >99.5% ee means more than 99.75 : 0.25 (our arithmetic). **Established.**

The mental picture: each run, the zinc alkoxide product sits in the flask as catalyst. Matched clusters of the major hand work; mismatched clusters soak up the minor hand and don't. The new product inherits the majority's handedness, purer than before, and becomes next round's catalyst.

Limits [SB p. 13–14]: it is the only known asymmetric autocatalysis that both amplifies and works with no chiral input, its substrate scope is narrow (pyrimidyl and closely related aldehydes), and it runs in dry organic solvent with organozinc reagents, so it is "not relevant for the emergence of biological homochirality in aqueous systems".

**Fig 5a, The Soai reaction scheme** (SVG): aldehyde (pyrimidine ring with CHO at position 5; position 2 drawn as a generic "R") + i-Pr₂Zn → zinc alkoxide of the alcohol (new stereocentre starred) → after workup, the alcohol. A curved feedback arrow from product back over the reaction arrow, labelled "product is the catalyst". Optional curved-arrow inset: the Zn–C bond electrons move to the carbonyl carbon while the C=O π electrons move to oxygen, which binds zinc. Schematic.
**Fig 5b, Amplification by run** (SVG bar or dot chart, real data): two panels sharing a **log-scale** y-axis of ee from 10⁻⁷ to 1 (label ticks as 0.00001%, 0.001%, 0.1%, 10%, 100%). Panel 1995: seed 5%, run 1 55%, run 2 87%, then one bar "runs 3–5: 90% plateau". Panel 2003: seed 0.00005%, 57%, 99%, >99.5% (last bar with an up-arrow for ">"). Sources in caption: "1995 values [SB Fig. 7]; 2003 endpoints [SB], intermediate runs [POP Fig. 6]." No "Schematic" label; these are real values.

---

## Tab 6. Handedness from nothing
**Takeaway:** with no chiral input at all, the Soai reaction still ends up strongly one-handed, but which hand is a coin flip, exactly as Frank's model predicts for amplified random noise.

**Absolute asymmetric synthesis** means getting an enantiomerically enriched product with no chiral input whatever. Soai (alkyne-substituted aldehyde, R = t-BuC≡C) and Daniel Singleton (R = Me) showed it independently with the Soai reaction in 2002–03 [SB p. 13; Singleton2002; Soai2003TA]. Singleton is not a laureate; keep the credit wording neutral and use "independently", as [SB] does.

The idea: a "racemic" batch of zinc alkoxide is never exactly 50:50. Random counting fluctuation leaves a tiny excess of one hand, which Kurt Mislow called **cryptochirality** [SB]. The +NLE then amplifies it. In 37 runs, 18 gave the R product and 19 gave S, with ee between 15% and 91% [SB; Soai2003TA]. That split is what a fair coin gives (our check). **Established.**

*How small is the seed?* (our illustration, not in [SB]): in N molecules of a random 50:50 mixture the typical excess is about √N, so the typical ee is about 1/√N. For 1 mmol, N ≈ 6×10²⁰, which gives ee ≈ 4×10⁻¹¹, roughly ten thousand times smaller than the deliberate 0.00005% seed of 2003 and far below anything measurable.

Other things can set the hand instead of chance [SB p. 12]: circularly polarised light shone on racemic additives, chiral crystals, minerals and surfaces, and molecules made chiral only by isotope substitution (e.g. hydrogen vs deuterium). Each tips the coin before the amplifier runs.

**Fig 6a, Coin-flip outcome** (SVG, real data): two bars, R = 18 and S = 19, total 37, with a dashed line at 18.5 labelled "50:50 expectation", and a note "product ee per run 15–91%". Source [SB]. No individual-run points (we don't have them).
**Fig 6b, Noise to signal** (small SVG, schematic): a jittering line around 0 ee (labelled "random excess ≈ 1/√N", our estimate) feeding an amplifier box labelled "+NLE autocatalysis", out of which come two diverging arrows to "≈ all R" and "≈ all S". Caption "Schematic".

---

## Tab 7. How does it work? (still debated)
**Takeaway:** everyone agrees that clusters of zinc alkoxides do the work; two detailed mechanisms disagree about which cluster and why it amplifies.

The timeline [SB p. 14–16]:
- 1990, Soai: a zinc monoalkoxide catalyst.
- 2001, Blackmond and Brown: reaction calorimetry (measuring the heat released over time) fits a dimeric catalyst.
- 2003, Buono and Blackmond: kinetics fits a tetrameric transition state and predicts both rate and NLE.
- 2007, Klankermayer, Gridnev and Brown (DFT calculations, quantum-mechanical modelling of structures and energies): a **square–macrocycle–square (SMS)** tetramer.
- 2010, Quaranta, Brown and Blackmond: the reaction gets *slower* as temperature rises; the active catalyst derives from SMS.
- 2015, Matsumoto, Kawasaki and Soai: **X-ray structures** of homochiral and heterochiral tetramers. Two Zn₂O₂ squares (zinc–oxygen four-rings) are joined by ring-nitrogen-to-zinc bonds into a 12-membered macrocycle, leaving two zinc atoms with open sites that can grab an aldehyde. **Established** as structures; their catalytic role is the debate.

The two current models:
- **Denmark and Houk (2020):** the aldehyde docks "floor-to-floor" onto the two open zinc sites of the *homochiral* SMS tetramer; the heterochiral tetramer can't adopt that geometry. That is Kagan's mismatched-pair idea and Frank's antagonism, made molecular. **Evidence.**
- **Trapp (2020–25):** in-situ mass spectrometry points instead to a short-lived **zinc hemiacetal** (product and aldehyde bound together) as the real catalyst. Monomer and dimers exist, but the dimers act as a kinetic gate, not a trap; amplification is a **kinetically controlled non-equilibrium steady state**, which the committee calls "different from the mechanism put forward by Kagan and Frank". **Evidence.**

[SB]: "Two detailed mechanisms have been put forward." They may both be right for different substrates, since Denmark and Trapp studied different aldehydes (Geiger 2022). **Open.**

**Fig 7a, SMS tetramer cartoon** (SVG): two Zn₂O₂ squares (Zn and O alternating at corners) at left and right, each linked to the other's ring nitrogen by N→Zn arrows, closing a 12-membered ring; two zinc atoms marked with open circles "open site". Label "proposed geometry, based on X-ray structures (2015)". Schematic, no bond lengths.
**Fig 7b, Two models side by side** (SVG two columns): left, homochiral tetramer + aldehyde docked at both open zinc sites → product, with a crossed-out heterochiral tetramer "can't dock". Right, a small cycle: monomer + aldehyde → zinc hemiacetal (marked "slow step") → alkyl transfer → splits into two hemiacetal catalysts (doubling arrow). Headers "Denmark/Houk 2020" and "Trapp 2020–25"; footer "Open: may depend on substrate". Schematic.

---

## Tab 8. Why it matters, what's open, sources
**Takeaway:** non-linear effects became a standard tool for reading catalytic mechanisms, and the Soai reaction is the proof that one-handedness can arise by chemistry alone, though not how life did it.

*Uses* [SB; POP p. 6]:
- **A mechanism probe.** Plot product ee against catalyst ee: a straight line is consistent with one chiral unit in the selectivity-setting step; a curve signals two or more, aggregation, or a phase effect. This is now routine in asymmetric catalysis (Jacobsen's two-metal discovery is the classic case) [SB p. 7, 9, 16]. **Established.**
- **A design lever.** Chiral poisoning (Faller: adding a cheap chiral additive to switch off one hand of a racemic catalyst) and chiral activation (Mikami) let chemists get high ee without an enantiopure catalyst [SB p. 9]. **Established.**
- **Process chemistry.** Merck's 70% → 95% ee step for L-699,392 [SB]. Carreira's group made a key intermediate of the anti-HIV drug efavirenz by an asymmetric autocatalytic step, though no NLE data were reported [SB p. 14]. Broader claims of impact on pharmaceuticals, flavours, agrochemicals and materials come from [POP]/[PR] without named examples. **Evidence** for those general claims.
- **Origin of life.** A proof of concept that homochirality *can* emerge from achiral ingredients in a closed system, the first laboratory demonstration of Frank's model [SB p. 13]. It is not the prebiotic route; current work looks at reaction networks and kinetic resolution in water (Deng, Yu and Blackmond 2024). **Open.**

*Established vs open* (two-column panel):
- Established: product ee can bend away from catalyst ee in both directions when catalysts pair or aggregate; asymmetric autocatalysis with amplification exists (1995); 0.00005% → >99.5% ee in three runs (2003); absolute asymmetric synthesis with random handedness (Soai and Singleton, independently).
- Evidence: the detailed Soai mechanism (SMS tetramer vs zinc hemiacetal).
- Open: how biology's homochirality actually arose ([SB]: "we will probably never have a definitive answer"); a Soai-like amplifier for amino acids or sugars in water ([POP] p. 6 says groups are trying); wider industrial use of autocatalysis.

*Sources list:* all keys from Rex §0 with DOI links, plus "Numbers marked ≈ (our estimate) and equations marked 'our illustration' are our own arithmetic from these sources."

---

## Notes for Ivy, Frank and Tess (decisions on Rex's §10 flags)
1. **Optical rotation:** not repeated. Homochirality is described by configuration (L-amino acids, D-sugars); Tab 2 says outright that D/L doesn't fix the rotation sign.
2. **1995 seed:** 5% (from [SB]), not [POP]'s 2%.
3. **2003 endpoint:** ">99.5% ee" only. No "99.99%", no "100%", no "only one mirror image" as a literal claim.
4. **630,000:** quoted from [SB] as a stereoisomeric-ratio factor; not recomputed anywhere.
5. **Credit:** "independently, 2002–03" for Soai and Singleton; Singleton, Noyori, Blackmond, Denmark, Houk, Trapp, Jacobsen are named as non-laureates. Kagan 1986 is credited to the six-author team.
6. **Hajos–Parrish:** left out. Its –NLE was later disputed (Hoang, Bahmanyar, Houk & List 2003 reported a linear relationship), so the page uses only the sulfoxide (–NLE) and Sharpless (+NLE) examples.
7. **Thalidomide:** left out (it racemises in the body, so it's a misleading example). Motivation uses [PR]'s general statement.
8. **Marckwald:** left out.
9. **Our illustrations:** the Frank-type equations and phase line (Tab 3) and the √N estimate (Tab 6) carry an "our illustration" label. Note a correction to the dossier's §3 wording: in that model the *difference* R − S grows exponentially but the *ee* does not; the copying term cancels and amplification comes only from the antagonism term, as derived in Tab 3. Rex, please align §3 if you touch it again.
10. **Eq. 3:** \( f = (1+\beta)/(1+g\beta) \), with g = heterochiral/homochiral reactivity.
11. **1995 compound:** draw the 2-position as a generic "R". The 2003 compound is 2-(t-BuC≡C).
12. **Figure honesty:** real data in Fig 5b and Fig 6a only. Fig 4a is a computed model with illustrative parameters. Everything else is "Schematic".
