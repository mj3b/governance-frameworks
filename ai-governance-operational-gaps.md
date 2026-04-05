# CDCF AI Governance: Five Operational Gaps

| | |
|---|---|
| **Document type** | Research memo |
| **Status** | Working draft — U.S.A. C-DART 1 discussion |
| **Relationship** | Supplementary to [CDCF Project Vetting Criteria v0.1](https://github.com/CatholicOS/foundation-docs/blob/main/ai-governance/ai-vetting-criteria.md) and [CDCF Project States v0.1](https://github.com/CatholicOS/foundation-docs/blob/main/PROJECT_STATES.md) |

---

## Table of Contents

1. [Purpose](#purpose)
2. [Gap 1 — Model Drift Has No Re-Vetting Trigger](#gap-1--model-drift-has-no-re-vetting-trigger)
3. [Gap 2 — No Incident Response Protocol](#gap-2--no-incident-response-protocol)
4. [Gap 3 — The Aggregator Is an Unvetted AI Tool Serving Governance Infrastructure](#gap-3--the-aggregator-is-an-unvetted-ai-tool-serving-governance-infrastructure)
5. [Gap 4 — Magisterial Sources Table Has No Maintenance Process](#gap-4--magisterial-sources-table-has-no-maintenance-process)
6. [Gap 5 — Conflict of Interest Protocol Does Not Cover TAC or EAC Members](#gap-5--conflict-of-interest-protocol-does-not-cover-tac-or-eac-members)
7. [Strategic Context: CDCF's Position in the Catholic AI Ecosystem](#strategic-context-cdfcs-position-in-the-catholic-ai-ecosystem)
8. [Gap Summary and Ownership Table](#gap-summary-and-ownership-table)
9. [Bibliography](#bibliography)

---

## Purpose

The CDCF Project Vetting Criteria v0.1 establishes what "vetted" means for projects submitted to the foundation. The criteria are rigorous at the point of evaluation. Five governance gaps exist in what happens before, during, and after that evaluation. Each gap is documented here with a specific failure scenario, the criteria or bylaws provision affected, a named owner within the existing CDCF governance structure, and a proposed resolution.

None of these gaps require new criteria. Four require process documents. One requires a bylaws amendment.

---

## Gap 1 — Model Drift Has No Re-Vetting Trigger

### The Problem

The vetting criteria evaluate a tool at a point in time. Most AI tools submitted to CDCF will not be built from scratch — they will wrap or depend on foundation models from OpenAI, Anthropic, Google, or equivalent providers. Those foundation models change when vendors release updates. A tool that clears all eight CDCF criteria in March 2026 may behave differently by September 2026 after a vendor updates their underlying model without notice to the tool's developer or to CDCF.

This is not theoretical. Catholic Answers launched "Father Justin" in April 2024 — an AI chatbot that presented itself as a priest-figure and claimed it could administer sacraments. The system required withdrawal within days.[1] That failure would have occurred regardless of prior vetting if the tool's underlying model had been updated to cross the sacramental boundary after initial review. The vetting criteria document cites this case explicitly under Criterion 1 as the boundary condition a shared standard would have identified before a single line of code shipped. The same failure mode can occur post-vetting when model behavior shifts.

### What Is Missing

The current framework has no definition of what constitutes a material change in a tool's behavior. It has no mechanism for triggering re-evaluation when a vendor updates their underlying model. It has no process for moving an Active project back to Incubating or Experimental status. A tool can hold Active status indefinitely after initial Gate 2 clearance.

### Magisterial Grounding

*Antiqua et Nova* §42 establishes that the responsibility for managing AI wisely "pertains to every level of society." Active status implies ongoing responsibility, not a single point of clearance. Canon 1609's pattern of deliberation with the capacity to revise judgments applies to governance decisions, not only initial ones.

### Proposed Resolution

A Re-Vetting Trigger Policy document defining three conditions that require re-evaluation of an Active project:

| Trigger | Description |
|---|---|
| **Foundation model update** | The tool's underlying model is updated by the vendor — any version change above a defined threshold |
| **Behavioral deviation report** | A verified report from a deploying institution that the tool is producing outputs outside the scope documented at Gate 2 |
| **Criterion 1 boundary proximity** | Any output approaching the sacramental simulation, authoritative teaching misrepresentation, or clerical identity boundaries defined in Criterion 1 |

Re-evaluation is not a full Gate 1 and Gate 2 review. It is a targeted review of the criteria most likely affected by the change, conducted by the TAC with EAC input on Criterion 1 boundary questions.

### Named Owner

Technical Advisory Council. Diglio Simoni holds a US patent for semantic test suite reduction — the discipline of defining exactly which tests are required to verify system behavior after a change. That expertise maps directly onto defining what constitutes a material behavioral deviation requiring re-review.

---

## Gap 2 — No Incident Response Protocol

### The Problem

The vetting framework endorses tools. It has no documented procedure for what happens when an endorsed tool causes harm in a Catholic institutional context.

Three documented failure scenarios in contexts directly relevant to CDCF:

**Scenario A — Catechetical harm.** A Gate 2 Active catechetical AI deployed by a diocesan schools office produces doctrinally incorrect content about a sacrament. Students receive the content before a teacher identifies the error. The content spreads through parent WhatsApp groups.

**Scenario B — Healthcare bias.** A Gate 2 Active clinical decision support tool deployed at a CommonSpirit facility produces triage recommendations that disproportionately underserve a minority patient population — the bias pattern documented in COMPAS criminal sentencing (cited in the vetting criteria under Criterion 3) reproduced in a Catholic healthcare context.[2]

**Scenario C — Data breach.** A Gate 2 Active parish management tool suffers a breach exposing sacramental records — the highest-sensitivity data category under Criterion 7's data stewardship requirements.

In all three scenarios, the current framework has no escalation path, no defined communication protocol to institutions that deployed the tool, no process for suspension of Active status, and no documented authority for who makes the suspension decision.

### What Is Missing

Taylor Black clarified on March 11, 2026: CDCF endorsement is not church oversight — it means committed Catholics across disciplines have reviewed a project against defined benchmarks. That clarification creates a gap between endorsement and ongoing accountability that an incident response protocol must bridge.

### Proposed Resolution

An Incident Response Protocol document covering four phases:

| Phase | Action |
|---|---|
| **Detection** | Defined reporting channels for deploying institutions, community members, and affected parties to submit verified incident reports |
| **Assessment** | TAC review within 72 hours to determine whether the incident constitutes a material behavioral deviation under Gap 1 criteria; EAC review for Criterion 1 boundary incidents |
| **Response** | Three possible outcomes: Active status maintained with documented mitigation, Active status suspended pending re-vetting, Active status revoked with documented rationale |
| **Communication** | Defined protocol for notifying all institutions that have deployed the tool, including the nature of the incident, the foundation's response, and recommended institution-level actions |

### Named Owner

Andrew DeBerry (Treasurer) as primary author. He helped draft the Department of Defense's responsible AI principles and launched AI governance and youth protection products at Meta. He has institutional muscle memory for exactly this type of protocol. Fr. Michael Baggot (EAC) for oversight of doctrinal incident classification. Taylor Black (President) for final suspension/revocation authority as a board-level decision.

---

## Gap 3 — The Aggregator Is an Unvetted AI Tool Serving Governance Infrastructure

### The Problem

Fr. John R. D'Orazio described an AI-powered web scraper on March 31, 2026 that will scour for news, events, and projects related to Catholicism and technology to build a knowledge base and aggregator. That scraper is itself an AI tool. It will:

- Make algorithmic decisions about what Catholic technology content to include or exclude
- Apply editorial judgment about what constitutes relevant Catholic technology news
- Build a knowledge base that will inform how the Catholic technology ecosystem understands itself and its participants
- Serve as the primary discovery mechanism for projects seeking CDCF incubation

The aggregator is governance infrastructure. It shapes what projects become visible to CDCF, which organizations enter the vetting pipeline, and how the broader Catholic digital community perceives what is happening in Catholic AI. An aggregator that systematically includes or excludes certain types of projects — not from malice but from training data bias or scope definition errors — distorts the governance process it is designed to serve.

The Vatican warned explicitly in January 2025 that AI poses serious risks from "biased or fabricated information" and "fake news," and that those who produce and share AI-generated content must "exercise diligence in verifying the truth of what they disseminate."[3]

### What Is Missing

The aggregator has not been submitted for Gate 1 review. CDCF is building an AI tool to serve its own governance infrastructure without subjecting that tool to its own governance process.

### Proposed Resolution

The aggregator passes through a streamlined Gate 1 review before deployment, with three specific questions replacing the full six-criterion Gate 1 process:

| Gate 1 Question Applied to the Aggregator | Why It Applies |
|---|---|
| C1 Mission Alignment: Does the aggregator's scope definition align with CDCF's stated mission? | The aggregator defines what "Catholic technology" means algorithmically. That definition must reflect the mission. |
| C2 Human Accountability: Is there a named human reviewer responsible for aggregator outputs before they enter the knowledge base? | Algorithmic curation without human review is the exact failure mode Criterion 2 exists to prevent. |
| C3 Transparency of Scope: Is the aggregator's inclusion/exclusion logic documented and reviewable? | Institutions and projects need to know why they appear or do not appear in the knowledge base. |

### Named Owner

Fr. John R. D'Orazio as builder; TAC for the technical Gate 1 assessment; EAC for Criterion 1 mission alignment review.

---

## Gap 4 — Magisterial Sources Table Has No Maintenance Process

### The Problem

The Magisterial Grounding table in the vetting criteria document lists eight sources as of March 2026. New Magisterial AI documents are being issued at a rate the current framework cannot absorb without a defined maintenance process. Between the framework's drafting and April 2026:

| Document | Body | Date |
|---|---|---|
| *Antiqua et Nova* | Dicastery for the Doctrine of the Faith and Dicastery for Culture and Education | January 28, 2025 |
| USCCB Joint Letter on AI Principles and Priorities | United States Conference of Catholic Bishops | June 2025 |
| Address to Builders AI Forum | Pope Leo XIV | November 3, 2025 |
| Address on Children and Adolescents in the Age of AI | Pope Leo XIV | November 13, 2025 |
| Address on AI and Care for Our Common Home | Pope Leo XIV | December 5, 2025 |
| Vatican City State AI Guidelines | Pontifical Commission for Vatican City State | Effective January 1, 2026 |
| Message for the 60th World Day of Social Communications | Pope Leo XIV | January 2026 |

Vatican City State's guidelines established a five-person AI commission to prepare laws, provide opinions on AI systems, and monitor implementation.[4] That commission is now producing regulatory documents that will affect Catholic institutions globally. The vetting criteria must track that output or they will cite outdated Magisterial authority while a more current standard exists.

New documents that cite earlier documents as their authority — and then update or extend that authority — can silently invalidate criteria grounded in the earlier documents if no one is monitoring the chain.

### What Is Missing

No defined monitoring responsibility. No update authority. No version trigger connecting new Magisterial documents to a criteria review cycle.

### Proposed Resolution

A Magisterial Sources Monitoring Protocol assigning:

| Role | Responsibility |
|---|---|
| **Primary monitor** | Fr. Michael Baggot (EAC) — Associate Professor of Bioethics at Regina Apostolorum, member of the Magisterium AI scholarly advisory board, contributor to *Emerging Issues in Catholic Bioethics* (Springer, 2026). Reviews new Vatican and episcopal conference AI documents within 30 days of publication. |
| **European episcopal monitor** | Fr. Charbel Bteich (EAC) — Vice General Secretary of the Council of European Bishops' Conferences (CCEE) since November 2024. Monitors CCEE member conference AI governance developments. |
| **Update authority** | EAC proposes table updates; board approves; Fr. John R. D'Orazio publishes new version to the repo. |
| **Trigger threshold** | Any new Magisterial document that introduces new AI-specific guidance, modifies an existing principle, or establishes a new institutional structure (such as the Vatican City State AI commission) triggers a 60-day criteria review cycle. |

---

## Gap 5 — Conflict of Interest Protocol Does Not Cover TAC or EAC Members

### The Problem

CDCF Bylaws Article VIII requires board members and committee members to disclose conflicts and abstain from votes where a conflict exists. The provision does not explicitly extend to TAC or EAC members reviewing submitted projects.

The TAC includes members with active professional relationships at organizations that are potential CDCF project submitters or whose clients are:

| TAC Member | Employer / Organization | Potential Conflict Scenario |
|---|---|---|
| Taylor Black | Microsoft Office of the CTO | Microsoft or a Microsoft partner submits a project |
| Randy Danielson | Microsoft Azure Edge | Same as above |
| Gabriel Dorta | Former Microsoft and Accenture | Former employer or its clients submit a project |
| Diglio Simoni | Wipro (AI initiatives for Apple, T-Mobile, SABIC) | Wipro client or competitor submits a project |
| Andrew DeBerry | Former Google X, AWS, Meta | Former employer ecosystems submit a project |

This is not a hypothetical risk. The Builders AI Forum Vatican conference in November 2025 included representatives from Microsoft, Palantir Technologies, and Goldman Sachs — all organizations with Catholic institutional relationships and potential technology project submissions.[5] Microsoft has signed the Rome Call for AI Ethics. A Microsoft-affiliated project submitted to CDCF for vetting would create an undocumented conflict of interest for at least two TAC members simultaneously.

The EAC carries an equivalent risk. Fr. Michael Baggot serves on the Magisterium AI scholarly advisory board. If Magisterium AI submits a project for CDCF Gate 1 review, Fr. Baggot would be reviewing a project from an organization he actively advises.

### What Is Missing

Bylaws Article VIII covers board and committee members. It does not explicitly name TAC and EAC members as covered parties in the context of project vetting reviews. The gap is one of scope, not of principle — the principle is already in the bylaws.

### Proposed Resolution

A two-paragraph addendum to Bylaws Article VIII extending the conflict of interest provision to TAC and EAC members participating in project vetting reviews:

- Any TAC or EAC member with a current or recent (within 24 months) professional relationship with a project submitter or its parent organization must disclose that relationship before the review begins.
- Disclosure is filed with the Secretary (Eugenio Zucal). The member abstains from voting on that project's vetting decision. They may provide technical input at the board's discretion.

### Named Owner

Eugenio Zucal (Secretary) owns the bylaws amendment process. The fix is a one-meeting board vote. The addendum does not require rewriting Article VIII — it requires a supplement of two paragraphs.

---

## Strategic Context: CDCF's Position in the Catholic AI Ecosystem

This gap is not a process document. It is a positioning question the board must answer.

The Builders AI Forum (BAIF) held its first Vatican conference in November 2025 with roughly 200 participants including software engineers, venture capital partners, Catholic media producers, bishops, and Vatican communications officials.[5] Magisterium AI is a live product with an institutional advisory board that includes Fr. Michael Baggot. Hallow has millions of users. The Rome Call for AI Ethics has been signed by Microsoft, IBM, and others.

CDCF has no documented position on how it relates to or differs from BAIF, Magisterium AI, or the Rome Call signatories. Three scenarios exist:

| Scenario | Risk |
|---|---|
| CDCF operates in isolation | Produces standards that duplicate or conflict with BAIF and Magisterium AI without coordination |
| CDCF is absorbed into BAIF | Loses the Gate 1 theological differentiation that the March 11, 2026 board session confirmed as CDCF's unique contribution |
| CDCF defines its relationship explicitly | Positions itself as the governance and commons infrastructure layer that BAIF's builder community and Magisterium AI's product ecosystem both need |

The third scenario is the one consistent with CDCF's founding documents. The manifesto's mission — aggregate, vet, and communalize — is a commons infrastructure mission, not a product mission. CDCF governs the ecosystem. BAIF builds inside it. Magisterium AI is a product that could be submitted for CDCF vetting.

That positioning requires a document. A one-page ecosystem positioning memo from the board that defines CDCF's relationship to adjacent Catholic AI organizations would close this gap and give the TAC and EAC clear framing for how to handle requests from those organizations.

---

## Gap Summary and Ownership Table

| Gap | Affected Document | Owner | Resolution Type | Urgency |
|---|---|---|---|---|
| 1 — Model drift, no re-vetting trigger | Vetting Criteria (all criteria) | Diglio Simoni, TAC | Process document | High — any Active project is currently at risk from silent vendor model updates |
| 2 — No incident response protocol | Vetting Criteria + Bylaws | Andrew DeBerry, Fr. Michael Baggot, Taylor Black | Process document | High — CDCF has Active projects pending; incident response must precede first deployment |
| 3 — Aggregator is unvetted AI | Vetting Criteria C1, C2, C3 | Fr. John R. D'Orazio, TAC, EAC | Streamlined Gate 1 review | High — aggregator development is active |
| 4 — Magisterial sources, no maintenance | Vetting Criteria (Magisterial Grounding table) | Fr. Michael Baggot, Fr. Charbel Bteich, EAC | Protocol document | Medium — 7 new documents issued since framework drafting |
| 5 — Conflict of interest, TAC/EAC uncovered | Bylaws Article VIII | Eugenio Zucal, Board | Bylaws addendum | Medium — resolves before any project from a TAC/EAC-affiliated organization enters vetting |
| Strategic — CDCF ecosystem positioning | None (does not exist) | Board | One-page positioning memo | Medium — required before BAIF, Magisterium AI, or Rome Call signatories engage with CDCF formally |

---

## Bibliography

1. "The Real Lesson Behind the 'Father Justin' AI Priest Debacle," *America*, April 26, 2024, https://www.americamagazine.org/faith/2024/04/26/father-justin-catholic-answers-ai-247808.

2. Julia Angwin, Jeff Larson, Surya Mattu, and Lauren Kirchner, "Machine Bias," *ProPublica*, May 23, 2016, https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing.

3. Dicastery for the Doctrine of the Faith and Dicastery for Culture and Education, *Antiqua et Nova: Note on the Relationship Between Artificial Intelligence and Human Intelligence* (Vatican City: Dicastery for the Doctrine of the Faith, January 28, 2025), https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_ddf_doc_20250128_antiqua-et-nova_en.html.

4. Vatican City State, Decree on the Use of Artificial Intelligence in Vatican City State, Pontifical Commission for Vatican City State, effective January 1, 2026, https://www.vaticanstate.va.

5. "Pope Leo XIV Urges Catholic Technologists to Spread the Gospel with AI," Catholic News Service, November 7, 2025, https://www.usccb.org/news/2025/pope-leo-xiv-urges-catholic-technologists-spread-gospel-ai.

6. "Vatican City State Puts AI Guidelines in Place," Catholic News Service, January 2025, https://www.usccb.org/news/2025/vatican-city-state-puts-ai-guidelines-place.

*Drafted by Mark Julius Banasihan, U.S.A. C-DART 1. April 2026. Submitted to CDCF for community review.*
