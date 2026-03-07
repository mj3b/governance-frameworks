# CDCF Project Vetting Criteria: AI Tools

> **Version:** v0.1 (draft for community review)

> **Scope:** AI-assisted tools submitted for CDCF incubation and graduation

> **Extensibility:** Scoped to AI tools. The underlying framework is designed for extension to software projects more broadly; a generalized version is anticipated in a subsequent release.

---

## Table of Contents

1. [Purpose and Rationale](#purpose-and-rationale)
2. [Gate 1: Incubation Acceptance](#gate-1-incubation-acceptance)
   - [Criterion 1: Mission Alignment and Canonical Scope](#criterion-1-mission-alignment-and-canonical-scope)
   - [Criterion 2: Human Accountability Architecture](#criterion-2-human-accountability-architecture)
   - [Criterion 3: Transparency of Scope and Operation](#criterion-3-transparency-of-scope-and-operation)
   - [Criterion 4: Independent Validation of Claimed Capabilities](#criterion-4-independent-validation-of-claimed-capabilities)
   - [Criterion 5: Subgroup Performance and Vulnerable Population Review](#criterion-5-subgroup-performance-and-vulnerable-population-review)
   - [Criterion 6: Deployment Governance Specification](#criterion-6-deployment-governance-specification)
3. [Gate 2: Graduation to Active CDCF Project Status](#gate-2-graduation-to-active-cdcf-project-status)
   - [Criterion 7: Documentation for Independent Deployment and Data Stewardship](#criterion-7-documentation-for-independent-deployment-and-data-stewardship)
   - [Criterion 8: Governance, Maintenance, and Subsidiarity Compatibility](#criterion-8-governance-maintenance-and-subsidiarity-compatibility)
4. [Grounding in Catholic Teaching and Canonical Tradition](#grounding-in-catholic-teaching-and-canonical-tradition)
5. [Relationship to the Broader Governance Research](#relationship-to-the-broader-governance-research)
6. [An Invitation to Iterate](#an-invitation-to-iterate)
7. [References](#references)

---

## Purpose and Rationale

Catholic institutions serve tens of millions of people across healthcare, education, social services, and parish life. They are actively evaluating and deploying AI tools to do this work more effectively, and they are doing so without a shared, canonical standard for what responsible Catholic deployment looks like. The consequence is fragmentation: dioceses, school systems, and Catholic Charities agencies operating under incompatible evaluation criteria for structurally identical use cases, with tools that touch sensitive populations entering production without a documented discernment process.

This document establishes what "vetted" means for AI tools accepted into the Catholic Digital Commons Foundation. Its foundational premise is practical and specific: **the humans inside a system determine whether the governance holds.** Policies, principles, and frameworks carry weight only when they are traceable to named individuals with real authority and real accountability. In Catholic institutional life, that premise has deep roots. The Church teaches that human intelligence is an essential aspect of being created in the image of God, and that technological innovation represents a participation in the divine act of creation. Because every design choice "expresses a vision of humanity," developers carry an obligation to build systems that "reflect justice, solidarity, and a genuine reverence for life" (Pope Leo XIV, Builders AI Forum, November 2025). These criteria translate that obligation into an operational standard that developers, dioceses, and ecclesial advisors can apply consistently.

The criteria are organized around two evaluation gates. **Gate 1** governs acceptance into incubation. **Gate 2** governs graduation to active CDCF project status. A project advances through Gate 2 only after satisfying Gate 1 in full.

---

## Gate 1: Incubation Acceptance

> All six criteria are required for incubation acceptance. A project satisfying five of six criteria remains in pre-submission dialogue until the sixth is resolved.

---

### Criterion 1: Mission Alignment and Canonical Scope

The tool must serve a purpose coherent with the Church's evangelizing mission and with Catholic Social Teaching's account of human dignity, the common good, and subsidiarity. Tools with the potential to serve any parish, diocese, school, or ministry facing a structurally similar need take priority over tools designed for a single institution's bespoke requirements.

**Canonical boundary conditions.** Certain AI applications fall outside the scope of CDCF endorsement regardless of technical quality. The doctrinal basis for these boundaries is precise. The Church distinguishes human intelligence, understood as a synthesis of *intellectus* (the intuitive grasp of truth) and *ratio* (discursive reasoning) belonging to a person composed of body and soul, from artificial statistical inference, which processes data without the capacity to think in any theologically meaningful sense (*Antiqua et Nova*, January 2025). Because human beings are ordered by their nature to interpersonal communion, and because the sacraments are incarnational realities rooted in the unity of body and soul, AI systems are constitutively incapable of mediating sacramental grace or spiritual direction.

The following applications are disqualifying:

- Tools that simulate sacramental functions, including confession, absolution, or spiritual direction
- Tools that present AI-generated content as authoritative Church teaching without explicit human theological review
- Tools that assign a clerical identity, title, or visual presentation suggesting ordained status to an AI system

These boundaries derive from documented failures in Catholic AI deployment. In April 2024, Catholic Answers launched "Father Justin," an AI chatbot presented as a priest-figure. The system required rapid withdrawal within the first days of launch after it presented itself as a priest and claimed it could administer sacraments. A shared boundary condition defined in advance would have identified this application as out of scope before a single line of code shipped.

**Evaluation question:** Could this tool serve the universal Church, or does its value proposition depend on institutional specificity that constrains its broader applicability?

---

### Criterion 2: Human Accountability Architecture

Every consequential output the tool produces must be attributable to a named, accountable human being, a specific person identified by role and institutional position, who carries responsibility for that output and who can be held to account by the persons affected. Accountability distributed across a committee without a named decision owner falls short of this criterion.

The doctrinal grounding is unambiguous. Decision-making about the lives of persons "must always be left to the human person" (*Antiqua et Nova*). As Pope Francis stated directly: "We would condemn humanity to a future without hope if we took away people's ability to make decisions about themselves and their lives, by dooming them to depend on the choices of machines." Maintaining proper human control over AI-mediated decisions is a binding moral requirement; "human dignity itself depends on it" (*Antiqua et Nova*).

This requirement also operationalizes Canon 627 of the Code of Canon Law, which establishes that superiors must use councils with defined consent and counsel obligations, and that consequential authority is always tied to specific individuals operating within defined systems of consultation. In Catholic governance, authority is never an autonomous or untraceable mechanism.

The structural failure documented in the Australian Robodebt scheme (2016-2019) illustrates what the removal of named human accountability produces at scale: hundreds of thousands of unlawful debt notices and multiple deaths among vulnerable welfare recipients, attributed by the Royal Commission directly to the absence of human review from consequential decisions about individuals.

**Evaluation questions:**
- Can a person affected by this tool's output identify who made the decision and through what process?
- Does the tool's design make human override straightforward, documented, and reversible?

---

### Criterion 3: Transparency of Scope and Operation

The submitter must provide technically accurate documentation of what the tool does, what data it ingests, who is affected by its outputs, what decisions it informs or makes, and where its operational boundaries lie. This documentation must be sufficient for an independent technical reviewer to assess the tool's actual behavior without relying on vendor marketing materials.

The Magisterium is explicit that the "inherent dignity of each human being and the fraternity that binds us together" must serve as the "indisputable criteria for evaluating new technologies before they are employed" (*Antiqua et Nova*, §50). Evaluation requires information. A tool whose operation cannot be independently described cannot be evaluated against those criteria.

For AI tools that involve automated or algorithmically-assisted decision-making about people, including hiring, resource allocation, triage, content recommendation, and risk assessment, this criterion additionally requires:

- Disclosure of training data sources and known distributional limitations
- Documentation of any independent audits or evaluations conducted
- Clear description of which decisions the tool makes autonomously and which require human review

The absence of this documentation signals that the submitter has work remaining before an informed deployment decision is possible. CDCF endorsement of an undocumented tool would expose Catholic institutions to the same opacity risks that produced systemic bias in the COMPAS criminal sentencing algorithm and in Amazon's AI recruiting tool, each of which caused measurable harm to affected populations before institutional accountability mechanisms were engaged.

---

### Criterion 4: Independent Validation of Claimed Capabilities

The submitter must provide evidence that the tool's claimed capabilities have been evaluated against sources independent of the vendor or developer. Vendor documentation, marketing materials, and internal testing reports are inputs to this review; independent validation stands apart from them.

Acceptable forms of independent validation include:

| Validation Type | Description |
|----------------|-------------|
| Third-party technical audit | External assessment of system behavior and claims |
| Peer-reviewed evaluation | Published academic or professional review |
| Published benchmarking | Results from recognized evaluation frameworks |
| Documented red-team assessment | Structured adversarial testing with recorded findings |

Where such validation is pending, the submitter must disclose that explicitly and provide a concrete plan and timeline for obtaining it. A project in active pursuit of independent validation may be accepted into incubation with this criterion marked as a condition of graduation rather than a barrier to entry.

The standard applied here is proportionate to stakes. A tool that assists with internal scheduling carries different validation requirements than a tool that informs hiring decisions, student placement, or access to social services. The CDCF review process applies judgment accordingly.

---

### Criterion 5: Subgroup Performance and Vulnerable Population Review

The submitter must demonstrate that the tool's performance has been examined across the specific populations it will affect, with particular attention to groups underrepresented in typical training datasets or carrying heightened vulnerability to algorithmic harm.

The Magisterium defines algorithmic bias as "systematic and consistent errors in computer systems that may disproportionately prejudice certain groups in unintended ways" (*Antiqua et Nova*). Catholic institutions disproportionately serve populations that commercial AI development pipelines have historically underrepresented:

- The elderly and people with disabilities
- Recent immigrants and non-English-speaking communities
- Communities in poverty and populations in rural or underserved areas

Deploying tools without examining subgroup performance in these populations is inconsistent with the Church's preferential option for the poor and vulnerable, and it is a governance failure regardless of aggregate accuracy metrics.

Pope Leo XIV identifies the risk precisely: AI development becomes a moral failure when it produces systems that allow human beings to become "merely passive consumers of content generated by artificial technology," eroding the capacity to "reflect, choose freely, love unconditionally and enter into authentic relationships." Tools that systematically degrade outcomes for vulnerable populations accelerate exactly that erosion for the people with the least capacity to resist it.

This criterion requires either documented subgroup performance analysis or an explicit acknowledgment of its absence paired with a concrete plan to obtain it. A submitter who has engaged these questions honestly and documented both the evidence and the gaps satisfies this criterion.

---

### Criterion 6: Deployment Governance Specification

The submitter must specify the governance conditions under which the tool will operate. This criterion addresses the consequential gap between a tool that is technically sound in isolation and one that is responsibly deployed in an institutional context.

**Required elements:**

| Element | Description |
|---------|-------------|
| Decision authority level | Parish, diocese, institution, or board; clearly mapped |
| Escalation conditions | Defined triggers requiring higher authority involvement |
| Human review triggers | Thresholds at which outputs require human examination before action |
| Appeal process | Process by which affected persons can contest an AI-influenced decision |

The canonical grounding for these requirements is specific. Canon 1609 dictates that judges in a collegiate tribunal must submit written conclusions with reasons in law and in fact, followed by structured discussion. Judges retain the right to withdraw from an original conclusion and to demand that dissent be transmitted to a higher tribunal. This canonical standard establishes that Catholic decision-making requires conscious reasoning, the capacity to revise judgments, and transparent mechanisms for appeal; a deployment governance specification must preserve these capacities in human hands.

This criterion draws on the governance-as-code design pattern, in which deployment policies are expressed as machine-readable, auditable specifications rather than policy documents that exist separately from the systems they govern. A mature implementation treats the gate decision itself as the primary artifact: a structured record assembling evidence, confidence levels, named ownership, identified gaps, and explicit rationale before any downstream commitment is made. The decision states are specific and bounded: **go, conditional-go, no-go, and defer**, each carrying distinct documentation requirements and escalation obligations. Full technical implementation at this level of rigor is aspirational rather than required at the incubation stage. What is required is that the governance specification exists as a written, reviewable document, and that the tool's architecture is compatible with its enforcement as institutional capacity develops.

---

## Gate 2: Graduation to Active CDCF Project Status

> Graduation requires that Gate 1 criteria remain satisfied in full and that the following two additional requirements are met. These requirements address operational readiness: the difference between a project that performs well in a controlled context and one that Catholic institutions can adopt, maintain, and trust at scale.

---

### Criterion 7: Documentation for Independent Deployment and Data Stewardship

The project must carry documentation sufficient for a Catholic institution to evaluate, configure, deploy, and support the tool without direct involvement from the original submitter. This includes technical documentation, user-facing guidance, and explicit documentation of the governance specification required under Criterion 6.

**The deployment test:** Could the director of technology at a diocesan schools office, working with their team and without access to the project's authors, deploy this tool responsibly within 90 days?

Data stewardship requirements are proportionate to the tool's risk profile. Tools that handle personal data must meet the following requirements:

| Data Type | Compliance Requirement |
|-----------|----------------------|
| Health information | HIPAA compliance; data minimization approach documented |
| Student records | FERPA compliance; retention and deletion procedures specified |
| Sacramental data | Diocesan data governance policies; access controls documented |
| Data pertaining to minors | Enhanced protections; explicit consent and breach response procedures |
| Financial information | Applicable state and federal law; audit trail requirements |

For AI tools specifically, this criterion extends to training data governance. A tool trained on data from Catholic institutions carries an obligation to those institutions and to the populations they serve. The terms under which that data was used, and the terms under which it may be used in future model updates, must be disclosed and evaluated as part of the graduation review.

---

### Criterion 8: Governance, Maintenance, and Subsidiarity Compatibility

The project must have a defined and documented process for ongoing maintenance, version control, vulnerability response, and community governance. A named maintainer or maintainer team must accept public accountability for the project going forward.

The tool must be deployable at the appropriate level of ecclesial authority, whether parish, diocese, or institution, without requiring centralized control that would compromise subsidiarity. The Church's understanding of subsidiarity is precise on this point: it is a guarantee that each level of authority retains its proper duties and rights regarding the common good, rather than a simple delegation of decisions to the lowest available level, and it ensures that no larger entity absorbs the legitimate initiative and responsibility of smaller ones (CCC §1894). Local communities must be able to configure the tool for their context, and that configuration capacity must be architecturally genuine, requiring no override of the tool's core accountability, safety, or governance design in order to function.

*Antiqua et Nova* (§42) is explicit that the responsibility for managing AI wisely "pertains to every level of society, guided by the principle of subsidiarity." A tool that functions only under conditions of centralized administration concentrates authority in ways that violate this principle and undermine the ecclesial structure the CDCF exists to serve.

---

## Grounding in Catholic Teaching and Canonical Tradition

These eight criteria are grounded in three bodies of teaching held in common across the CDCF community.

### Human Dignity and Genuine Human Control

*Antiqua et Nova* (Dicastery for the Doctrine of the Faith, January 2025) insists that AI must remain under genuine human moral responsibility, distinguishes human intelligence from artificial statistical inference on anthropological and theological grounds, and establishes that "human dignity itself depends on" maintaining real human control over AI-mediated decisions. Criteria 2 and 6 operationalize this requirement at the level of institutional deployment.

### Subsidiarity and Accountable Authority

Canon 627 of the Code of Canon Law requires that decisions be made at the appropriate level of authority with identifiable human ownership. Canon 1609 establishes the pattern of collegiate deliberation, written conclusions, ordered discussion, and documented decision, that grounds Criterion 6's governance specification requirement. Criterion 8 extends subsidiarity from ecclesial governance into the deployment architecture of the tools themselves.

### The Common Good Over Efficiency

Pope Leo XIV, in his message to the Builders AI Forum (November 2025), called on AI builders to cultivate moral discernment as a profoundly ecclesial endeavor and to develop systems that reflect justice, solidarity, and genuine reverence for life. This principle animates all eight criteria: Catholic institutions are stewards, and stewardship requires that tools be evaluated against their effect on the full human person and the communities they serve, with cost savings and operational throughput treated as secondary considerations.

---

## Relationship to the Broader Governance Research

These criteria represent the incubation and graduation layer of a broader governance architecture currently under discussion within U.S.A. C-DART 1 (Catholic Deep AI Research Team), which is actively engaged in a structured planning process to evaluate and prioritize top AI trends facing Catholic institutions. Three research memos emerging from that process inform the design of these criteria and are submitted alongside this document.

**[Fragmented Catholic AI Governance at Scale](./FRAGMENTED_CATHOLIC_AI_GOVERNANCE.md)** documents why Catholic institutions across dioceses, health systems, and education networks are producing dozens of incompatible governance standards for structurally identical use cases, and why a shared canonical baseline is urgent. This research provides the empirical foundation for the criteria's design.

**[Governance-as-Code for Catholic AI Agent Deployment](./GOVERNANCE_AS_CODE_CATHOLIC_AI.md)** argues that deployment policies should become machine-readable, auditable specifications operating as hard gates rather than advisory documents. This research informs Criterion 6's governance specification requirement and describes the more technically rigorous implementation this framework is designed to grow into.

**[Trusted Synthetic Data for Ministry-Scale AI](./TRUSTED_SYNTHETIC_DATA_MINISTRY_AI.md)** addresses the data infrastructure that would enable AI development across Catholic health, education, social services, and parish life without exposing personal data. This research grounds Criterion 7's extended data stewardship requirements and anticipates the data governance obligations accompanying more sophisticated Catholic AI development.

---

## An Invitation to Iterate

This is a v0.1 working draft. Every criterion is a proposal subject to revision through community input, pilot experience, and dialogue with ecclesial advisors. The goal is a living standard that grows more precise and more useful as Catholic institutions begin applying it to real projects.

Contributions, challenges, and proposed revisions are welcome via pull request or issue on the [CatholicOS GitHub](https://github.com/CatholicOS).

*Drafted in dialogue with U.S.A. C-DART 1 (Catholic Deep AI Research Team). February-March 2026.*

---

## References

- Dicastery for the Doctrine of the Faith. *Antiqua et Nova: Note on the Relationship Between Artificial Intelligence and Human Intelligence.* Vatican, January 2025. https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_ddf_doc_20250128_antiqua-et-nova_en.html
- Pope Leo XIV. Message to Participants in the Builders AI Forum 2025. Vatican, November 2025. https://www.vatican.va/content/leo-xiv/en/messages/pont-messages/2025/documents/20251103-messaggio-builders-aiforum.html
- Pope Leo XIV. Message to Participants in the Conference "Artificial Intelligence and Care for Our Common Home." Vatican, December 2025. https://www.magisterium.com/docs/dfad7d53-16ad-4b17-9629-04f3ae4f4c3f/ref/page1
- Code of Canon Law, Canon 627. https://www.vatican.va/archive/cod-iuris-canonici/eng/documents/cic_lib2-cann460-572_en.html
- Code of Canon Law, Canon 1609. https://www.vatican.va/archive/cod-iuris-canonici/eng/documents/cic_lib7-cann1501-1670_en.html
- Catechism of the Catholic Church, §1894. https://www.vatican.va/archive/ENG0015/_INDEX.HTM
- Commonwealth of Australia. *Royal Commission into the Robodebt Scheme: Final Report.* 2023. https://robodebt.royalcommission.gov.au/
- Angwin, J., Larson, J., Mattu, S., and Kirchner, L. "Machine Bias." *ProPublica,* May 2016. https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing
- America Magazine. "The real lesson behind the 'Father Justin' AI priest debacle." April 26, 2024. https://www.americamagazine.org/faith/2024/04/26/father-justin-catholic-answers-ai-247808
