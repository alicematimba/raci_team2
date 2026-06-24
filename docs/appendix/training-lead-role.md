# Understanding the Training Lead Role

A common source of confusion about the Training Lead role is conflating domain expertise with technical development. The Training Leads are not developers — they do not build environments, produce content, or design learning. What they bring to the pipeline is something different and irreplaceable: deep domain expertise applied specifically to the question of whether a course is sound enough to be delivered to learners.

---

## What this means in practice

When an Education Developer writes learning outcomes for an informatics practical, the Informatics Training Lead reviews them — not to improve the pedagogy, but to confirm the framing is current, appropriate for the learner level, and reflects meaningful practice in the field. The Lead is not a co-author of those outcomes; they are the domain quality gate.

When the Informatics Technical Developer configures a bioinformatics compute environment, the Informatics Training Lead validates it — not by doing the configuration, but by running through the workflows as a domain expert and confirming they work as the teaching requires. The Lead's A on environment readiness is an expert sign-off, not a development role.

When a lab practical runs for the first time, the Lab Training Lead's accountability for approach validity and safety sign-off comes from their knowledge of wet lab science, safety requirements, and what learners at different levels can safely do. That is domain expertise protecting the integrity of delivery — not educational design, and not technical build.

---

## The three distinct expertise types in this pipeline

Understanding why these roles sit next to each other without overlapping requires separating three types of expertise:

| Expertise type | Role | What they contribute |
|----------------|------|----------------------|
| **Pedagogical and educational design** | Education Developers | How content is structured, sequenced, and delivered to maximise learning. They are the experts on the learner experience. They are not expected to have deep domain expertise — that is why they work with Training Leads and SMEs. |
| **Domain expertise in the service of educational quality** | Training Leads | Whether the science or methods are right — current, appropriate for the audience, valid for this context. They validate; they do not design the learning or build the infrastructure. Their expertise is applied as a quality gate at key decision points. |
| **Engineering and build** | Technical Developers | How to provision, configure, and maintain the technical environments and systems that make delivery possible. They are not scientific validators — they build what has been specified and approved. |

!!! warning "Why this boundary matters"
    Tension arises when a Training Lead is expected to act as a developer (asked to 'fix' an environment or 'redo' a practical) or when developers are asked to make domain judgements about content validity. The RACI is designed to prevent both. The Lead brings expertise; the Developer brings build capability. They need each other — but they are not interchangeable.

---

## What each role checks at the QA stage

The following examples show both review lenses applied to the same practical — illustrating what each role is checking and why both are needed.

### Whole-genome sequencing practical (Illumina short-read)

=== "Training Lead — approach currency and validity"

    - The protocol uses a library prep kit designed for human genomics — for clinical microbiology, a different kit with shorter insert sizes is more appropriate for bacterial genomes. **Needs changing.**
    - The expected output (>5Gb per sample) is based on a full flow cell — for a teaching run, a partial flow cell giving ~1Gb is sufficient and more realistic for participants to see in clinical practice.
    - The quality control thresholds used (Q30 >80%) are appropriate for this audience and reflect current clinical WGS standards.
    - Participants at this level can be expected to perform library prep independently with written guidance — no live demonstration needed for experienced microbiologists.

=== "Technical Developer — feasibility and build"

    - The library preparation protocol has 14 steps and is scheduled for a 3-hour slot — feasible, but only if DNA quantification (step 3) uses the plate reader, not the Nanodrop, which queues.
    - The protocol assumes pre-quantified DNA inputs from the morning session — the handoff timing needs confirming with the Education Developer.
    - The sequencing run is set to run overnight and be ready for the informatics session at 09:00 the next morning — the instrument queue and run time need confirming.
    - FastQ files need to be on the shared drive before the informatics session begins — an automated transfer script should be in place.

!!! info "What the Education Developer does with both reviews"
    The Technical Developer's flag on the Nanodrop queue means the session plan needs a 20-minute buffer — the Education Developer adjusts the afternoon schedule. The Training Lead's flag on the library prep kit is a domain correction — the Education Developer updates the SME brief and confirms the kit change with the supplier. Neither flag is the Education Developer's domain to judge — but both land with them to manage the resolution and update the design.

---

## Domain-specific review examples

### Lab domain — DNA extraction and library preparation

=== "Lab Training Lead — approach currency and validity"

    - Is the extraction method appropriate for this organism and sample type? (e.g. CTAB for plant material, bead-beating for gram-positive bacteria, column-based for clinical swabs — these are not interchangeable)
    - Are expected DNA yields and purity metrics (A260/280 ratio) realistic for this input material? Will participants see meaningful results or spend the session troubleshooting poor yields?
    - Is the library prep kit appropriate for the sequencing platform and organism? (e.g. a human-genome kit used for bacterial WGS gives poor results — insert size distributions differ significantly)
    - Are the quality control thresholds specified (Qubit concentration, Bioanalyzer fragment size) consistent with current standards for this application?
    - Is the safety guidance adequate for the reagents involved? (ethanol, phenol-chloroform, and column wash buffers each carry different risks that must be correctly documented)
    - Does the protocol represent current best practice, or has it been superseded by a method that would better prepare participants for real-world application?

=== "Lab Technical Developer — feasibility and build"

    - Is the centrifuge capacity sufficient for the participant group? If 20 participants each have 4 tubes at the same step, how many centrifuge runs are needed and does the session timing allow for it?
    - Have all reagents been sourced, are they in date, and are they available in sufficient volume? Has a buffer been prepared fresh where required?
    - Has the full protocol been tested in this lab with this equipment to confirm the expected yields? Protocols from literature or kit manuals often need optimisation for local conditions.
    - Does the timing add up step by step? (e.g. ethanol precipitation requires 20 minutes on ice — does the session plan account for this?)
    - Are all instruments serviced and calibrated: Qubit, Bioanalyzer, thermocycler, centrifuge? Are consumables (tips, tubes, spin columns) pre-prepared per participant?
    - Are DNA samples pre-extracted and available as backups, in case participant extractions fail and the session needs to continue?

---

### Lab domain — real-time PCR practical for pathogen detection

=== "Lab Training Lead — approach currency and validity"

    - Are the primer and probe sequences validated for the target pathogen? Have they been checked against current databases for specificity? Cross-reactivity with related organisms is a common issue in clinical diagnostics.
    - Are the cycling conditions (annealing temperature, extension time) appropriate for this polymerase and target amplicon size?
    - Are the positive and negative controls scientifically appropriate? Is the positive control at a clinically relevant concentration, or so high it gives no information about assay sensitivity?
    - Will the expected Ct values make sense to participants — are the samples designed to produce a range of results that illustrate the clinical interpretation challenge?
    - Does the interpretation guidance reflect current clinical practice? (Ct thresholds for clinical action vary by institution and pathogen — this should be framed as illustrative, not prescriptive)

=== "Lab Technical Developer — feasibility and build"

    - How many thermocyclers are available and how many participants share each? A 40-cycle qPCR run takes 90 minutes — does the session slot allow for setup, run, and interpretation?
    - Are the fluorescent dyes compatible with the detection channels on the specific qPCR instruments in this lab? (FAM/SYBR on one instrument, ROX normalisation requirements differ)
    - Are all reagents prepared, aliquoted, and on ice before participants arrive? Has a master mix been pre-calculated for the number of reactions including controls?
    - Has the protocol been tested on these specific instruments to confirm the cycling conditions produce clean amplification curves?
    - Is there a contingency if a thermocycler fails mid-run? Is a backup machine available or pre-booked?

---

### Informatics domain — variant calling and genome analysis

=== "Informatics Training Lead — approach currency and validity"

    - Is the analysis pipeline appropriate for this organism and variant type? (BWA-MEM + GATK is standard for human SNVs; for bacterial WGS, Snippy or a reference-based approach is more appropriate — these are not interchangeable)
    - Are the filtering thresholds scientifically justified for this application? (A QUAL score threshold appropriate for research may differ from clinical diagnostic practice — participants need to understand the difference)
    - Do the example datasets contain real, meaningful variation at the expected frequency and type? Synthetic or over-simplified datasets can give participants a misleading picture of real-world analysis challenges.
    - Is the biological interpretation of results correct? If the session shows a resistance gene call, is the clinical implication stated accurately and with appropriate nuance?
    - Does the pipeline represent current best practice, or has it been superseded? (Tools like Kraken, MetaPhlAn, and Bracken update rapidly — version choices carry implications)

=== "Informatics Technical Developer — feasibility and build"

    - Does the compute environment have sufficient memory for the alignment step? (BWA-MEM alignment of a 5Gb bacterial dataset requires ~8GB RAM per user — if 20 participants run simultaneously, the environment needs sufficient capacity or jobs will queue or fail)
    - How long does each pipeline step take? If the alignment step takes 20 minutes per sample, the session needs either pre-computed BAM files provided at that stage, or the time must be built into the session plan explicitly.
    - Are all software tools installed at the correct versions, with all dependencies resolved? (GATK version changes frequently and older workflows can break — the environment must be tested end to end, not just installed)
    - Is the reference genome pre-indexed? (BWA index creation for a bacterial genome takes several minutes — this must be done before the session, not during it)
    - Do all input files sit in the correct directory structure with appropriate read/write permissions for participant accounts? Has a test run confirmed participants can execute all steps without file path or permission errors?

---

### Informatics domain — outbreak investigation and phylogenetics

=== "Informatics Training Lead — approach currency and validity"

    - Is the tree-building algorithm appropriate for the dataset size and type? (Maximum likelihood is appropriate for SNP alignments; neighbour-joining is faster but less accurate — the choice should be justified, not just convenient)
    - Is the bootstrapping threshold guidance correct and presented with appropriate caveats? (Bootstrap values of 70+ are conventional but context-dependent — participants should understand what the threshold means, not just apply it)
    - Does the phylogenetic interpretation example correctly illustrate transmission inference? Outbreak clusters are often misread — the worked example must model correct interpretation, not intuitive but wrong conclusions.
    - Are the datasets representative of real outbreak diversity? Overly clean datasets do not prepare participants for the messy, ambiguous real-world data they will encounter.
    - Is the public health framing accurate — what can and cannot be concluded from phylogenetic data alone in a clinical context?

=== "Informatics Technical Developer — feasibility and build"

    - How long does the alignment and tree-building step take for the dataset size? (IQ-TREE on a 200-taxon SNP alignment is fast; on a whole-genome alignment it is not — pre-computed trees may need to be provided for participants to load and interpret, rather than build from scratch)
    - Is the visualisation tool (FigTree, iTOL, Microreact) accessible from the participant environment? If web-based, does the network at the host site allow outbound access to external URLs?
    - Are all input files (alignment, tree, metadata) pre-staged and in compatible formats? (Newick, Nexus, and Phylip formats are not interchangeable — the tool and the file format must match)
    - Has the full workflow been tested end to end, including the visualisation step? Visualisation tools frequently have version or browser compatibility issues that only appear when actually run.
    - Is there a simplified dataset available as a fallback if the full analysis takes longer than expected?

---

## RACI worked examples

### Example A — Informatics environment for a variant-calling practical

| RACI | Role | Responsibility |
|------|------|----------------|
| **R** | Informatics Technical Developer | Builds the compute environment — installs tools, loads datasets, configures user accounts, tests that everything runs without errors. |
| **A** | Informatics Training Lead | Validates the environment from a domain perspective — runs through the pipeline as a learner would, confirms the tools are the right versions, the datasets are appropriate, and the expected outputs are correct. Signs off that it is fit for delivery. This is expert validation, not development. |
| **C** | Education Developer(s) | Confirms that the environment supports the learning activities as designed — the technical setup should match the session plan. |

### Example B — Lab practical on CRISPR gene editing — protocol review

| RACI | Role | Responsibility |
|------|------|----------------|
| **R** | Lab Technical & Operations Developer | Develops the step-by-step protocol, tests it, documents it, and maintains the SOP. This is technical build work. |
| **A** | Lab Training Lead | Reviews the protocol with domain expertise — assesses safety, checks that the methodology is current and sound, confirms the level of complexity is appropriate for the learner group. Their sign-off is a domain expert quality gate. They are not co-writing the SOP. |
| **C** | Education Developer(s) | Consulted on whether the practical fits the overall course structure and learner flow — not on the science. |

!!! success "The core distinction"
    Training Leads are domain experts in the service of educational quality assurance. Their expertise is what gives them the authority to say 'this is current, this is valid, this is appropriate for teaching'. That is their value — not building or designing, but confirming that what has been built or designed meets the standard required for delivery.
