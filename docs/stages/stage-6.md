# Stage 6 — Quality Assurance & Sign-off

This stage covers domain accuracy reviews, learning design quality reviews, and technical readiness sign-off before a course runs.

!!! info "Domain-specific reviews"
    Reviews are conducted separately by domain. The Informatics Training Lead reviews computational & data elements; the Lab Training Lead reviews lab elements. For training events with both element types, both reviews are conducted independently. This applies to all content regardless of format — in-person, virtual or online.

---

## Domain accuracy review of course materials

| RACI | Role | Responsibility |
|------|------|----------------|
| **A** | Informatics Training Lead (for computational & data elements) / Lab Training Lead (for lab elements) | Accountable — they are the domain authority for their area. Their sign-off is the quality gate. For the Informatics Training Lead this covers computational tools, data approaches and analytical methods; for the Lab Training Lead this covers experimental methods, safety and practical validity. |
| **R** | Education Developer(s) | Responsible for collating materials and managing the review process. |
| **C** | Subject Matter Experts | Consulted where the Training Lead wants a second opinion on specific technical or scientific detail. |
| **I** | Head of LDD | Informed that sign-off has been given. |

---

## Learning design quality review

This review covers two distinct dimensions — overall instructional design, and the quality of the digital/online learning experience where relevant.

### Instructional design quality (all formats)

| RACI | Role | Responsibility |
|------|------|----------------|
| **A/R** | Education Developer(s) | Accountable for the quality of the overall instructional design — learning outcomes, curriculum structure, assessment, content organisation. This applies across all delivery formats. |
| **C** | Informatics Training Lead (for computational & data elements) / Lab Training Lead (for lab elements) | Consulted — they can flag if the design won't work in practice for their learner group, but learning design methodology is not their domain. |
| **I** | Head of LDD | Informed; may review at programme level. |

### Digital instructional design quality (digital and online content only)

| RACI | Role | Responsibility |
|------|------|----------------|
| **A** | Digital Learning Developer | Accountable for the instructional design quality of digital and online content — does this work as a digital learning experience? Covers chunking, interactivity, navigation, pacing, multimedia treatment, accessibility and platform suitability. This is the DLD's specialist domain; the ED does not hold A here for the digital dimension. |
| **R** | Education Developer(s) | Responsible for providing materials and ensuring digital content aligns with the overall learning intent and outcomes. |
| **I** | Head of LDD | Informed; brought in if there is a significant quality concern. |

!!! info "Why two reviews?"
    The ED's review asks: does this content achieve the learning outcomes and follow sound instructional principles? The DLD's review asks: does this work as a digital experience — is it appropriately structured, interactive, accessible and effective on screen? A course can pass one review and fail the other. Both are required before digital content is signed off.

---

## Two review lenses: what each role is looking for

Two separate reviews are needed before any training event runs — whether in-person, virtual or online. The Technical Developer and the Training Lead each review the same material but are looking for entirely different things.

=== "Technical Developer reviews for: feasibility and operational flow"

    - Will this work technically in the time allocated? Does the step timing add up across the session?
    - Does the output of step A become the correct input for step B? Are dependencies in the right order?
    - Will the tool, software version, or instrument handle this dataset, sample volume, or file size?
    - Is the environment or equipment configured to do what the protocol assumes? Are there hardware or infrastructure constraints?
    - Is anything technically ambiguous — steps that could be interpreted multiple ways and cause participant error?
    - Are there any operational blockers: reagents not yet sourced, equipment not yet booked, datasets not yet loaded, virtual environments not yet provisioned?

=== "Training Lead reviews for: domain accuracy and appropriateness"

    **Informatics Training Lead checks:**

    - Are the computational tools, data types and analytical approaches correct and current for this topic?
    - Is the tool or pipeline choice appropriate for this audience's level — not too advanced, not too simplistic?
    - Are the expected outputs what the analysis would actually produce?
    - Does the content reflect current practice in the field, or is it outdated?
    - Is the level of computational complexity appropriate for the learner group?

    **Lab Training Lead checks:**

    - Are the experimental methods, protocols and expected outputs scientifically sound?
    - Is the technique appropriate for this audience and their level of prior knowledge?
    - Are there safety considerations that have not been accounted for?
    - Does the content accurately represent current laboratory practice?
    - Is the level of practical complexity appropriate — and does this hold for virtual/simulated versions as well as physical practicals?

!!! danger "Both reviews are required — neither replaces the other"
    - Content can be domain-accurate but operationally undeliverable — the Technical Developer catches that; the Training Lead would not.
    - Content can be technically executable but wrong for this audience or context — the Training Lead catches that; the Technical Developer would not.
    - The Education Developer holds the brief that connects both. If either review raises a change, the Education Developer assesses the impact on the design and manages the resolution.

---

## Technical readiness sign-off before a training event runs

| RACI | Role | Responsibility |
|------|------|----------------|
| **A** | Informatics Training Lead (for computational & data elements) / Lab Training Lead (for lab elements) | Accountable that the full learner experience — not just the technical parts — is ready. This is the Lead's assurance function and applies to in-person, virtual and online events equally. |
| **R** | Informatics Technical Developer (for computational & data elements) / Lab Technical & Operations Developer (for lab elements) | Responsible for confirming the technical components are working and tested. |
| **C** | Education Developer(s) | Consulted — confirms learner-facing materials are aligned with the environment. |
| **I** | Head of LDD | Informed that the course is cleared to run. |
