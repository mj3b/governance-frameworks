# Governance-as-Code for Catholic AI Agent Deployment

> **Document type:** Research memo

> **Status:** Working draft - U.S.A. C-DART 1 discussion

> **Relationship:** Supplementary research underlying [CDCF AI Vetting Criteria v0.1](./ai-vetting-criteria.md)

---

## Table of Contents

1. [The Core Argument](#the-core-argument)
2. [What Governance-as-Code Is](#what-governance-as-code-is)
3. [Why Catholic Institutions Need It](#why-catholic-institutions-need-it)
4. [The Three-Layer Stack](#the-three-layer-stack)
5. [The Gate Decision as Primary Artifact](#the-gate-decision-as-primary-artifact)
6. [Honest Assessment of Institutional Readiness](#honest-assessment-of-institutional-readiness)
7. [What Catholic Institutions Can Do Now](#what-catholic-institutions-can-do-now)
8. [Relationship to the CDCF Vetting Criteria](#relationship-to-the-cdcf-vetting-criteria)
9. [Bibliography](#bibliography)

---

## The Core Argument

AI governance currently lives in PDFs and committee meetings. When a diocese, school, or Catholic hospital deploys an AI system, the governance process typically produces a document that says the system is approved. That document exists separately from the system it governs. It cannot prevent a non-compliant deployment. It cannot be automatically validated. It can only react after something goes wrong.

Governance-as-code is the practice of turning those policy documents into machine-executable specifications wired directly into deployment pipelines. The governance becomes part of the infrastructure. This shift is already occurring in regulated enterprise environments. The question for Catholic institutions is whether they participate in shaping what those specifications encode, or whether they inherit secular governance schemas designed without reference to Catholic moral theology, canonical authority, or the Church's preferential concern for the vulnerable.

---

## What Governance-as-Code Is

In a governance-as-code architecture, policy requirements are expressed as version-controlled schemas — typically JSON or YAML — that define exactly what an AI system must demonstrate before it can reach production. When a developer attempts to deploy an agent, the deployment pipeline calls those schemas as hard gates.

The gate logic is deterministic. Pass all gates and the agent deploys. Fail any gate and it does not. Every decision, pass or fail, is logged in an immutable audit trail that regulators, diocesan authorities, or institutional leadership can examine after the fact.

The schemas themselves define the governance criteria: what evidence of safety testing is required, what data domains the system is permitted to touch, what level of human oversight it operates under, who the named accountable person is, and what conditions require escalation to a higher authority. These are the same questions the CDCF Vetting Criteria ask. Governance-as-code is the technical architecture that makes those questions into enforceable gates rather than advisory checklists.

This is distinct from using AI to govern AI. The gate decision in a governance-as-code architecture is deterministic: a schema either passes or it does not, based on explicit criteria defined in advance by human authorities. AI can assist with evidence synthesis and risk surfacing within the pipeline, but the gate logic itself remains under human-defined, machine-enforced control. This distinction matters because an AI-governed pipeline requires governance of its own, creating a regress that deterministic schema enforcement avoids.

Researchers studying multi-agent system failures have identified 14 distinct failure modes across three categories — system design issues, inter-agent misalignment, and task verification breakdowns — underscoring the structural importance of deterministic gate logic rather than agent-mediated compliance review.[^1] Empirical survey data from 306 AI practitioners across 26 domains confirms that reliability remains the top deployment challenge, with 68 percent of production agents executing ten or fewer steps before human intervention is required.[^2] These findings argue for governance architectures in which human-defined, machine-enforced gates are the primary control mechanism rather than agent judgment.

A further structural concern is the compliance gap between regulatory intent and deployment practice. Current AI governance frameworks — including California SB 53, the New York RAISE Act, the U.S. AIREA, and EU AI Act GPAI obligations — share three recurring gaps: scope ambiguity in defining covered systems, point-in-time compliance requirements that fail to address systems that evolve after initial approval, and information asymmetries between regulators and deploying institutions.[^3] Governance-as-code directly addresses all three: schema definitions establish scope with precision, version-controlled schemas evolve with the system they govern, and immutable audit trails close the information gap.

The Commission of the Bishops' Conferences of the European Union (COMECE) affirms that evaluating AI from an ethical perspective "requires internal control principles and risk assessment in addition to legislation."[^4] Governance-as-code is the direct instantiation of those mandated internal control principles, translating ethical evaluation from a periodic review activity into a continuous, enforceable infrastructure requirement.

---

## Why Catholic Institutions Need It

The fragmentation problem documented in the companion memo on Catholic AI governance at scale is fundamentally a governance encoding problem. Each diocese is expressing its Catholic AI values in a different format, at a different level of specificity, for different audiences. Orange wrote a council charter. Biloxi wrote a decree. Arlington wrote school policy. None of those instruments are machine-readable. None of them can be automatically validated against. A vendor can acknowledge all three documents and deploy a non-compliant system anyway, because the documents have no technical enforcement mechanism.

Governance-as-code changes that structural relationship. A shared canonical governance schema — a baseline set of machine-executable policies encoding the principles of *Antiqua et Nova*,[^5] the USCCB AI principles,[^6] and the Ethical and Religious Directives into version-controlled, reusable specifications — would let any diocese adopt the shared baseline and extend it with local requirements. Subsidiarity is preserved because local authority still governs local decisions. Solidarity is achieved because every institution operating on the shared baseline is interoperable.

A vendor serving Catholic schools would face one canonical schema with optional diocesan extensions rather than dozens of incompatible checklists. A Catholic hospital system operating across diocesan lines could deploy uniformly because the governance infrastructure is compatible across jurisdictions. The governance becomes as portable as the tools it governs.

The EU AI Act, with key obligations for high-risk AI systems taking effect in 2026, creates structural demand for auditable deployment governance in high-risk AI categories.[^7] Catholic healthcare, education, and social services operate squarely in those categories. The regulatory pressure is arriving regardless of whether Catholic institutions have prepared for it.

The *Rome Call for AI Ethics* demands that principles and values be instilled into a framework that "acts as a point of reference for digital ethics, guiding our actions and promoting the use of technology to benefit humanity."[^8] The governance platform layer of this architecture directly answers that call, creating a shared, tangible reference point for digital ethics that is enforceable across Catholic institutional boundaries rather than aspirational.

---

## The Three-Layer Stack

A mature governance-as-code architecture for Catholic AI deployment operates across three layers, each serving a distinct institutional function.

**Infrastructure layer.** CI/CD pipeline hooks, Kubernetes admission controllers, and deployment gate logic. This is where schemas execute as hard gates and where audit trails are generated. Developers interact with this layer. It is invisible to most institutional leadership but is the enforcement mechanism that gives the other layers their operational force.

**Governance platform layer.** The schema library itself: version-controlled policy specifications, risk classification logic, and the canonical Catholic governance baseline that dioceses and institutions can adopt and extend. This is where Catholic moral theology, canonical requirements, and regulatory frameworks are encoded as machine-readable criteria. The CDCF is positioned to steward this layer as the shared, community-maintained standard for Catholic AI deployment governance.

**Application layer.** The institutional-facing tools: onboarding workflows that walk submitters through governance requirements, risk dashboards that surface compliance status across a portfolio of deployed systems, and audit artifacts that demonstrate governance compliance to diocesan leadership or external regulators.

These three layers correspond directly to the three levels of institutional capacity Catholic organizations actually have. A small parish or school operates primarily at the application layer, using governance tools without needing to understand the infrastructure underneath. A diocesan IT office operates at the governance platform layer, adopting and extending canonical schemas for local context. A large Catholic health system or university operates at the infrastructure layer, embedding governance gates into its own CI/CD pipelines.

---

## The Gate Decision as Primary Artifact

The most significant design principle in this framework is that the gate decision itself — the go, conditional-go, no-go, or defer determination — is treated as a first-class artifact rather than a byproduct of the review process.

A gate decision artifact captures the specific evidence assembled, the confidence levels assigned, the gaps identified, the named human decision owner, the rationale for the outcome, and the conditions under which the decision was made. It is immutable once recorded. It is the document that answers the regulator's question, the bishop's question, and the affected person's question: why was this system deployed, under whose authority, and on what basis.

This design directly reflects the canonical standard established in Canon 1609, which requires that deliberative processes produce written conclusions with reasons in law and in fact, and that the capacity for review and appeal be preserved.[^9] A gate decision artifact is the technical implementation of that canonical requirement.

The immutability of the audit trail also serves a specifically Catholic institutional concern. The USCCB warns that AI can be misused to "undermine the dignity of persons and respect for the truth" through the manipulation of information.[^6] An immutable gate decision record ensures that if a deployed system begins generating falsehoods or utilitarian biases, institutional accountability is clear, traceable, and preserved for review. The practical consequence of ungoverned audit trails is documented in enterprise deployments: when a production AI system retrieves a superseded policy document with no captured provenance, the organization cannot reconstruct what the system saw or why — turning incident response into forensic guesswork rather than evidence-based accountability.[^10]

The four decision states carry distinct implications. A **go** decision records that all governance criteria were satisfied and deployment is authorized. A **conditional-go** records that deployment is authorized subject to specific conditions that must be satisfied within a defined timeframe, typically used when independent validation is pending. A **no-go** records that one or more criteria fell short of requirements and deployment is blocked, with the specific criteria and evidence gaps documented. A **defer** records that the decision requires escalation to a higher authority before proceeding, and specifies which authority and why.

---

## Honest Assessment of Institutional Readiness

Full technical implementation of governance-as-code at the infrastructure layer is beyond the current capacity of most Catholic institutions, and overstating that capacity would produce the kind of governance credibility gap this framework is designed to prevent. Most Catholic institutions — including well-resourced dioceses and health systems — currently operate at the application layer at best. They have policy documents. Some have review committees. Very few have version-controlled governance schemas. None, to the knowledge of this research, have canonical Catholic governance schemas embedded as hard gates in CI/CD deployment pipelines.

That gap is the opportunity, and it is the reason the CDCF Vetting Criteria are structured as they are. Criterion 6 requires a written, reviewable governance specification and architectural compatibility with future enforcement. Full infrastructure-layer implementation is aspirational at the incubation stage. The governance specification written today becomes the schema encoded tomorrow. The criteria are designed to build institutional capacity progressively, meeting institutions at their current maturity rather than requiring capabilities still to be developed.

A critique raised in C-DART 1 session discussions is worth acknowledging directly: healthcare governance in Catholic institutions is primarily a legal and regulatory problem rather than an engineering problem. HIPAA, FDA, CMS, and state law set the floor. That critique is accurate, and this framework accepts it. Governance-as-code operates as the technical layer that makes compliance with those frameworks auditable, reproducible, and interoperable across Catholic institutional boundaries. The distinction between replacing regulation and making compliance technically enforceable is the distinction that makes this approach credible rather than overreaching.

---

## What Catholic Institutions Can Do Now

Given the honest assessment of current institutional readiness, the near-term contribution of this research is a written evaluation standard that functions as the precursor to a production CI/CD governance pipeline rather than the pipeline itself.

The CDCF Vetting Criteria represent that evaluation standard. Criterion 6 asks submitters to specify decision authority levels, escalation conditions, human review triggers, and appeal processes in a written, reviewable document. That specification is the first step toward a machine-executable schema. An institution that has written a rigorous governance specification for one tool has done most of the intellectual work required to encode that specification as a reusable governance schema.

The CDCF is positioned to maintain the canonical schema library that individual institutions extend rather than build independently. That is the solidarity layer described in the fragmentation memo: a shared baseline that preserves local authority while making Catholic AI governance interoperable at scale.

Three concrete actions follow from this research for Catholic institutions at any level of technical maturity.

First, require written governance specifications for every AI tool under evaluation. The specification format in Criterion 6 of the CDCF Vetting Criteria provides a starting template. Second, version-control those specifications. Even a Word document in a shared drive with a version number and a named owner is a meaningful step toward governance-as-code discipline. Third, evaluate vendor AI tools for schema compatibility: does the tool's architecture support governance gate integration, or does it require overriding governance controls to function?

---

## Relationship to the CDCF Vetting Criteria

Criterion 6 of the [CDCF AI Vetting Criteria](./ai-vetting-criteria.md) is the direct operational expression of this research. It requires a deployment governance specification as a condition of incubation acceptance, with the four-state decision model (go, conditional-go, no-go, defer) as the structural framework for that specification.

Criterion 8 extends the governance-as-code principle to the deployment architecture of the tools themselves, requiring that tools be deployable at the appropriate level of ecclesial authority without overriding their core governance design.

Together, Criteria 6 and 8 establish the governance specification requirements that position Catholic institutions to adopt fuller governance-as-code implementation as institutional capacity develops.

---

## Bibliography

[^1]: Mert Cemri, Melissa Z. Pan, Yapei Yang, Aditya Agrawal, Tatsunori Hashimoto, Diyi Yang, Qian Yang, and Percy Liang, "Why Do Multi-Agent LLM Systems Fail?" arXiv:2503.13657, submitted March 17, 2025, https://arxiv.org/abs/2503.13657.

[^2]: Melissa Z. Pan, Mert Cemri, Lingjiao Chen, Matei Zaharia, James Zou, and Percy Liang, "Measuring Agents in Production," arXiv:2512.04123, submitted December 2, 2025, revised February 3, 2026, https://arxiv.org/abs/2512.04123.

[^3]: Joe Kwon and Stephen Casper, "Internal Deployment Gaps in AI Regulation," arXiv:2601.08005, submitted January 12, 2026, revised February 14, 2026, https://arxiv.org/abs/2601.08005.

[^4]: Commission of the Bishops' Conferences of the European Union (COMECE), "Statement on the EU Artificial Intelligence Act," COMECE, 2024, https://church.mt/comece-on-the-artificial-intelligence-act-it-does-justice-to-the-ethical-foundations-of-the-eu/.

[^5]: Dicastery for the Doctrine of the Faith and Dicastery for Culture and Education, *Antiqua et Nova: Note on the Relationship Between Artificial Intelligence and Human Intelligence* (Vatican City: Dicastery for the Doctrine of the Faith, January 28, 2025), https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_ddf_doc_20250128_antiqua-et-nova_en.html.

[^6]: United States Conference of Catholic Bishops, *Joint Letter on Artificial Intelligence Principles and Priorities*, June 9, 2025, https://www.usccb.org/resources/joint-letter-artificial-intelligence-principles-and-priorities.

[^7]: European Parliament and Council of the European Union, *Regulation (EU) 2024/1689 of the European Parliament and of the Council Laying Down Harmonised Rules on Artificial Intelligence (Artificial Intelligence Act)*, Official Journal of the European Union, August 12, 2024, https://artificialintelligenceact.eu.

[^8]: Pope Francis, "Address at the Signing of the Rome Call for AI Ethics," Vatican City, February 28, 2020, https://www.vatican.va/content/francesco/en/speeches/2020/february/documents/papa-francesco_20200228_eticaartificiale.html.

[^9]: *Code of Canon Law*, Canon 1609 (Vatican City: Libreria Editrice Vaticana, 1983), https://www.vatican.va/archive/cod-iuris-canonici/eng/documents/cic_lib7-cann1501-1670_en.html.

[^10]: Rick Hamilton, "Data Governance for AI Must Be Executable," *hamiltonandboss.com* (Substack), 2025, https://substack.com/@rickwritesai/p-189861656.
