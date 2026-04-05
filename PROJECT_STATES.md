# CDCF Project States

| | |
|---|---|
| **Version** | v0.1 (draft for community review) |
| **Status** | Working draft — pending publication to foundation website |
| **Scope** | All projects submitted to or hosted within the CDCF ecosystem |
| **Relationship** | Companion to [CDCF Project Vetting Criteria v0.1](https://github.com/CatholicOS/foundation-docs/blob/main/ai-governance/ai-vetting-criteria.md) |
| **Origin** | CDCF board and advisory council review session, Wednesday, March 11, 2026 |

---

## Origin of This Document

This document captures decisions and language confirmed during the CDCF board and advisory council review of the governance framework on Wednesday, March 11, 2026. Every decision in the table below derives directly from that session.

| Decision | Source |
|---|---|
| Change scope from "AI governance" to "project governance" — AI tools are among the projects vetted, not the only ones | Fr. John R. D'Orazio, Vice Chair and Lead Developer |
| The Church needs one shared meaning of "vetted" that works everywhere, from the Holy See down to a rural parish — this constraint originated the two-gate model | Fr. John R. D'Orazio, Vice Chair and Lead Developer |
| Framework is versioned and iterable — publish after review period, revise based on community feedback | Fr. John R. D'Orazio, Vice Chair and Lead Developer |
| Gate 1 = the why (theological/mission alignment); Gate 2 = the how (technical/operational deployment) | Diglio Simoni, Technical Advisory Council |
| Gate 1 is CDCF's differentiator from secular incubators — "not everything that can be done should be done" | Diglio Simoni, Technical Advisory Council |
| CDCF is not providing church oversight — it means committed Catholics across disciplines have reviewed a project against defined benchmarks | Taylor Black, President |
| Projects in the ecosystem do not all need to go through vetting — make project states explicit | Taylor Black, President |
| Use "states" not "stages" — a project can remain in Experimental indefinitely and still provide community value | Taylor Black, President |
| If CDCF does its job, 10,000 developers will engage with these governance standards — project states must be clear enough to scale | Taylor Black, President |
| Framework endorsed — "This is fantastic, faithful and technical work, right in line with the mission of CDCF" | Taylor Black, President; Andrew DeBerry, Treasurer |
| CDCF sets itself apart by providing not only the how but the why | Eugenio Zucal, Secretary |
| Three-tier articulation: exploratory → first review (incubation) → second review (active/endorsed) | Mark Julius Banasihan, Technical Advisory Council |
| Labels "Experimental" and "Incubating" make status visible without slowing early innovation | Mark Julius Banasihan, Technical Advisory Council |

---

## Why CDCF Project Review Differs from Secular Incubators

Fr. John R. D'Orazio identified the design constraint that produced the two-gate model: the Church needs one shared meaning of "vetted" that works everywhere, from the Holy See down to a rural parish. Diglio Simoni confirmed the resulting differentiator against Apache and other secular incubators on March 11, 2026.

| | Gate 1 | Gate 2 |
|---|---|---|
| **Question** | Should the Church use this tool at all? | If yes, how should it be deployed responsibly? |
| **Type** | Theological / mission alignment | Operational / technical deployment |
| **Primary council** | Ecclesial Advisory Council | Technical Advisory Council |
| **Grounded in** | Magisterial teaching, Canon Law, Catholic Social Teaching | Engineering standards, deployment governance, subsidiarity compatibility |
| **Apache equivalent** | No equivalent — CDCF's specific contribution | Closely maps to Apache Software Foundation incubation criteria |
| **Vetting criteria** | C1 Mission Alignment · C2 Human Accountability · C3 Transparency · C4 Independent Validation · C5 Subgroup Performance · C6 Deployment Governance | C7 Documentation and Data Stewardship · C8 Governance, Maintenance, and Subsidiarity Compatibility |

The manifesto states the mission directly: "Our mission is to aggregate, vet, and communalize these gifts." Project states operationalize that sequence. Aggregate covers Experimental. Vet covers Incubating. Communalize covers Active.

---

## The Three Project States

### State Definitions

| State | Definition | Duration | Vetting Applied | CDCF Endorsement |
|---|---|---|---|---|
| **Experimental** | Part of the CDCF ecosystem for community collaboration. No formal review. No endorsement. | Indefinite — no expectation of progression | None | None |
| **Incubating** | Has satisfied all six Gate 1 criteria. Mission alignment and theological threshold confirmed. Under active development toward Gate 2. | Active development period | Gate 1 — all six criteria required | Theological and mission alignment confirmed |
| **Active** | Has satisfied Gate 2 while maintaining full Gate 1 compliance. Meets full deployment governance requirements. | Ongoing — requires sustained maintenance and named accountability | Gate 1 + Gate 2 — all eight criteria required | Full endorsement — recommended for Catholic institutional deployment |

---

### What Each State Means in Practice

| | Experimental | Incubating | Active |
|---|---|---|---|
| **For contributors** | Build, collaborate, iterate freely. No review requirements. | Gate 1 cleared. Develop with Gate 2 requirements in view. | Represents the foundation. Maintenance, version control, vulnerability response, and named accountability required. |
| **For Catholic institutions** | Apply your own discernment. No CDCF review has occurred. | Gate 1 satisfied — theological threshold met. Gate 2 gaps remain. Evaluate accordingly. | Recommended for institutional deployment. A diocesan technology director could deploy this without access to the original authors within 90 days. |
| **For the aggregator** | Catalogued as community work in progress. | Catalogued as under active CDCF review. | Catalogued as foundation-endorsed. |
| **Hackathon projects** | Correct home for hackathon and prototype work. | Entered once maturity warrants formal review. | Entered once full deployment readiness is established. |

---

### Gate 2 Subsidiarity Requirement

Criterion 8 requires that every Active project remain configurable at the parish, diocesan, or institutional level without a central authority absorbing local control. This derives from four sources.

| Source | Provision |
|---|---|
| CDCF Bylaws, Article I Section 2 | Subsidiarity listed as a governing organizational principle under the ethical technology and AI purpose clause |
| CDCF Manifesto (translating Belloc) | "The purpose of the foundation is to support cooperation among Church institutions in maintaining a shared digital infrastructure — preserving each institution's independent ability to use, contribute to, and govern its own data and tools — without centralizing ownership or control beyond what is necessary for sustainability." |
| *Catechism of the Catholic Church* §1894 | "No larger body may take over the legitimate initiative and responsibility of a smaller one." |
| *Antiqua et Nova* §42 | The responsibility for managing AI wisely "pertains to every level of society, guided by the principle of subsidiarity." |

A project that functions only under conditions of centralized administration fails Criterion 8 and does not reach Active status.

---

## Current CDCF Projects by State

The four projects currently listed on catholicdigitalcommons.org carry the label "Incubating" as a descriptive placeholder that predates the formal vetting framework. The vetting criteria document now provides the definition of what Incubating formally requires. These projects have not yet been evaluated against the Gate 1 criteria. The table below reflects their current site label and the formal vetting status as of March 2026.

| Project | Type | Site Label | Formal Vetting Status | Notes |
|---|---|---|---|---|
| Catholic Semantic Canon | Data / Ontology | Incubating | Pre-vetting | Long-term ontology project — no defined endpoint. Continues to evolve across versions. Diglio Simoni is the primary contributor. |
| OntoKit | API | Incubating | Pre-vetting | Collaborative OWL ontology curation API. Authentication layer in development. |
| Bible API | API | Incubating | Pre-vetting | Fr. John R. D'Orazio is the author. Documentation in progress. |
| Liturgical Calendar API | API | Incubating | Pre-vetting | Fr. John R. D'Orazio is the author. Authentication layer completion required before documentation begins. |

The vetting criteria document provides the pathway for any of these projects to move from pre-vetting to formally Incubating status under Gate 1.

---

## Relationship to Existing Documents

| Document | Role | Relationship to This Document |
|---|---|---|
| [CDCF Project Vetting Criteria v0.1](https://github.com/CatholicOS/foundation-docs/blob/main/ai-governance/ai-vetting-criteria.md) | Primary policy document — defines all eight criteria in full | Defines *what* is evaluated at each gate. This document defines *when* those criteria apply. |
| [Fragmented Catholic AI Governance](https://github.com/CatholicOS/foundation-docs/blob/main/ai-governance/fragmented-catholic-ai-governance.md) | Research memo — documents the fragmentation problem | Provides the empirical foundation for why a shared project states framework is urgent. |
| [Governance-as-Code for Catholic AI](https://github.com/CatholicOS/foundation-docs/blob/main/ai-governance/governance-as-code-catholic-ai.md) | Research memo — machine-readable deployment governance | Describes the technical implementation the Active state is designed to grow into. |
| CDCF Manifesto | Founding document — theological and mission direction | Source of the aggregate / vet / communalize mission that project states operationalize. |
| CDCF Bylaws, Article I Section 2 | Legal instrument — organizational purposes | Source of subsidiarity as a binding organizational principle. |

---

## Invitation to Iterate

| Council | Appropriate scrutiny |
|---|---|
| Ecclesial Advisory Council | Theological and canonical basis for state transitions — particularly the Gate 1 criteria that define the formal Incubating threshold |
| Technical Advisory Council | Gate 2 deployment criteria — whether the Active state requirements hold in real diocesan, health system, and educational institution environments |
| Board | Whether the three-state model and the pre-vetting / formally-vetted distinction accurately reflects the organizational intent confirmed on March 11, 2026 |

Contributions, challenges, and proposed revisions are welcome via pull request or issue on the [CatholicOS GitHub](https://github.com/CatholicOS).

*Drafted in response to the CDCF board and advisory council review session, Wednesday, March 11, 2026. Decisions by Fr. John R. D'Orazio, Taylor Black, Andrew DeBerry, Eugenio Zucal, and Diglio Simoni are documented above. Grounded in the CDCF Manifesto, CDCF Bylaws, and CDCF Project Vetting Criteria v0.1.*
