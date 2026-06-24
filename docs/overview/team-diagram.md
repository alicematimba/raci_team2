# Team Structure & Interactions

The diagram below shows how the roles in the Learning Design & Delivery team relate to each other across the shared pipeline — including normal working relationships and escalation routes.

```mermaid
flowchart TD
    HEAD["**Head of LDD**
    Portfolio owner · strategic decisions
    Final escalation point for all roles"]

    ITL["**Informatics Training Lead**
    Domain expert: computational & data
    Approves scientific quality"]

    ED["**Education Developer(s)**
    Owns design pipeline end-to-end
    Issues briefs · coordinates all roles"]

    LTL["**Lab Training Lead**
    Domain expert: wet lab
    Approves science & safety"]

    ITD["**Informatics Technical Dev**
    Builds computational environments"]

    DLD["**Digital Learning Developer**
    Online platforms & multimedia"]

    LTOD["**Lab Technical & Ops Dev**
    Develops lab protocols"]

    HEAD -->|commissions| ED
    HEAD -.->|consults| ITL
    HEAD -.->|consults| LTL

    ED -.->|seeks domain input| ITL
    ITL ==>|approves / signs off| ED
    ED -.->|seeks domain input| LTL
    LTL ==>|approves / signs off| ED

    ED -->|issues design brief| ITD
    ED -->|issues design brief| DLD
    ED -->|issues design brief| LTOD
    ITL -.->|quality gate| ITD
    LTL -.->|quality gate| LTOD

    ITD -. "escalates incident" .-> ITL
    LTOD -. "escalates incident" .-> LTL
    ITL -. "escalates if strategic" .-> HEAD
    LTL -. "escalates if strategic" .-> HEAD
    ED -. "escalates if scope/SME issue" .-> HEAD

    style HEAD fill:#4361ee,color:#fff,stroke:#2a44c4
    style ITL fill:#7b2d8b,color:#fff,stroke:#5a1a6a
    style ED  fill:#0a9396,color:#fff,stroke:#077679
    style LTL fill:#7b2d8b,color:#fff,stroke:#5a1a6a
    style ITD fill:#e76f51,color:#fff,stroke:#c4522e
    style DLD fill:#0a9396,color:#fff,stroke:#077679
    style LTOD fill:#e76f51,color:#fff,stroke:#c4522e
```

---

## How to read this diagram

Normal working relationships flow **downward** — from strategic decisions at the top, through design coordination in the middle, to technical build at the bottom.

Escalation routes (dotted arrows labelled "escalates") flow **upward** and are only triggered in specific circumstances:

- **Technical Developers → Training Leads** — when an incident occurs during delivery (e.g. environment fails, practical goes wrong). The Technical Developer fixes the technical problem; the Training Lead manages the learner situation and decides how to proceed.
- **Training Leads → Head of LDD** — when a stakeholder ask is strategically significant, or a scope disagreement cannot be resolved at team level.
- **Education Developer → Head of LDD** — when an SME relationship is senior or politically sensitive, or when a scope issue on a design brief cannot be resolved.

For the full detail on each role's responsibilities at each stage, see the [Pipeline Stages](../stages/stage-1.md).
