# Nobel Medicine 2026 explainer: narrative + figure specs (Sommer → Frank)

Every claim and number comes from `/workspace/nobel2026-medicine/research.md` (Rex). Citation keys in [brackets] use [SB], [PR] or "Author Year", matching Rex §0. Reader-facing tag pills: **Established**, **Evidence**, **Open**. Textbook values that are not in [SB] carry "≈ textbook value". Frank: don't add numbers that aren't here. Every figure is captioned "Schematic".

## Global layout
- Same frame as the physics explainer: dark mode, a horizontal tab bar with 8 tabs, each tab about 1–2 screens long, `#t1`–`#t8` hash links, and arrow-key navigation.
- Header: "The 2026 Nobel Prize in Physiology or Medicine: switching neurons on and off with light". Subline: "Karl Deisseroth, Peter Hegemann, Georg Nagel · 5 Oct 2026".
- Each tab opens with a one-line **Takeaway** box. Each term is bold at first use, with an inline definition.
- Footer on every tab links to the Sources section on tab 8.

---

## Tab 1. The prize
**Takeaway:** an alga's light sensor turned out to be a light-switched pore, and putting it into neurons let scientists turn chosen brain cells on and off with millisecond timing.

The Nobel Assembly at Karolinska Institutet split the prize equally among three laureates "for their discoveries concerning light-gated ion channels and optogenetics" [PR]:
- Karl Deisseroth (HHMI and Stanford, born 1971)
- Peter Hegemann (Humboldt University of Berlin, born 1954)
- Georg Nagel (University of Würzburg, born 1953)

In the press release's framing, Hegemann and Nagel discovered **channelrhodopsin** (a light-sensing protein from algae that is itself an ion channel), and Deisseroth turned it into a light-controlled switch for neurons: first in cultured neurons in 2005, then in living mice in 2007 [PR]. Committee chair Per Svenningsson put the payoff this way: "Optogenetics provides opportunities for mapping the brain in a way that we could once only dream of."

**Fig 1: Timeline** (horizontal SVG). The ticks are:
- 1971 bacteriorhodopsin
- 1991 fast algal photocurrents
- 2002 ChR1
- 2003 ChR2
- 2005 neurons spike to light
- 2006 the word "optogenetics"
- 2007 living mice and the first silencer
- 2011–2013 circuit maps
- 2021 first patient

Colour-code each tick by laureate lab where [SB] attributes it: Hegemann/Nagel for 1991–2003, the joint paper for 2005, Deisseroth for 2006–2007. Grey the others.

---

## Tab 2. The minimum neuroscience
**Takeaway:** neurons compute with millisecond voltage spikes, so a useful control tool has to be that fast and has to hit only one cell type.

A **neuron** is a cell that signals electrically. Its interior is held negative relative to the outside; this is the **resting potential**, typically around −70 mV (≈ textbook value). Pushing the membrane less negative is **depolarization**. Past a threshold it fires an **action potential** (a **spike**), an all-or-none pulse about a millisecond long. Pushing it more negative is **hyperpolarization**, which suppresses spikes. [SB] stresses that the brain computes "on the millisecond timescale."

Ions cross the membrane in two ways [SB pp. 6, 8]:
- An **ion channel** is a gated pore. When open, ions flow passively *down* their gradient, many per opening, and fast.
- A **pump** actively pushes ions *against* their gradient. Light-driven pumps move **one ion per photon**, so their currents are smaller.

This difference explains why channelrhodopsin, a light-gated channel (tab 4), mattered so much.

A **rhodopsin** is a protein that crosses the membrane seven times and holds **retinal**, a light-absorbing molecule related to vitamin A. Light changes retinal's shape, and that changes the protein. In **microbial rhodopsins**, the protein moves ions directly. Animal vision instead relays the signal through a slower chain of enzymes.

**Genetic targeting:** a virus delivers the gene with a **promoter**, a DNA switch that only one cell type reads. Only those cells make the protein. The method in one line: **the protein picks *which* cells; the light picks *where* and *when*.**

Francis Crick had asked for exactly this. He wanted a way to switch "all neurons of just one type" while "leaving the others more or less unaltered", and he wrote that "the ideal signal would be light", an idea he called "rather far-fetched" [SB, Crick 1999].

**Fig 2a: Spike** (SVG). A voltage trace shows rest, a depolarizing push, threshold, the spike and the return. Label the axes "voltage" and "time (~1 ms spike)". There are no other values except an optional "≈ −70 mV (textbook)" label.

**Fig 2b: Channel vs pump** (SVG). Two membrane patches side by side.
- Left: an open pore with many ions streaming downhill, labelled "channel: passive, many ions, fast".
- Right: a pump carrying one ion uphill per photon, labelled "pump: active, 1 ion per photon".

---

## Tab 3. The problem: earlier attempts
**Takeaway:** every earlier light-control trick failed at least one requirement: genetically targetable, one component, fast, and needing no added chemical.

The criteria [SB] set for an ideal tool:
- genetically encodable and compact
- expresses well in the membrane
- fast and reversible
- turns photons *directly* into current

**Fig 3: Scorecard table/matrix** (styled HTML table). Rows are the earlier approaches in Rex §3:
- Fork 1971
- Farber & Grinvald 1983
- chARGe 2002
- P2X2 + caged ATP 2005
- photoswitchable tethered ligands 2004 onward
- ChR2 2005, in the last row

Columns are: targetable · single protein · fast · no added chemical. Mark ✓ or ✕ from the Limitation column. Only ChR2 is all ✓, though chARGe is targetable. Show each limitation on hover, using Rex's wording. Add a footnote that the ✓/✕ marks condense [SB]'s stated limitations.

[SB]'s conclusion: the answer had to be "a single protein… delivered genetically… coupl[ing] photon absorption directly to ionic current with millisecond kinetics."

---

## Tab 4. The discovery: from alga to channel
**Takeaway:** a photocurrent too fast for an enzyme chain suggested that receptor and pore were one protein, and putting the gene into frog eggs proved it.

1. **The alga.** *Chlamydomonas reinhardtii* is a single-celled green alga that swims toward light using an **eyespot**, a light-sensing patch [SB].
2. **The clue (1991).** Harz and Hegemann recorded currents from swimming cells with a suction pipette. The current started **microseconds** after a flash of light. That is too fast for a chain of messenger molecules, so Hegemann's team proposed that **the light receptor and the ion channel are a single protein** [Harz & Hegemann 1991; SB]. ***Established.***
3. **The genes.** Three groups (Hegemann, Spudich, Takahashi) independently found algal genes resembling bacteriorhodopsin. Bacteriorhodopsin is a light-driven proton pump found in 1971 in a salt-loving microbe, and Hegemann trained in the lab that studied it. He named the genes Chop1 and Chop2. Spudich's group showed that they drive the photocurrents, and Takahashi's group located them in the eyespot [SB]. Keep this wording neutral: [SB] credits all three groups for this step.
4. **ChR1 (2002).** Nagel, Hegemann and Bamberg expressed the gene in ***Xenopus* oocytes**, large frog egg cells used as test tubes for membrane proteins. **Voltage clamp** holds the cell's voltage fixed and measures the current. **Green** light drove an inward **proton** current. A shortened core of the protein was enough, so the protein *is* the channel. This was the first light-gated ion channel [Nagel 2002; SB]. ***Established.***
5. **ChR2 (2003).** It responds to **bluer** light and passes **cations** in general, meaning positive ions, not only protons. The first 315 amino acids suffice. Under steady light the current spikes to a **peak**, then settles to a **plateau** [Nagel 2003; SB]. [SB] calls this "arguably more consequential", because letting positive ions in depolarizes a neuron.

**Fig 4a: Alga** (SVG). Shows a *Chlamydomonas* cell with two flagella, the eyespot, a light arrow and a swim-direction arrow.

**Fig 4b: Oocyte recording** (SVG). Left: an oocyte with two electrodes, labelled "voltage clamp". Right: a current trace under a light bar, showing a sharp transient peak that relaxes to a plateau and then returns when the light goes off. There are no axis values. Caption: "ChR2 photocurrent, peak then plateau (schematic) [Nagel 2003]".

**Fig 4c: ChR2 in the membrane** (SVG). The seven helices hold retinal. Blue light opens the pore and cations flow in. Use a small inset that reuses Fig 2b's channel/pump contrast.

---

## Tab 5. Making neurons obey light
**Takeaway:** in 2005, ChR2 put into neurons made them fire on cue, pulse for pulse, and in 2007 the same trick moved a living mouse's whiskers.

**2005 (Boyden, Zhang, Bamberg, Nagel, Deisseroth).** The team used a **lentivirus**, a gene-delivery virus, to put ChR2 into cultured hippocampal neurons from rats [PR]; [SB] does not name the species. The protein sat in the membrane with no apparent toxicity. Blue light pulses drove **precise, millisecond-scale spikes, including trains at increasing frequencies** [SB]. No retinal had to be added, because the trace amount already in the cells was enough. That detail made in-animal work practical. ***Established.*** Within a year, other groups confirmed it in chick spinal cord, worms (*C. elegans*), retina, fruit flies and living tissue [SB].

**2006.** Deisseroth and co-authors coined the word **optogenetics** in a J Neurosci review [Deisseroth 2006].

**2007 (Aravanis et al.).** A laser diode was coupled to an **optical fibre** implanted in the brain of freely moving rodents. Light on ChR2-expressing neurons in the whisker motor cortex made the whiskers deflect [SB; Aravanis 2007]. ***Established.***

**Interactive Fig 5a: Light pulses → spikes** (canvas). A slider sets the pulse rate across a few rates labelled only "low → high". The top track shows blue light pulses and the bottom track a voltage trace with one spike per pulse. Caption: "Schematic of [SB] Fig. 3: spikes follow light pulse trains". Don't claim a frequency limit, because [SB] gives none.

**Fig 5b: Fibre in vivo** (SVG). A mouse head in profile with an implanted fibre into motor cortex. Highlight the ChR2 cells, and show the whisker in its rest and deflected positions.

---

## Tab 6. The toolbox
**Takeaway:** after the on-switch came off-switches and colour variants, so one experiment could excite and silence different cells with different colours.

- **Silencing (2007).** **NpHR** is a **yellow**-light chloride pump from a salt-loving microbe. It pushes negative ions in, which hyperpolarizes the neuron. Because it responds to a different colour from blue ChR2, the same tissue could be driven both ways: the **first two-colour, bidirectional control** [Zhang 2007; Han & Boyden 2007; SB]. Its limit is that, as a pump, it moves only one ion per photon.
- **Chloride channels.** ChR2 was re-engineered to pass chloride [Berndt 2014; Wietek 2014]. Natural anion channels GtACR1 and GtACR2 came from the alga *Guillardia theta* [Govorunova 2015]. Both conduct far more than the pumps and are far more light-sensitive [SB].
- **Red-shifted.** **Chrimson** responds to longer, redder light and is used in primate and human retina [SB].
- **Chemogenetics**, the complementary approach. **DREADDs** are engineered receptors switched on by a drug rather than light [Armbruster 2007]. They are slower and act body-wide, which suits long-lasting modulation [SB].

**Fig 6: Toolbox palette** (SVG). Cards in a row are coloured by their [SB] colour words: ChR2 blue (excite), ChR1 green (protons), NpHR yellow (silence), Chrimson red-shifted (excite), GtACR (silence, channel), DREADD as a pill icon (drug, slow). Each card has an arrow for depolarize or hyperpolarize and a channel or pump icon. **Don't put nm values on the cards.** If Frank wants a spectrum strip, label it "approximate textbook peaks: ChR2 ≈ 470 nm, NpHR ≈ 580 nm (not from [SB])", or leave it out.

---

## Tab 7. What it revealed
**Takeaway:** for the first time, researchers could *write* activity into a defined circuit and watch the behaviour change, which proves cause instead of correlation.

[SB]'s thesis is that behaviours "are assembled from discrete, projection-defined circuits", and that neuroscience moved "from observing and 'reading'… to actively 'writing'." Here **projection** means the axon pathway from one brain region to another. All of the findings below are ***Established*** in mice.

**Interactive Fig 7: Circuit explorer** (SVG brain schematic, sagittal mouse brain with labelled regions). Clicking a pathway lights it up and opens its card.
- **Sleep → waking** [Adamantidis 2007]: stimulating hypocretin (orexin) neurons in the lateral hypothalamus made the mouse more likely to wake from both deep and REM sleep, and how fast depended on stimulation frequency. This was one of the first direct causal links to a mammalian behaviour [SB].
- **Memory engrams** [Liu 2012; Ramirez 2013]: an **engram** is the set of cells that stores a memory. Cells in the hippocampal dentate gyrus that were active during fear learning were tagged with ChR2. Reactivating them in a neutral box made mice freeze, so these cells are *sufficient* for recall. The same method planted a **false memory**: the safe-box cells were reactivated during a shock, and the mice then feared the safe box.
- **Reward vs aversion** [Lammel 2012]: in the VTA, a dopamine hub, input from the laterodorsal tegmentum drives **reward** and input from the lateral habenula drives **aversion**. Dopamine is not one broadcast signal.
- **Anxiety** [Tye 2011; SB]: basolateral amygdala → central amygdala lowers anxiety, basolateral amygdala → ventral hippocampus raises it, and the BNST splits into risk-avoidance and positive-valence outputs.
- **Aggression and parenting** [Lin 2011; Kohl 2018; SB]: Esr1+ neurons in the VMH give a graded continuum from social interaction to mounting to attack as intensity rises. Galanin neurons in the medial preoptic area split parenting into separate modules.
- **Locomotion** [SB]: midbrain locomotor neurons separate into streams for speed, body extension and forelimb use.

**Fig 7b: Engram protocol** (SVG, three panels): (1) fear learning in box A, with active cells tagged; (2) neutral box B, light on, mouse freezes; (3) false memory: box A cells reactivated during a shock in box C, then the mouse freezes in A.

---

## Tab 8. The clinic, what's open, sources
**Takeaway:** one blind patient has partial vision back. That is a proof of concept, not yet a therapy.

**Restoring vision** [SB].
- **The disease.** In **retinitis pigmentosa**, inherited mutations kill the rods and cones, the retina's light-sensing cells. The **retinal ganglion cells**, which carry the signal to the brain, survive.
- **The idea.** Make those surviving ganglion cells light-sensitive.
- **The path to people.** It was tested in mice with ChR2 [Bi 2006], then in marmosets, then in macaques with Chrimson.
- **The first patient** [Sahel 2021]: Chrimson was delivered into the ganglion cells, and engineered goggles turned the scene into light pulses. The patient regained **prolonged, partial** vision and could tell apart high-contrast objects on a table. EEG, a recording of brain activity from scalp electrodes, showed object-related activity in visual cortex. ***Evidence (n = 1).***
- **Trials.** [SB] says "several clinical trials… are presently underway." **Name no trials and give no counts.**

**Fig 8a: Retina and goggles** (SVG). A camera in the goggles sends light pulses to the eye. A retina cross-section shows dead rods and cones greyed out, and red-shifted light reaching ganglion cells that express Chrimson. An arrow runs to visual cortex.

**Established / Evidence / Open** (three columns, from Rex §9):
- **Established:** ChR1 and ChR2 are single-protein light-gated channels. ChR2 drives millisecond spikes in neurons (2005). The method controls behaviour in vivo (2007). Causal circuit-behaviour links are established for sleep, memory, reward, anxiety, aggression, parenting and locomotion.
- **Evidence:** human vision restoration rests on one patient, with trials underway.
- **Open (SPEC, not in [SB]):** wider human therapy. The hurdles are getting light into tissue, gene-therapy safety and immune responses. [SB] says chemogenetics "may eventually" be usable in humans.

**Credit note** (small panel). The discovery involved more people than the three laureates. [SB] names Spudich, Takahashi, Boyden, Bamberg and Miesenböck, along with others. Keep the wording neutral and quote [SB].

**Sources:** all of Rex §0 with doi.org links, plus [SB] and [PR] URLs. Add a note that values marked "≈ textbook value" are not from [SB].

---

## Notes for Frank and Tess
- Rex flag 1: nm and ms values appear only as labelled textbook approximations, in Fig 2a and the optional Fig 6 strip. Everything else uses [SB]'s colour words.
- Rex flag 2: rats are attributed to [PR].
- Rex flag 5: [SB] says "the late Susumu Tonegawa's laboratory". I avoided the phrase and wrote "Tonegawa lab" only in the citation; the text uses Liu 2012 and Ramirez 2013 as the citations.
- Rex flag 4: credit is handled neutrally in tab 4 and the tab 8 credit note.
- No quantitative figures. Every figure is schematic.
