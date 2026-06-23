# Stage 6 — Quality Assurance & Sign-off

This stage covers scientific accuracy reviews, learning design quality reviews, and technical readiness sign-off before a course runs.

!!! info "Domain-specific reviews"
    Scientific accuracy review is conducted separately by domain. The Informatics Training Lead reviews informatics elements; the Lab Training Lead reviews lab elements. For training events with both element types, both reviews are conducted independently — the Informatics Lead does not review lab content, and the Lab Lead does not review informatics content.

---

## Scientific accuracy review of course materials

| RACI | Role | Responsibility |
|------|------|----------------|
| **A** | Informatics Training Lead (for informatics elements) / Lab Training Lead (for lab elements) | Accountable — they are the scientific authority for their domain. Their sign-off is the quality gate. |
| **R** | Education Developer(s) | Responsible for collating materials and managing the review process. |
| **C** | Subject Matter Experts | Consulted where the Training Lead wants a second scientific opinion. |
| **I** | Head of LDD | Informed that sign-off has been given. |

---

## Learning design quality review

| RACI | Role | Responsibility |
|------|------|----------------|
| **A/R** | Education Developer(s) | Accountable for the quality of the instructional design — this is their professional domain. |
| **C** | Informatics Training Lead (for informatics elements) / Lab Training Lead (for lab elements) | Consulted — they can flag if something won't work in practice for their learner group, but learning design methodology is not their domain. |
| **I** | Head of LDD | Informed; may review at programme level. |

---

## Two review lenses: what each role is looking for

When protocols and practicals are reviewed before a training event runs, two separate reviews are needed. Conflating them, or assuming one covers both, is a common source of gaps. The Technical Developer and the Training Lead each review the same material but are looking for entirely different things.

=== "Technical Developer reviews for: feasibility and operational flow"

    - Will this work technically in the time allocated? Does the step timing add up across the session?
    - Does the output of step A become the correct input for step B? Are dependencies in the right order?
    - Will the tool, software version, or instrument handle this dataset, sample volume, or file size?
    - Is the environment or equipment configured to do what the protocol assumes? Are there hardware constraints?
    - Is anything in the protocol technically ambiguous — steps that could be interpreted multiple ways and cause participant error?
    - Are there any operational blockers: reagents not yet sourced, equipment not yet booked, datasets not yet loaded?

=== "Training Lead reviews for: scientific accuracy and appropriateness"

    - Is the science correct? Are the protocols, methods, and expected outputs scientifically sound?
    - Is this technique, tool, or approach appropriate for this audience and their level of prior knowledge?
    - Are the expected results what the science would actually produce? Will participants see what the session claims they will see?
    - Is the level of complexity appropriate — not so simple it is trivial, not so advanced participants cannot engage?
    - Are there safety considerations that have not been accounted for?
    - Does this content accurately represent current practice in the field, or is it outdated?

!!! danger "Both reviews are required — neither replaces the other"
    - A protocol can be scientifically correct but operationally undeliverable in the time available — the Technical Developer catches that; the Training Lead would not.
    - A protocol can be technically executable but scientifically wrong for this audience or context — the Training Lead catches that; the Technical Developer would not.
    - The Education Developer holds the brief that connects both: the learning outcomes, the session plan, and the overall design. If either review raises a change, the Education Developer assesses the impact on the design and manages the resolution.

---

## Technical readiness sign-off before a training event runs

| RACI | Role | Responsibility |
|------|------|----------------|
| **A** | Informatics Training Lead (for informatics elements) / Lab Training Lead (for lab elements) | Accountable that the full learner experience — not just the technical parts — is ready. This is the Lead's assurance function. |
| **R** | Informatics Technical Developer (for informatics elements) / Lab Technical & Operations Developer (for lab elements) | Responsible for confirming the technical components are working and tested. |
| **C** | Education Developer(s) | Consulted — confirms learner-facing materials are aligned with the environment. |
| **I** | Head of LDD | Informed that the course is cleared to run. |
