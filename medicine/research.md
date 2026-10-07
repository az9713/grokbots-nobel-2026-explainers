# 2026 Nobel Prize in Physiology or Medicine: research dossier (Rex Research)

Audience: PhD-level readers without a neuroscience or biology background. Source tags: **[SB]** is the committee's scientific background ("Optogenetics. Discovery of a neuronal switch", 15 pp.), which anchors almost everything here. **[PR]** is the press release. Claim tags: **FACT** means a primary source states it, **DERIVED** means my own arithmetic or textbook physics (shown or flagged), and **SPEC** means interpretation or an open question. Local copies are in `src/adv.pdf` and `src/adv.txt`. I checked every DOI below against Crossref on 7 Oct 2026; the list is in `src/dois.json`.

**Note on numbers:** this prize is about methods, and [SB] gives very few hard numbers. I have kept to the numbers it does give and flagged textbook values such as wavelengths and kinetics in §9 instead of slipping them in.

## 0. Primary sources
- [SB] https://www.nobelprize.org/uploads/2026/10/advanced-medicineprize2026.pdf, with a mirror at https://www.nobelprizemedicine.org/wp-content/uploads/2026/10/Nobel_Prize_ENG_adv.pdf. Its authors are A. El Manira, P. Svenningsson (Chair) and S. Linnarsson (Vice-Chair).
- [PR] https://www.nobelprize.org/prizes/medicine/2026/press-release/
- Key papers, with DOIs (FACT, verified on Crossref):
  - Harz & Hegemann 1991, Nature 351:489. Fast photocurrents in *Chlamydomonas*. `10.1038/351489a0`
  - Nagel et al. 2002, Science 296:2395. ChR1 is a light-gated proton channel. `10.1126/science.1072068`
  - Sineshchekov, Jung & Spudich 2002, PNAS 99:8689. CSRA and CSRB. `10.1073/pnas.122243399`
  - Nagel et al. 2003, PNAS 100:13940. ChR2 is a light-gated cation channel. `10.1073/pnas.1936192100`
  - Boyden, Zhang, Bamberg, Nagel & Deisseroth 2005, Nat Neurosci 8:1263. Millisecond control of spikes in neurons. `10.1038/nn1525`
  - Li et al. 2005, PNAS 102:17816. `10.1073/pnas.0509030102`
  - Nagel et al. 2005, Curr Biol 15:2279. *C. elegans*. `10.1016/j.cub.2005.11.032`
  - Zhang et al. 2006, Nat Methods 3:785. `10.1038/nmeth936`
  - Bi et al. 2006, Neuron 50:23. Vision restored in blind mice. `10.1016/j.neuron.2006.02.026`
  - Deisseroth et al. 2006, J Neurosci 26:10380. The term "optogenetics" is coined. `10.1523/jneurosci.3863-06.2006`
  - Aravanis et al. 2007, J Neural Eng 4:S143. Optical fibre in vivo, whisker control. `10.1088/1741-2560/4/3/s02`
  - Adamantidis et al. 2007, Nature 450:420. Hypocretin neurons and waking. `10.1038/nature06310`
  - Zhang et al. 2007, Nature 446:633. NpHR silencing. `10.1038/nature05744`
  - Han & Boyden 2007, PLOS ONE 2:e299. `10.1371/journal.pone.0000299`
  - Tye et al. 2011, Nature 471:358. Anxiety circuit. `10.1038/nature09820`
  - Lin et al. 2011, Nature 470:221. Aggression locus. `10.1038/nature09736`
  - Liu et al. 2012, Nature 484:381. Engram recall. `10.1038/nature11028`
  - Lammel et al. 2012, Nature 491:212. Reward vs aversion. `10.1038/nature11527`
  - Ramirez et al. 2013, Science 341:387. False memory. `10.1126/science.1239073`
  - Berndt et al. 2014, Science 344:420, `10.1126/science.1252367`, and Wietek et al. 2014, Science 344:409, `10.1126/science.1249375`. Engineered chloride ChRs.
  - Govorunova et al. 2015, Science 349:647. GtACRs. `10.1126/science.aaa7484`
  - Kohl et al. 2018, Nature 556:326. Parenting modules. `10.1038/s41586-018-0027-0`
  - Sahel et al. 2021, Nat Med 27:1223. Partial vision in a blind patient. `10.1038/s41591-021-01351-4`
  - Background papers: Crick 1999, Phil Trans R Soc B 354:2021, `10.1098/rstb.1999.0541`. Zemelman 2002, Neuron 33:15, `10.1016/s0896-6273(01)00574-8`. Banghart 2004, Nat Neurosci 7:1381, `10.1038/nn1356`. Oesterhelt & Stoeckenius 1971, Nature New Biol 233:149, `10.1038/newbio233149a0`. Armbruster 2007, PNAS 104:5163, `10.1073/pnas.0700293104`. Deisseroth 2015 review, Nat Neurosci 18:1213, `10.1038/nn.4091`.

## 1. The prize (FACT, from [PR])
- Announced **5 October 2026** by the Nobel Assembly at Karolinska Institutet. The prize is shared jointly by:
  - **Karl Deisseroth**, HHMI and Stanford University, USA. Born 1971; PhD 1998 and MD 2000 from Stanford.
  - **Peter Hegemann**, Humboldt University of Berlin. Born 1954; PhD 1984 at the MPI of Biochemistry, Martinsried, where the prize-winning work was done.
  - **Georg Nagel**, University of Würzburg. Born 1953; PhD 1988 from Frankfurt. The work was done at the MPI of Biophysics, Frankfurt.
- The citation reads: "**for their discoveries concerning light-gated ion channels and optogenetics**."
- The prize is 12 million SEK, shared equally. The committee chair, Per Svenningsson, said: "Optogenetics provides opportunities for mapping the brain in a way that we could once only dream of."
- The split of credit, in the press release's framing: Hegemann and Nagel discovered channelrhodopsin, and Deisseroth turned it into a light-controlled switch for neurons (2005 in cultured neurons, 2007 in living mice).

## 2. Backgrounder: the minimum biology (DERIVED, textbook; the reader needs this before §3)
- **Neuron:** a cell that signals electrically. The inside sits at a negative voltage relative to the outside, which is called the resting potential. *(The usual value, about −70 mV, is a textbook figure and **not in [SB]**.)*
- **Action potential (spike):** an all-or-none voltage pulse lasting about a millisecond, triggered when the membrane is pushed less negative (**depolarization**) past a threshold. Pushing it more negative (**hyperpolarization**) suppresses spikes. [SB] stresses that neural computation happens on the "millisecond timescale."
- **Ion channel versus pump** (this contrast is FACT in [SB] p. 6 and p. 8). A channel is a gated pore that lets ions flow passively *down* their electrochemical gradient, which is fast and carries many ions. A pump actively moves ions *against* the gradient, which is slow, at **one ion per photon** for light-driven pumps. That is why ChR2 (a channel) gives large, fast currents and NpHR (a pump) is less efficient.
- **Rhodopsin and retinal:** a 7-transmembrane protein plus a retinal chromophore. Light isomerizes the retinal and changes the protein's shape. Microbial (type I) rhodopsins couple this *directly* to ion movement, while animal vision uses a slower G-protein cascade. [SB] covers the microbial rhodopsins.
- **Genetic targeting:** a gene is delivered by a virus (lentivirus, AAV) under a cell-type-specific promoter, so only one defined cell type makes the protein. Then light delivered by optical fibre picks the *where and when*. **The protein gives cell-type specificity and the light gives millisecond, location-specific control.** That is the whole method in one sentence.
- Crick's requirement (FACT [SB], quoting Crick 1979 and 1999): activate or inactivate "all neurons of just one type… leaving the others more or less unaltered"; "the ideal signal would be light", an idea he called "rather far-fetched."
- [SB]'s design criteria for an ideal actuator (FACT): it is genetically encodable, compact, expresses well in the membrane, has fast kinetics, is reversible, and turns photons *directly* into membrane current.

## 3. Before channelrhodopsin: attempts and why they fell short (FACT [SB])
| Year | Approach | Limitation |
|---|---|---|
| 1971 | Fork: lasers on *Aplysia* neurons, using their weak intrinsic light sensitivity | not targetable |
| 1983 | Farber & Grinvald: dye-stained leech neurons | phototoxicity |
| 2002 | Miesenböck's chARGe: three *Drosophila* genes (arrestin-2, rhodopsin, Gαq) | multi-component, slow, needs added retinal |
| 2005 | Lima & Miesenböck: P2X2 receptor plus caged ATP | needs a chemical, limited by diffusion |
| 2004 onward | Isacoff, Kramer, Trauner: photoswitchable tethered azobenzene ligand on the Shaker K⁺ channel (Banghart 2004), then a glutamate receptor (Volgraf 2006, Szobota 2007) | needs a synthetic compound delivered into tissue |
- The lesson [SB] draws: it had to be "a single protein… delivered genetically… coupl[ing] photon absorption directly to ionic current with millisecond kinetics."

## 4. Microbial rhodopsins: the molecular lineage (FACT [SB])
- Bacteriorhodopsin, a light-driven **proton pump**, was found in *Halobacterium* by Oesterhelt & Stoeckenius (1971, 1973). Halorhodopsin, a **chloride pump**, followed (Matsuno-Yagi & Mukohata 1977, Mukohata & Kaji 1981); the *Natronomonas pharaonis* variant is NpHR. These established that a single protein can move a specific ion when hit by light.
- Hegemann did his PhD with Oesterhelt, which links the two lines.

## 5. Discovery of channelrhodopsin, step by step (FACT [SB] unless tagged)
1. **Phototaxis:** *Chlamydomonas reinhardtii*, a single-celled alga with two flagella, swims toward light using an **eyespot** and a rhodopsin-like chromophore (Foster et al. 1984; Uhl & Hegemann 1990).
2. **Suction-pipette recordings** (Harz & Hegemann 1991; method from Litvin and Sineshchekov in *Haematococcus*) showed photocurrents with **microsecond latency** after a flash. That is too fast for a second-messenger cascade, so Hegemann's team proposed that **the receptor and the channel are one protein** (Harz 1992; Holland 1996). This was the conceptual turning point.
3. **Genes:** the *Chlamydomonas* EST database (Asamizu 2000) let three groups (Hegemann, Spudich, Takahashi) independently find cDNAs homologous to bacteriorhodopsin. Hegemann named them **channelopsin-1 (Chop1, GenBank AF385748)** and **Chop2 (AF461397)**. Spudich's group called them CSRA and CSRB and used RNAi to show they drive the photocurrents (Sineshchekov 2002). Takahashi's group placed them in the eyespot by immunofluorescence (Suzuki 2003).
4. **ChR1, 2002 (Nagel, Hegemann, Bamberg):** in *Xenopus* oocytes with all-trans retinal, two-electrode voltage clamp showed that **green light** drives an inward **proton** current. A truncated 7-TM core was enough, which proved the protein itself is the channel. This was the first direct evidence of a light-gated ion channel.
5. **ChR2, 2003 (Nagel et al., PNAS):** expressed in oocytes and HEK cells. It has a **blue-shifted** action spectrum and is a **broad, non-selective cation channel**. The **first 315 amino acids** are sufficient. The current shows a transient peak that relaxes to a steady-state plateau under continuous light. Reversal-potential shifts confirmed passive inward cation flux. [SB] calls this "arguably more consequential."
6. **Neurons, 2005 (Boyden, Zhang, Bamberg, Nagel, Deisseroth):** ChR2 with a fluorescent tag was delivered by **lentivirus** into cultured **hippocampal neurons** (rat, per [PR]). It expressed stably in the membrane with no apparent toxicity. Blue light drove **precise, millisecond-scale action potentials, including trains at increasing frequencies** ([SB] Fig. 3). Nagel observed that **no added retinal was needed**, because trace endogenous retinal was enough. This is what made in vivo work practical.
7. Independent confirmations followed within a year: hippocampal neurons and chick spinal cord (Li 2005), *C. elegans* behaviour (Nagel 2005), retina (Bi 2006), *Drosophila* learning (Schroll 2006), and in vivo tissue (Bi 2006; Ishizuka 2006; Zhang 2006).
8. **The name:** "optogenetics" was coined in a 2006 J Neurosci review by Deisseroth, Feng, Majewska, Miesenböck, Ting and Schnitzer.
9. **In vivo, 2007 (Aravanis et al.):** laser diode plus optical fibre in freely behaving rodents. ChR2 in **layer 5 excitatory neurons of vibrissal motor cortex** made the whiskers deflect on light. Again no added retinal was needed.

Priority note (FACT, but sensitive): [SB] credits Spudich and Takahashi with parallel gene identification, and Boyden is first author of the 2005 paper. Neither is a laureate. Present this neutrally and quote [SB]'s wording.

## 6. The toolbox (FACT [SB])
- **Silencing:** in 2007, Zhang et al. (Deisseroth lab) and Han & Boyden adapted **NpHR**, a **yellow-light** chloride pump that hyperpolarizes neurons. Because it is spectrally separate from blue ChR2, it allowed the **first two-colour, bidirectional control**. Later variants: eNpHR3.0 (Gradinaru 2010) and proton pumps (Chow 2010). Limitation: one ion per photon.
- **Chloride channels:** ChR2 was engineered to conduct chloride (Berndt 2014; Wietek 2014, Hegemann lab). Natural anion channels **GtACR1 and GtACR2** came from the alga *Guillardia theta* (Govorunova 2015, Spudich lab). They have much higher light sensitivity and chloride conductance than the pumps.
- **Red-shifted:** Chrimson is used in primate and human retina (Gauvain 2021; Sahel 2021).
- **The complementary method:** chemogenetics with DREADDs (Armbruster 2007, Roth lab). These are engineered GPCRs activated by CNO or deschloroclozapine. They are slower and systemic, which suits prolonged modulation, and [SB] notes they may eventually be usable in humans.

## 7. What it revealed: causal circuit neuroscience (FACT [SB]; these are the examples Sommer should use)
- **Sleep and waking** (Adamantidis 2007, Deisseroth and de Lecea): stimulating hypocretin/orexin neurons in the lateral hypothalamus made transitions to waking more likely from both slow-wave and REM sleep. The latency depended on stimulation frequency. [SB] calls it one of the first demonstrations of a direct causal link to a mammalian behaviour.
- **Memory engrams** (Tonegawa lab): ChR2 was put into dentate gyrus cells that were active during fear conditioning. Reactivating them in a neutral context triggered freezing, so activating that ensemble is *sufficient* for recall (Liu 2012). They also created a **false memory**: cells tagged in a safe context were reactivated during shock in another context, and the mice then froze in the safe context (Ramirez 2013).
- **Dopamine is not one broadcast signal** (Lammel 2012): in the VTA, inputs from the laterodorsal tegmentum drive **reward** and inputs from the lateral habenula drive **aversion**.
- **Anxiety is built from pathways:** activating basolateral amygdala projections to central amygdala is anxiolytic (Tye 2011). Projections from basolateral amygdala to ventral hippocampus increase anxiety (Felix-Ortiz 2013). In the anterodorsal BNST, projections to the lateral hypothalamus drive risk avoidance and projections to the VTA carry positive valence (Kim 2013).
- **Innate behaviours:** stimulating Esr1+ neurons in ventrolateral VMH produces a graded continuum from social interaction to mounting to attack, depending on intensity (Lin 2011; Lee 2014). Galanin neurons in the medial preoptic area split parenting into separate modules for pup interaction, motivation and adult social behaviour (Kohl 2018).
- **Locomotion:** neurons in the mesencephalic locomotor region separate into streams for speed, body extension and forelimb manipulation (Caggiano 2018; Ferreira-Pinto 2021).
- [SB]'s thesis: behaviours "are assembled from discrete, projection-defined circuits," and neuroscience has moved "from observing and 'reading'… to actively 'writing'."

## 8. The clinic: restoring vision (FACT [SB])
- In **retinitis pigmentosa**, inherited mutations destroy rods and cones, but retinal ganglion cells survive.
- In mice, AAV-delivered ChR2 in ganglion cells restored light responses that reached visual cortex (Bi 2006). In marmosets, ChR2 expressed in surviving retina (Ivanova 2010). In macaques, Chrimson gave high expression and responsiveness (Gauvain 2021).
- **The first patient (Sahel et al. 2021, Nat Med; Roska is senior author):** Chrimson was delivered to ganglion cells, and engineered goggles supplied light pulses. The result was a **prolonged, partial** restoration: the patient could tell apart high-contrast objects on a table, and EEG showed object-related activity in visual cortex. This is **n = 1**.
- "**Several clinical trials… are presently underway**" ([SB]). [SB] gives no trial names or counts, and I have not verified any. **Do not name trials.**

## 9. Fact vs speculation
**Established:** ChR1 and ChR2 are single-protein light-gated channels (2002 and 2003). ChR2 drives millisecond spikes in neurons (2005) and controls behaviour in vivo (2007). Optogenetics has established causal circuit-behaviour links across sleep, memory, reward, anxiety, aggression, parenting and locomotion.
**Evidence (early or limited):** human vision restoration, which rests on one patient (Sahel 2021) plus trials in progress.
**Open or speculative:** wider human therapeutic use (light delivery, gene-therapy safety, immune response; **not discussed in [SB]**, so tag any mention SPEC), and chemogenetics in humans ([SB] says "may eventually").

## 10. Flags for Tess
1. Wavelengths and kinetics are **not in [SB]**. The often-quoted ChR2 peak near 470 nm, NpHR near 580 nm, ChR2 off-kinetics of about 10 ms, and a resting potential of about −70 mV are all textbook values. Use them only as labelled approximations, or leave them out. [SB] only says "blue", "green", "yellow" and "red-shifted."
2. The press release says the 2005 neurons were "from rats". [SB] says hippocampal neurons and doesn't name the species.
3. On "two years later… living mice" (2007): the [SB] Fig. 4 caption says "in vivo in mice (Aravanis et al. 2007)", which is consistent with the press release.
4. Credit is sensitive: Spudich, Takahashi, Boyden, Bamberg and Miesenböck are named in [SB] but are not laureates. Keep the wording neutral.
5. [SB] says "the late Susumu Tonegawa's laboratory". Report it as [SB] words it; I did not verify it independently.
6. The Aravanis 2007 DOI resolves on Crossref to "An optical neural interface: in vivo control…". Its title has inline markup, but it matches.
7. There are no figures with axis values to reproduce from [SB]. Every figure should be **schematic**: algal eyespot and phototaxis, ChR2 in a membrane (channel vs pump), oocyte recording showing peak and plateau, a spike train locked to light pulses, fibre in the brain with whisker deflection, the engram-tagging protocol, VTA reward and aversion pathways, and the retina with goggles.
