# The Brief-to-Build Handoff

A common source of friction in learning design teams is the assumption that technical roles need scientific expertise, or that educational roles need to understand technical infrastructure. In practice, neither is true — but it requires clean handoffs to work. This appendix maps where educational ownership ends and technical ownership begins at each major stage of the pipeline.

!!! abstract "Key principle"
    Education Developers own the **intent** (what learners need to know and do, and why). Technical Developers own the **implementation** (how that is built, hosted, and delivered). Training Leads hold the **quality gate** — they do not do either.

---

## 1. From needs analysis to design brief

Education Developers translate stakeholder needs into a learning design specification: learning outcomes, audience profile, format rationale, and assessment approach. This brief is what the rest of the team works from. Technical leads do not need scientific expertise to do their job — they need a clear brief. The Education Developer is responsible for making that brief scientifically accurate and pedagogically sound.

| Who owns it | What they produce | Who receives it | What they do with it |
|-------------|-------------------|-----------------|----------------------|
| Education Developer | Learning design brief (outcomes, audience, format, assessment) | Technical Developer / Digital Learning Dev | Builds or configures the platform/environment to match the spec |
| Education Developer | Content scripts or storyboards defining learning intent | Digital Learning Developer | Applies instructional design expertise to shape the digital experience, then produces video, interactive, or multimedia — the DLD is not simply executing a script but is accountable for how it works as digital learning |
| Education Developer | SME-reviewed content | Technical Developer | Uploads, structures, or integrates into the LMS or platform |

!!! warning "What this means in practice"
    If a Technical Developer has to make a scientific or pedagogical judgement call because the brief is incomplete, the handoff has broken down. The fix is always upstream — a better brief, not broader technical expertise.

---

## 2. From curriculum design to technical environment

When a programme requires a specific technical environment — a computational cluster, wet lab setup, or specialist software — the Education Developer specifies the learning requirements ('learners need to run X pipeline on Y data') and the Technical Developer determines how to provision it. The Training Lead validates that the environment meets the learning intent, but does not build it.

| Who owns it | What they produce | Who receives it | What they do with it |
|-------------|-------------------|-----------------|----------------------|
| Computational & Data ED / Lab ED | Technical environment requirements (what learners must be able to do in the environment) | Informatics Technical Dev / Lab Technical Dev | Provisions, configures, and tests the environment |
| Training Lead (A) | Sign-off: does the environment meet the learning requirements? | Technical Developer | Makes any adjustments flagged at sign-off |

!!! info "Boundary note"
    The Informatics Training Lead does not configure lab infrastructure. The Lab Training Lead does not configure computational & data environments. Cross-domain technical work is N/A for both Leads — it belongs to the relevant Technical Developer.

---

## 3. From assessment design to platform configuration

Assessment design (what the question is, what a good answer looks like, how it is marked) is owned by the Education Developer, ideally in consultation with the relevant Training Lead for scientific accuracy. Configuring the assessment in the LMS or platform is a separate, technical task.

| Who owns it | What they produce | Who receives it | What they do with it |
|-------------|-------------------|-----------------|----------------------|
| Education Developer | Assessment specification (questions, marking scheme, pass criteria, instructions) | Digital Learning Developer / Technical Dev | Configures the assessment in the LMS or platform |
| Training Lead (C) | Scientific accuracy check on assessment content | Education Developer | Revises content before it goes to technical build |
