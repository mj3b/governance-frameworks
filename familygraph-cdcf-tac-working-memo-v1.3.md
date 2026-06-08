# TAC Working Memo: FamilyGraph
## CDCF Gate 1 Incubation Evaluation and Assurance Review — Version 1.3

---

| Field | Detail |
|---|---|
| **Document type** | TAC Working Memo — Governed Pre-Finding Analysis and Request for Response |
| **Version** | 1.3 |
| **Evaluated artifact** | `github.com/christreadaway/familygraph`, main branch; ZIP archive reviewed June 2026 |
| **Submission channel** | WhatsApp / Telegram; introduced by Fr. John Romano D'Orazio; submitted by Chris Treadaway |
| **Vetting framework** | CDCF Project Vetting Criteria v0.2, Gate 1 (C1–C6) |
| **Evaluating TAC member** | Mark Julius Banasihan, AI Governance Specialist |
| **AI assistance** | AI systems assisted with repository inspection, source synthesis, adversarial review, and drafting. AI output is treated as research assistance rather than authority. The evaluating TAC member remains responsible for every retained claim, inference, risk classification, and recommendation. Code-level observations should be reproducible from the cited repository location before becoming a formal CDCF finding. |
| **Preliminary disposition** | **Conditional incubation may be considered; CDCF endorsement, broad deployment, and Gate 2 graduation are deferred.** |

---

## Preliminary Disposition at a Glance

This memo distinguishes **incubation eligibility** from **institutional endorsement**.

Under the published CDCF lifecycle, Gate 1 incubation requires mission alignment and a credible plan for satisfying Criteria 2–6. Graduation requires demonstrated satisfaction of all eight criteria and readiness for broad deployment. FamilyGraph may be considered for a tightly bounded incubation pathway because its mission and architecture are serious and several gaps are remediable. It should not yet be represented as CDCF-vetted for production use, broadly safe for Catholic family data, or ready for diocesan-scale adoption.

| Criterion | Current Status | Epistemic Basis | Required Before |
|---|---|---|---|
| C1 Mission Alignment | ✅ Pass with scope conditions | Observation | Incubation |
| C2 Human Accountability | ❌ Material gap | Observation + inference | Live-family-data pilot |
| C3 Transparency | ⚠️ Partial | Observation + correction | Incubation documentation |
| C4 Independent Validation | ❌ Gap | Observation | Validation plan for incubation; results for graduation |
| C5 Vulnerable Populations | ❌ Gap | Risk analysis + missing evidence | Live-family-data pilot |
| C6 Deployment Governance | ❌ Gap | Observation | Live-family-data pilot |
| C7 Data Stewardship | ❌ Gap | Observation + missing policy evidence | Gate 2 |
| C8 Maintenance and Community Governance | ❌ Gap | Observation + stated maintainer posture | Gate 2 |

### Present recommendation

- **Gate 1:** Conditional incubation may proceed only after the project owner accepts the review method, supplies the required response package, and agrees that incubation is an evidence-producing stage rather than an endorsement.
- **Live production use:** Deferred pending named-human accountability, vulnerable-family safeguards, field-level authority rules, incident and correction procedures, and an approved pilot protocol.
- **Gate 2 / active CDCF status:** No-go at present.
- **Diocesan or multi-institution deployment:** Outside the present assurance case and prohibited from being inferred from a single-institution pilot.

This is a working recommendation for TAC deliberation. It is not a Board decision and does not bind CDCF.

---

## Governance of This Review

This review is itself a governed decision process.

The evaluating member is not claiming unilateral authority to approve or reject FamilyGraph. Under the CDCF Bylaws, committees provide recommendations unless the Board expressly delegates decision authority. Conflicts must be disclosed, and materially interested participants should abstain from dispositive voting. The repository author, pilot institution, contributors, reviewers, and any CDCF member with a commercial, institutional, authorship, funding, or close collaborative interest should disclose that relationship before formal deliberation.

The following controls apply to this memo:

1. **Pre-finding status.** The document records analysis, questions, conditions, and provisional judgments. It is not a certification, legal opinion, security attestation, canonical determination, or final Board action.
2. **Author response.** Chris Treadaway should be able to correct factual errors, supply missing evidence, dispute inferences, and propose remediation. Disagreement should remain visible in the record.
3. **Independent review.** Material security, privacy, safeguarding, identity-resolution, and legal claims should be reviewed by qualified persons independent of the project’s development.
4. **Recusal.** A materially interested TAC member may provide facts and technical explanation but should not control the final vote.
5. **Versioned judgment.** Findings apply only to the identified repository version, commit, deployment profile, and evidence package. Material architectural or deployment changes require reassessment.
6. **No marketing inference.** Neither submission nor incubation may be described as CDCF endorsement.
7. **Protection of families.** Where evidence is incomplete and the plausible harm falls disproportionately on children or vulnerable families, uncertainty is not transferred to those families through premature deployment.

## Methodology Note: How This Review Should Be Read

This memo is not only a list of findings. It is a governed review method. The method matters because a technically impressive project can still become trusted faster than its evidence supports.

The review uses a simple rule:

> No governance word counts unless it points to an actor, mechanism, evidence standard, decision threshold, or correction path.

This section is written for three audiences at once:

- **Chris** — to understand what evidence would resolve a finding.
- **TAC reviewers** — to scrutinize claims by discipline without re-litigating the whole memo.
- **CDCF leadership** — to distinguish incubation, endorsement, live deployment, and graduation.

---

### Method Card M-01 — Source Hierarchy

| Field | Review method |
|---|---|
| **Purpose** | Prevent weak sources from carrying strong claims. |
| **Primary evidence** | Repository code, tests, migrations, specifications, security docs, integration contracts, session notes, deployment instructions. |
| **Governance authority** | CDCF bylaws, manifesto, lifecycle, vetting criteria, standards, and Board-adopted policies. |
| **Moral frame** | Catholic teaching on human dignity, prudence, subsidiarity, solidarity, common good, and institutional responsibility. |
| **External standards** | NIST AI RMF, privacy/security standards, software supply-chain guidance, legal/regulatory materials where relevant. |
| **Diagnostic layer** | Rationality, cognitive-failure, and AI-safety concepts used to locate failure mechanisms. |
| **Boundary** | Diagnostic concepts do not prove that the project is unsafe, lawful, unlawful, Catholic, or non-Catholic. They generate questions the evidence must answer. |

**Reviewer prompt:** Is this claim supported by the right kind of evidence, or is the memo using a diagnostic concept where repository evidence, law, security review, or CDCF authority is required?

---

### Method Card M-02 — Epistemic Labels

Every material claim should fit one of these labels.

| Label | Meaning | Example |
|---|---|---|
| **Observation** | Directly reproducible from repository or authoritative source | `recomputeStatus()` appears to update EIM status without an audit call |
| **Inference** | Conclusion drawn from observations | Silent EIM changes weaken decision reconstruction |
| **Risk** | Forward-looking possibility | A stale or silent EIM status could affect ministry access decisions |
| **Unknown** | Evidence is insufficient | Sanitizer recall for Vietnamese or Filipino names is unknown |
| **Correction** | Earlier claim narrowed, revised, or withdrawn | General audit atomicity claim narrowed to `entity_changes` |
| **Recommendation** | Proposed control | Add audit coverage matrix |
| **Decision** | Authorized CDCF disposition | Board approval, incubation, graduation, rejection |

**Reviewer prompt:** Does the memo label the claim correctly? If not, correct the label before debating the conclusion.

---

### Method Card M-03 — Concept Discipline

| Governance term | What it must resolve into |
|---|---|
| **Human oversight** | Named reviewer, evidence access, independent reason, authority to reject/escalate, correction duty |
| **Auditability** | Reconstructable chain from source record → system output → human action → downstream effect → correction |
| **Validation** | Representative deployment-context testing with predetermined thresholds |
| **Safety** | Prevention, detection, containment, correction, learning, and stopping rules |
| **Pseudonymization** | Measured reduction in direct-identifier and contextual re-identification risk |
| **Local-first** | Supported deployment profile, key custody, backup, operator authority, incident response |
| **Source of truth** | Field-level authority, provenance, permissible purpose, override path, correction right |

**Reviewer prompt:** Where a term appears in FamilyGraph documentation, does it name a real control or merely a reassuring posture?

---

### Method Card M-04 — Map–Territory Test

| Project map | Territory question |
|---|---|
| Conflicts enter a review queue | Do operators have time, competence, and authority to review them? |
| Merges are reversible | Can affected families discover, contest, and obtain reversal? |
| Actor fields are logged | Do they correspond to authenticated named people? |
| PII is encrypted | Who can access the host, browser token, backups, and key file? |
| Data remains local | Do connectors, webhooks, support workflows, or AI use transmit data elsewhere? |
| AI receives pseudonyms | Can context still identify the family? |
| Consent is recorded | Was consent valid, contextual, current, and supplied by someone with authority? |
| Provenance exists | Does provenance determine which source controls the field? |
| Safe-environment status exists | Is the local operator authorized to interpret or alter it? |

**Reviewer prompt:** Are we approving the documented map, or do we have evidence from the operational territory?

---

### Method Card M-05 — Bayesian Evidence Updating

This review should state what would change its mind.

| Current belief | Present confidence | Evidence that would raise confidence | Evidence that would lower confidence |
|---|---:|---|---|
| FamilyGraph addresses a real institutional identity problem | High | Adopter evidence and repeated cross-system need | Proof incumbent tools already solve the same governed interoperability problem |
| Matching is safe enough for real family data | Low / unknown | Independent benchmark with representative records and low false-merge severity | Any high-risk false merge or uncalibrated threshold behavior |
| Sanitization is adequate for external-AI workflows | Low / unknown | Leakage tests, contextual re-identification tests, approved destination controls | Missed direct identifiers or ungoverned AI exports |
| Human review preserves judgment | Partial / unknown | Telemetry showing evidence access, reasons, overrides, escalations, and corrections | Near-total acceptance, minimal review time, no reasons, shared actors |
| Broad CDCF endorsement is appropriate | Low | Completed Gate 2 evidence package and independent review | Any unresolved P0 condition |

**Reviewer prompt:** What evidence would change this finding? If no evidence would change it, the finding is not being governed rationally.

---

### Method Card M-06 — Cognitive Failure Checks

| Failure mode | How it could appear in this review | Control |
|---|---|---|
| **Founder halo** | Chris’s competence substitutes for independent evidence | Review the artifact as if author identity were removed |
| **Catholic attire belief** | “Catholic” becomes a trust signal instead of a constraint | Ask what feature was delayed, prohibited, or redesigned because of Catholic governance |
| **Motivated stopping** | Review stops at encryption, tests, or local-first design | Require evidence for family-facing risks |
| **Motivated continuation** | Conditions accumulate but no stopping threshold is enforced | Use predefined suspension and no-go triggers |
| **Documentation substitution** | Strong docs are treated as operational proof | Require runtime, pilot, and independent evidence |
| **Metric defense** | Duplicate reduction or import success hides family harm | Add safety metrics and appeal outcomes |
| **Scope drift** | Single-machine tool becomes diocesan infrastructure without reassessment | Require deployment-profile reassessment |

**Reviewer prompt:** What would this review miss if everyone involved wants the project to succeed?

---

### Method Card M-07 — Human Influence Telemetry

This method asks whether human counsel, judgment, and command survive the workflow.

| Prudential act | Evidence required |
|---|---|
| **Counsel** | Source records viewed, conflicting evidence, provenance, freshness, data-quality warnings, household context |
| **Judgment** | Reviewer identity, role, reasoning, review time, acceptance/rejection, escalation, second review |
| **Command** | Authority domain, override power, downstream effect, rollback power, stop-use authority |
| **Contestability** | Family correction path, appeal owner, response deadline, evidence supplied by affected person |
| **Repair** | Correction, notification, downstream propagation, harm assessment, remediation owner |
| **Reform** | Rule change, threshold update, reviewer training, system restriction, revalidation |

**Reviewer prompt:** Does the record show a human judgment, or only a human action?

---

### Method Card M-08 — Catholic Governance Lens

| Principle | Review question |
|---|---|
| **Human dignity** | Does the system treat the person as a subject who can be represented wrongly and seek correction? |
| **Prudence** | Are counsel, judgment, and command practically exercisable? |
| **Subsidiarity** | Is authority held at the proper level, with higher authority where law, safeguarding, or ecclesial competence requires it? |
| **Solidarity** | Does the review begin from the family least able to detect or contest error? |
| **Common good** | Are administrative gains subordinated to trust, family protection, and institutional accountability? |
| **Institutional repentance** | Can the institution acknowledge harm, reconstruct cause, repair injury, and reform the system? |

**Reviewer prompt:** Does the technical design embody the moral claim, or merely describe it?

---

### Method Card M-09 — Reviewer Self-Governance

Before moving a finding toward closure, the reviewer should answer:

| Question | Yes / No / Notes |
|---|---|
| Did I reproduce the code-level claim or mark it for independent reproduction? | — |
| Did I separate observation from inference and risk? | — |
| Did I look for evidence that weakens my preferred conclusion? | — |
| Did I avoid using “AI safety” language where privacy, identity, security, or safeguarding language is more precise? | — |
| Did I avoid treating local-first, encryption, Catholic mission, or open source as proof of safety? | — |
| Did I specify what evidence would update the finding? | — |
| Did I identify the affected family, child, operator, institution, or diocese? | — |
| Did I preserve a route for Chris to correct factual errors? | — |

---

### Method Card M-10 — AI Assistance Boundary

| Field | Rule |
|---|---|
| **Allowed use** | Code navigation, draft synthesis, risk brainstorming, source comparison, issue-card generation. |
| **Not allowed** | Treating AI output as independent validation, legal advice, security attestation, canonical judgment, or Board authority. |
| **Required control** | Every code-level claim should be reproducible by a human reviewer before formal adoption. |
| **Disclosure** | AI assistance should be disclosed in the memo and in any formal review record. |
| **Reviewer prompt** | Did AI help produce this claim, and has a human reviewer verified it? |

---

## Collaborative Review Protocol

This file is intended to remain in the repository so the project owner and TAC reviewers can work from one shared evidentiary record.

### Suggested repository location

`governance/reviews/CDCF-TAC-FAMILYGRAPH-WORKING-MEMO.md`

### Status vocabulary

Use only these statuses:

- `OPEN`
- `AUTHOR RESPONSE RECEIVED`
- `EVIDENCE REQUESTED`
- `REMEDIATION PROPOSED`
- `REMEDIATION VERIFIED`
- `DISPUTED`
- `ACCEPTED RISK`
- `CLOSED`
- `SUPERSEDED`

### Finding identifier format

Use:

`FG-C[criterion]-[number]`

Examples:

- `FG-C2-01` — named-human operator accountability;
- `FG-C4-02` — independent sanitizer validation;
- `FG-C6-01` — connector pause threshold.

### Response fields

For each material finding, retain:

| Field | Required content |
|---|---|
| Finding ID | Stable identifier |
| Criterion | CDCF criterion or cross-cutting domain |
| Type | Observation, inference, risk, unknown, correction, recommendation |
| Severity | Critical, high, moderate, low |
| Evidence | File, function, line, test, policy, or external source |
| Reasoning | Why the evidence supports the conclusion |
| Affected parties | Adults, minors, families, operators, institution, diocese |
| Required response | Evidence, correction, design change, policy, independent review |
| Project response | Maintainer’s answer |
| TAC comments | Named reviewer comments |
| Disposition | Open, disputed, remediated, accepted, closed |
| Verification | Person, date, repository version, and evidence used |

### Rules for collaborative feedback

- Do not erase a disputed finding. Add the counterevidence and disposition.
- Separate factual corrections from disagreements about risk tolerance.
- Require a named reviewer for every material acceptance or closure.
- Do not close a finding on the basis of a planned control; verify implementation where implementation is required.
- Record dissent where consensus is absent.
- Link remediation to commits, pull requests, tests, policy versions, or independent reports.
- Reopen findings when deployment scope changes.

---

## What FamilyGraph Is

Catholic institutions run on family data. A mid-size parish holds records for 400 to 800 families across a parish management system, a donor CRM, a faith-formation database, and at minimum a handful of spreadsheets. A Catholic school adds a student information system and a parent-engagement platform. The same family appears in all of them, under different spellings, phone numbers, and addresses. Every application solves identity resolution independently. Within weeks of any import or merger, the systems disagree about who belongs to which household.

FamilyGraph is the identity layer that resolves this. It holds the authoritative record of who a family is and serves that record to consuming applications through a versioned local API. FamilyGraph does not store sacramental records, financial transactions, grades, or enrollment decisions. Those remain in their source systems.

Version 1 shipped to one pilot institution (St. Theresa Catholic School) in April 2026. The v0.2 integration contract is live. A parent-engagement application is in flight as the first consuming application. The session notes document 15 build sessions between April 27 and June 4, 2026.

### Deployment Environments

| Environment | Primary Systems Integrated | Population Size | Key Data Sensitivity |
|---|---|---|---|
| Parish | Ministry Platform, Breeze, Google Sheets, generic CSV | 400–2,000+ registered families | Donor relationships, custody flags, family structure |
| Catholic School | FACTS SIS, RenWeb, Google Sheets | 200–1,500 students and families | Student records, minor PII, parental consent, EIM certifications |
| Multi-campus / Diocesan | Multiple parishes and schools sharing one instance | Thousands of families across linked institutions | Per-school consent overrides, cross-institution family links, diocesan EIM records |

### What the Session Notes Reveal About Development Posture

The session notes (`session_notes.md`) document a decision log spanning v1 through v13 of the specification, written by Chris Treadaway with Claude (web chat) for spec work. All implementation was built by Claude Code across 15 documented sessions. The notes are an unusually complete record of design decisions, rejected alternatives, and known limitations. The following decisions are relevant to this evaluation.

The codebase was developed as UNLICENSED (closed source) from April 27 through June 3, 2026. The Apache-2.0 decision was made on June 3, 2026, approximately six weeks after development began and days before the CDCF submission context. The open-source commitment is recent.

Real family data, specifically the Treadaway surname and real-sounding dates of birth, appeared in test fixtures and was scrubbed in the pre-public review on June 3, 2026. The evaluated archive should be clean. The scrubbing reveals that earlier development used real data patterns.

The sanitizer's anonymization language was explicitly softened to best-effort in the same June 3 session, with the disclosure now reading: "no automated system detects every possible identifier; operators should review sanitized output before sharing with untrusted parties." This disclosure confirms rather than undermines the C3 assessment.

---

## Data Classification and Risk Profile

FamilyGraph holds the following categories of personal data. Each carries distinct compliance obligations and harm potential if breached, misclassified, or incorrectly merged.

| Data Category | Storage Method | Compliance Obligation | Harm if Compromised |
|---|---|---|---|
| Contact PII (names, emails, phones, addresses) | AES-256-GCM ciphertext; searchable via HMAC-SHA256 | State privacy law; diocesan data policy | Identity theft, stalking, unauthorized contact |
| Date of birth | AES-256-GCM ciphertext | Heightened protection for minors under 13 | Age-targeted harm |
| Household structure and custody designations | Relational schema; notes encrypted | Family court orders; institution-level policy | Custody violation, child safety risk |
| Photo and directory consent | Boolean flags; per-person and per-school overrides | FERPA (school deployments); state student privacy law | Unauthorized publication of minors' images |
| EIM certification status and expiry | Plaintext status field (`pending` / `certified` / `expired`); notes encrypted | Diocesan safe-environment policy | Uncertified volunteer accessing minors |
| Minor PII (student roster data) | Same encryption as adult PII | FERPA; heightened privacy protections | Heightened harm to children |
| Operator notes (free-form) | AES-256-GCM ciphertext | Institutional policy | Variable; notes may capture sensitive family circumstances |
| Source provenance | Unencrypted metadata (category tag, import timestamps) | Minimal | Low; no PII in provenance layer |

**On FERPA:** When a school deploys FamilyGraph to manage student identity data, FERPA applies to the education records it holds under 20 U.S.C. § 1232g and 34 C.F.R. Part 99. The compliance obligation rests with the deploying institution and extends to systems it uses to maintain those records. FERPA compliance documentation for the school deployment context is absent from the submitted materials and constitutes a Gate 2 condition.

**On COPPA:** FamilyGraph is a local server application, not an online service directed to children under 13 within the meaning of 15 U.S.C. § 6501. COPPA exposure is limited in the standard deployment scenario. Institutions deploying FamilyGraph with remote access or cloud hosting change this analysis and should seek independent legal review.

---

## Automated Decision Points and AI-Safety Review Map

FamilyGraph should be reviewed as **identity-governance infrastructure with automated decision points**, not as a general-purpose AI system. The governance question is practical:

> Which software functions can shape identity, disclosure, consent, family linkage, or institutional trust before a human fully understands the consequence?

This section is intentionally structured as reviewer-facing issue cards. Each card separates **what the component does**, **what evidence supports the finding**, **why it matters**, **who should review it**, and **what Chris can do next**.

### Component risk map

| Component | What it does | Risk posture | Main governance question | Primary TAC review lane |
|---|---|---:|---|---|
| Identity matching | Scores imported records and routes them to auto-merge, review, or new-person creation | **High** | Can the system wrongly join or split persons, households, guardians, or children? | AI governance, software engineering, data science, safeguarding |
| PII sanitizer | Replaces detected identifiers before AI-assisted workflows | **High** | Does pseudonymization reduce disclosure risk enough for approved use, or does it create false confidence? | AI safety, privacy, NLP, security |
| Column auto-mapper | Suggests mappings from CSV / spreadsheet headers to FamilyGraph fields | **Moderate / Low** | Can incorrect field mapping corrupt identity or consent data before import? | Software engineering, QA, operator UX |
| Conflict review workflow | Surfaces possible matches to an operator | **High** | Does the operator exercise judgment, or mostly confirm system-shaped recommendations? | AI governance, human factors, institutional operations |
| Downstream integration API | Serves canonical identity data to consuming applications | **High** | Can one wrong identity decision propagate across applications? | Software architecture, security, product governance |
| External AI workflow support | Enables sanitized content to be used outside FamilyGraph | **High** | What data may leave the institution, under whose approval, and with what residual re-identification risk? | AI governance, privacy, legal, safeguarding |

### Rationality rule used in this section

| Claim | Required evidence before trust |
|---|---|
| “The matcher is accurate.” | Empirical performance against representative parish and school records, including children and complex households |
| “The sanitizer makes output AI-safe.” | Measured identifier recall, leakage testing, contextual re-identification testing, and approved destination policy |
| “A human reviews conflicts.” | Evidence that the reviewer saw the relevant facts, recorded reasons, had authority, and sometimes rejected the recommendation |
| “The API is safe because it is local.” | Threat model for local workstation, shared server, remote access, backups, connectors, and consuming apps |
| “The system is not AI.” | Correct but insufficient; deterministic systems still require governance when they create consequential identity assertions |

---

### Issue Card FG-AUTO-01 — Identity Matching

| Field | Review content |
|---|---|
| **Function** | Scores incoming records and routes each to `auto-merge`, `conflict queue`, or `new person`. |
| **Repository evidence** | `server/identity/matching.js`, especially `scoreMatch()` and threshold logic. |
| **Current strength** | Matching logic is inspectable, deterministic, and not a black-box model. It records reasons for conflicts and can route ambiguous cases to human review. |
| **Governance concern** | A deterministic score can still become practical authority. A false merge involving a child, custody-sensitive household, protected address, consent status, or school relationship can create real-world disclosure risk. |
| **Rationality applied** | Do not treat a confidence score as calibrated probability until empirical validation proves that relationship. Code determinism is not the same as institutional safety. |
| **Evidence gap** | No independent validation yet showing false-merge and missed-match rates across Catholic parish and school populations. |
| **TAC reviewers to engage** | AI governance, software engineering, data science, safeguarding, parish / school operations. |
| **Chris next action** | Provide or create a validation plan with representative test records, known-match labels, false-merge severity weighting, and threshold acceptance criteria. |

#### What needs to be checked

| Check | Why it matters | Suggested reviewer |
|---|---|---|
| Auto-merge threshold behavior | Determines when the system acts without review | Software engineer / QA |
| Shared email and phone handling | Parent contact fields may appear on many child records | Data / safeguarding |
| Children versus adults | Harm severity differs | AI governance / school operations |
| Compound and non-English names | Catholic institutions serve multilingual communities | Data science / pastoral operations |
| Reversibility and propagation | A wrong merge must be repairable downstream | Systems architect |
| Reviewer override rate | Detects automation bias | AI governance |

#### Minimum acceptance evidence

- A labeled test set containing true matches, false candidates, shared-contact households, children, adults, common surnames, compound surnames, protected-address cases, and conflicting household records.
- Reported precision, recall, false-merge rate, missed-match rate, and severity-weighted errors.
- Threshold rationale for `autoMerge` and `review`.
- A rule that no minor, custody-sensitive, protected-address, consent-changing, or safe-environment-linked merge auto-merges without human review unless independently validated and explicitly approved.

---

### Issue Card FG-AUTO-02 — PII Sanitizer and AI Workflow Boundary

| Field | Review content |
|---|---|
| **Function** | Replaces detected identifiers with pseudonyms before an operator uses content in an AI workflow. |
| **Repository evidence** | `server/sanitize/ner.js`, detection layers; README sanitizer limitation language. |
| **Current strength** | Uses multiple detection layers and includes Catholic-specific ecclesiastical titles such as `Fr`, `Sr`, `Rev`, `Father`, `Sister`, and `Brother`. The documentation acknowledges best-effort limits. |
| **Governance concern** | Sanitization can create false confidence. A missed identifier may silently pass into an external model, and contextual facts can still re-identify a family even when names are replaced. |
| **Rationality applied** | “Pseudonymized” is not the same as “anonymous,” “safe,” or “approved for AI.” The claim must resolve into leakage testing and destination governance. |
| **Evidence gap** | No measured miss rate, no community-specific name testing, no contextual re-identification test, and no approved AI destination policy. |
| **TAC reviewers to engage** | AI governance, NLP, security, privacy, legal, safeguarding. |
| **Chris next action** | Add an AI Export Policy and sanitizer evaluation plan before recommending any external-AI workflow involving family or student data. |

#### Sanitizer detection stack

| Layer | What it catches | Where it can fail | Required test |
|---|---|---|---|
| Regex PII | Emails, phones, SSN-shaped strings, DOBs, US addresses | Non-US formats, malformed entries, narrative identifiers | Direct identifier recall |
| Registry lookup | Known FamilyGraph names | New names not yet in registry, alternate spellings | Known-person substitution tests |
| NER library | English-language person/place entities | Non-English names, uncommon Catholic community names | Multilingual / community name corpus |
| Capitalized-token heuristic | Unrecognized name-like strings | False positives; misses lowercase or unusual formats | Precision and recall sampling |
| Operator review | Human final check | Review fatigue, false confidence, unclear instructions | Reviewer checklist and sampling protocol |

#### Minimum acceptance evidence

- Sanitizer test set drawn from realistic parish / school text.
- Direct identifier recall rate.
- False negative examples.
- False positive burden estimate.
- Contextual re-identification red-team examples.
- Policy stating which data classes may never be exported to an external AI system even after sanitization.
- Destination approval record: provider, retention, training-use terms, data-processing agreement if applicable, and approving authority.

---

### Issue Card FG-AUTO-03 — Column Auto-Mapper

| Field | Review content |
|---|---|
| **Function** | Suggests field mappings from imported CSV / spreadsheet headers. |
| **Repository evidence** | `server/sources/csv.js`, `autoMapFlat()`. |
| **Current strength** | Deterministic and operator-visible. The import preview disables import when no identity columns are detected. |
| **Governance concern** | A wrong mapping can corrupt identity, consent, DOB, phone, address, or household fields before matching begins. |
| **Rationality applied** | Human preview is a control only if the operator can understand the mapping and detect errors. |
| **Evidence gap** | No operator usability evidence showing that non-technical parish or school staff catch bad mappings reliably. |
| **TAC reviewers to engage** | Software engineering, QA, parish / school operations, UX. |
| **Chris next action** | Add import-preview warnings for sensitive fields and a required confirmation step for DOB, minor status, custody, consent, and EIM-related mappings. |

#### Minimum acceptance evidence

- Test files with ambiguous headers.
- Demonstrated rejection or warning for unsafe mappings.
- Operator-facing import checklist.
- Audit record of final mapping accepted by the operator.

---

### Issue Card FG-AUTO-04 — Human Influence in Conflict Review

| Field | Review content |
|---|---|
| **Function** | Presents ambiguous matches to an institutional operator for resolution. |
| **Repository evidence** | `server/api/conflicts.js`, conflict assignment and resolution notes. |
| **Current strength** | The operator can view candidate records, confidence, reasons, and notes. Sticky decisions preserve prior human judgment. |
| **Governance concern** | The interface may still shape the operator toward confirmation. A reviewer clicking “merge” is not evidence of independent judgment unless the record shows what evidence was seen and why the decision was made. |
| **Rationality applied** | Human presence is not human judgment. Human influence must be visible in the record. |
| **Evidence gap** | Reason recording is available but not required for high-risk decisions. No reliance telemetry exists yet. |
| **TAC reviewers to engage** | AI governance, human factors, school operations, safeguarding. |
| **Chris next action** | Require reason recording and escalation for high-risk merge categories; add telemetry for evidence viewed, review duration, override, rejection, escalation, and downstream correction. |

#### Minimum acceptance evidence

- Reviewer identity.
- Reviewer role.
- Evidence viewed.
- System recommendation.
- Reviewer reason.
- Decision outcome.
- Downstream systems affected.
- Reversal path.
- Appeal or correction link.

---

### Issue Card FG-AUTO-05 — Downstream Propagation

| Field | Review content |
|---|---|
| **Function** | Provides canonical identity data to consuming applications through a local API and integration contract. |
| **Repository evidence** | `FAMILYGRAPH_INTEGRATION.md`, `server/api/safe.js`, scoped API key implementation. |
| **Current strength** | Versioned integration contract and scoped keys show platform discipline. |
| **Governance concern** | The more useful FamilyGraph becomes, the more one wrong identity decision can propagate. That is the central platform risk. |
| **Rationality applied** | “Single source” increases both consistency and blast radius. Governance must measure both. |
| **Evidence gap** | No full downstream correction protocol showing how a wrong merge is corrected in every consuming application. |
| **TAC reviewers to engage** | Systems architecture, API engineering, product governance, incident response. |
| **Chris next action** | Add a downstream-correction playbook and a connector pause / rollback procedure. |

#### Minimum acceptance evidence

- Which consuming apps receive identity changes.
- What event is sent.
- How apps acknowledge correction.
- How failed propagation is retried.
- How a rollback or split is communicated.
- Who owns incomplete downstream correction.

---

## Technical Architecture Review Board

This section converts the architecture assessment into a review board. Each row is a concrete object for TAC scrutiny. The goal is not to make Chris read less; it is to make the review easier to act on.

### Architecture heat map

| Area | Present design | Current judgment | Main risk | Next action |
|---|---|---|---|---|
| Cryptography | AES-256-GCM, random IVs, separate HMAC lookup key | Strong v1 design | Data key cannot yet rotate | Add key-rotation and recovery plan |
| Secret storage | Local `secret.key` with restricted file mode | Acceptable for local prototype | Database and key may live together | Define OS keychain / institutional custody path |
| Audit events | General audit table plus `entity_changes` history | Useful but uneven | Not all consequential changes are transactionally coupled or complete | Map audit coverage by event type |
| EIM expiry sweep | Automated status update | Governance gap | Status changes silently, no audit event | Add audit and notification |
| Safe API | Loopback-only, no PII, no Bearer token | Good for single-machine local use | Weak if shared server or multi-user host | Define deployment profiles |
| Scoped API keys | Capability-scoped consuming-app access | Strong direction | Needs named actor and lifecycle discipline | Add key inventory and rotation rules |
| Connector security | URL and redirect restrictions for Google Sheets | Strong control | Connector trust expands attack surface | Add connector approval and pause rules |
| Supply chain | Socket Firewall install guard | Strong early control | Needs release-level evidence | Add SBOM, signed releases, vulnerability policy |
| Backup / restore | Commands exist | Useful but incomplete as governance | Restore, key custody, expired data, and succession unresolved | Add backup drill and recovery evidence |
| Browser credential model | Bearer token used by dashboard | Prototype-friendly | XSS / local storage / shared workstation concern | Move toward named-user sessions |

---

### Architecture Card FG-ARCH-01 — Cryptography and Key Lifecycle

| Field | Review content |
|---|---|
| **Evidence** | `server/crypto/encryption.js`, `server/crypto/secret.js`. |
| **Strength** | AES-256-GCM with random IVs, authenticated encryption, separate data and HMAC keys. |
| **Issue** | The master token can rotate, but `dataKey` and `hmacKey` cannot yet rotate without re-encrypting the database. |
| **Why it matters** | If the key file is compromised, historical PII remains exposed until re-encryption exists. |
| **Rationality applied** | Encryption is not a binary claim. Ask which threat it mitigates, which key is exposed, and what recovery exists after compromise. |
| **TAC lane** | Security engineering, software engineering, institutional operations. |
| **Next action** | Add a v2 key-rotation plan: re-encryption job, key versioning, recovery key, operator procedure, backup handling, and compromise playbook. |

### Architecture Card FG-ARCH-02 — Audit and Decision Reconstruction

| Field | Review content |
|---|---|
| **Evidence** | `server/audit/index.js`; `server/integration/` entity-change history. |
| **Strength** | Audit events exist; `entity_changes` provides stronger transactionally coupled history for archive, reinstate, merge, and split paths. |
| **Issue** | General `audit_events` are not uniformly transactionally coupled to every data write. Some consequential state changes may lack the decision evidence required for institutional reconstruction. |
| **Why it matters** | Families and institutions need to know who changed what, why, with what evidence, and how it can be corrected. |
| **Rationality applied** | “Auditable” must resolve into a reconstructable decision chain, not merely an event table. |
| **TAC lane** | Software engineering, AI governance, incident response. |
| **Next action** | Produce an audit coverage matrix: event type, transactionality, actor, reason, before/after values, downstream effects, retention, and appeal usefulness. |

### Architecture Card FG-ARCH-03 — EIM / Safe-Environment Status

| Field | Review content |
|---|---|
| **Evidence** | `server/identity/eim.js`, `recomputeStatus()`. |
| **Strength** | The system can track certification status and expiry. |
| **Issue** | Automated expiry status changes appear to update records without an audit event or operator notification. |
| **Why it matters** | Safe-environment status affects who may serve around minors. Silent status changes are weak governance. |
| **Rationality applied** | A status field is not accountability. The institution must reconstruct when the status changed, why, and who was notified. |
| **TAC lane** | Safeguarding, school operations, software engineering, diocesan policy. |
| **Next action** | Add audit event, notification, and report surface for EIM status changes; clarify that FamilyGraph records status but does not determine diocesan eligibility. |

### Architecture Card FG-ARCH-04 — Local API and Deployment Profile

| Field | Review content |
|---|---|
| **Evidence** | `server/api/safe.js`; loopback-only middleware. |
| **Strength** | Local-only access and `includePii: false` are good defaults for a single-machine deployment. |
| **Issue** | Loopback-only is not the same as authenticated multi-user governance. Any local process on the same host may become relevant to the threat model. |
| **Why it matters** | A single-user workstation, shared office computer, parish server, and remote-access deployment are different risk classes. |
| **Rationality applied** | Do not let “local” collapse several deployment realities into one safety claim. |
| **TAC lane** | Systems architecture, security, cloud / Linux, parish IT operations. |
| **Next action** | Define supported deployment profiles: local single operator, shared workstation, institutional server, remote access, and unsupported configurations. State required controls for each. |

### Architecture Card FG-ARCH-05 — Supply Chain and Release Integrity

| Field | Review content |
|---|---|
| **Evidence** | `scripts/preinstall-sfw-check.js`; dependency and install guidance. |
| **Strength** | Enforced dependency screening is better than a documentation-only recommendation. |
| **Issue** | CDCF endorsement would require release-level assurance, not only install-time dependency screening. |
| **Why it matters** | Institutions need to know what they are running, whether it changed, whether dependencies are vulnerable, and how emergency fixes are distributed. |
| **Rationality applied** | Supply-chain trust must be reproducible by downstream adopters, not dependent on the original developer’s local environment. |
| **TAC lane** | Open-source maintainers, security engineering, DevOps. |
| **Next action** | Add SBOM, release checksums, signed tags or releases, vulnerability disclosure policy, supported-version matrix, and emergency patch procedure. |

### Architecture Card FG-ARCH-06 — Backups, Recovery, and Institutional Succession

| Field | Review content |
|---|---|
| **Evidence** | Backup / restore commands and local data design. |
| **Strength** | Local operation gives institutions control and avoids unnecessary vendor centralization. |
| **Issue** | Local control also creates local recovery obligations: keys, backups, restore testing, staff turnover, and record retention. |
| **Why it matters** | A family identity registry becomes critical infrastructure once downstream apps depend on it. Losing the database or key can become an institutional failure. |
| **Rationality applied** | Subsidiarity means local authority with local competence, not merely local possession of files. |
| **TAC lane** | Institutional operations, security, systems administration. |
| **Next action** | Require a restore drill, backup encryption procedure, key custody plan, staff succession path, and offboarding procedure before live deployment. |

### Architecture reviewer routing

| Reviewer lens | Best-fit TAC expertise | Questions to answer |
|---|---|---|
| Software correctness | Matthew Ayers, Jeff Geerling, Mike Kasberg, Randy Danielson, Gabriel Dorta, other engineers | Are the controls implemented as described? Are tests adequate? What failure paths are missing? |
| AI / data science / knowledge graph | Diglio Simoni, Tomislav Karačić, Riccardo Petricca, AI-focused reviewers | Are matching, identity graph, and downstream propagation assumptions valid? What evaluation is required? |
| Security / DevOps / open source | Jeff Geerling, Randy Danielson, Matthew Ayers, other infrastructure reviewers | Are release, dependency, deployment, backup, and credential controls production-worthy? |
| Canonical / ecclesial / safeguarding | Ecclesial Advisory Council and safeguarding-domain reviewers | Does the data model exceed local authority? What fields require diocesan or ecclesial review? |
| AI governance | Mark Banasihan and other governance reviewers | Does the system preserve human influence, appeal, correction, risk thresholds, and post-harm reform? |
| Privacy / data protection | Data-protection and legal reviewers | What laws, notices, retention rules, and processing limits apply by deployment profile? |

## Human Control Architecture: From Operator Review to Accountable Judgment

FamilyGraph already has a meaningful human-control surface: ambiguous matches can be routed to an operator, the operator can inspect candidate records, and sticky decisions can preserve a prior resolution. That is a real strength.

The governance question is narrower and harder:

> Can FamilyGraph prove that a named, authorized human exercised judgment with evidence, authority, reasons, and correction duties?

This section turns the human-control review into cards.

---

### Human Control Summary

| Control layer | Current posture | Governance status | Next action |
|---|---|---|---|
| Conflict queue | Exists and appears useful | Strong starting point | Add high-risk routing and mandatory reasons |
| Evidence display | Candidate records and reasons appear available | Partial | Prove what evidence the reviewer saw |
| Operator authority | Operator can resolve conflicts | Partial | Tie authority to named role and institution |
| Reason recording | Available | Partial | Require for high-risk decisions |
| Sticky decisions | Preserves prior human decision | Useful but risky | Add review / expiration rules for high-risk cases |
| Family correction path | Not sufficiently documented | Gap | Add intake, appeal, correction, and downstream repair process |
| Reliance monitoring | Not evident | Gap | Add telemetry for acceptance, rejection, escalation, review time |
| Downstream repair | Not sufficiently documented | Gap | Add correction propagation evidence |

---

### Human Control Card HC-01 — Conflict Review Is a Control, Not a Complete Governance System

| Field | Review content |
|---|---|
| **Current strength** | The conflict queue can route ambiguous identity matches to a human operator. |
| **Evidence to verify** | `server/api/conflicts.js`, conflict assignment, resolution notes, sticky decision handling. |
| **Governance concern** | A conflict queue protects only the cases that reach it. Auto-merge thresholds, UI defaults, reviewer incentives, and downstream propagation can still weaken judgment. |
| **Rationality applied** | Human involvement is not the same as human judgment. |
| **Chris next action** | Document which cases must always enter review even when the matcher score is high. |
| **TAC prompt** | Which cases should be prohibited from auto-merge? |

#### Suggested mandatory-review classes

| Class | Rationale |
|---|---|
| Minor records | Higher harm severity |
| Custody or guardianship conflict | Wrong linkage can disclose to unauthorized adult |
| Protected address | Disclosure risk |
| Consent-changing merge | A merge may alter directory, photo, or contact permissions |
| Safe-environment / EIM-linked person | Ministry access implications |
| Conflicting DOB | Strong identity conflict |
| Shared email or phone as primary signal | Common family pattern; weak individual identity evidence |
| Multiple active households | Context-sensitive family reality |
| Prior “different person” decision | Human judgment already found ambiguity |

---

### Human Control Card HC-02 — Named-Human Accountability

| Field | Review content |
|---|---|
| **Current strength** | The system records actors and supports scoped application keys. |
| **Governance concern** | A generic dashboard actor, shared workstation, or bearer token cannot carry moral and institutional responsibility. |
| **Required control** | Named authentication, role, authority domain, MFA for privileged users, and attribution for every consequential action. |
| **Rationality applied** | If an affected family asks “who decided this?”, the system must answer with a responsible person or office, not merely a process. |
| **Chris next action** | Provide an operator identity model and authority matrix. |
| **TAC prompt** | Would the attribution satisfy a pastor, principal, diocesan office, safeguarding reviewer, and affected family? |

---

### Human Control Card HC-03 — Independent Judgment

| Field | Review content |
|---|---|
| **Current strength** | Reviewers can see match reasons and record notes. |
| **Governance concern** | Optional notes may not prove independent reasoning. High acceptance rates may reveal automation bias. |
| **Required control** | Mandatory reason recording for high-risk cases; review-time and evidence-view telemetry; acceptance/rejection/escalation metrics. |
| **Rationality applied** | A click is not a judgment unless the record shows what the reviewer evaluated and why. |
| **Chris next action** | Add required reason fields and reliance telemetry for high-risk decisions. |
| **TAC prompt** | What evidence would show that the reviewer disagreed with the system when appropriate? |

---

### Human Control Card HC-04 — Appeal and Family Contestability

| Field | Review content |
|---|---|
| **Current strength** | Technical correction mechanisms appear possible through merge/split/reversal patterns. |
| **Governance concern** | Families need a visible process to report identity errors. Technical reversibility does not equal appeal. |
| **Required control** | Family-facing correction path: intake, evidence, investigator, timeline, escalation, correction, downstream propagation, closure. |
| **Rationality applied** | A system is not correctable if affected persons cannot discover or contest the error. |
| **Chris next action** | Add a `FAMILY_CORRECTION_PROCESS.md` or equivalent governance note. |
| **TAC prompt** | Could a parent with limited technical knowledge successfully use this process? |

---

### Human Control Card HC-05 — Downstream Repair

| Field | Review content |
|---|---|
| **Current strength** | FamilyGraph has a versioned integration contract and change-event architecture. |
| **Governance concern** | A corrected record in FamilyGraph does not repair harm if consuming applications retain stale data. |
| **Required control** | Downstream correction acknowledgement, retry, exception queue, and unresolved-correction owner. |
| **Rationality applied** | Repair is complete only when the consequences of the error have been corrected, not when the source row changes. |
| **Chris next action** | Add downstream correction playbook and test it with at least one consuming app. |
| **TAC prompt** | Can the institution prove that each dependent system received and applied the correction? |

---

### Human Control Card HC-06 — Human Influence Telemetry Minimum Schema

| Field group | Minimum fields |
|---|---|
| **Case identity** | event ID, person IDs, household IDs, source system, import batch |
| **System output** | candidate match, score, threshold, reasons, conflicting signals |
| **Evidence access** | records opened, provenance viewed, protected-data flags seen |
| **Reviewer identity** | named user, role, institution, authority domain |
| **Judgment** | decision, reason, confidence, review duration, escalation |
| **Command** | authority exercised, downstream effect, rollback path |
| **Contestability** | correction request ID, appeal owner, deadline |
| **Repair** | corrected systems, notifications, unresolved propagation |
| **Reform** | rule change, threshold change, training, revalidation |

**Implementation note:** This schema does not need to be fully implemented before incubation, but it should govern the design of any live-family-data pilot.

---

## Gate 1 Criterion Analysis: Incubation Readiness

Gate 1 should answer one narrow question:

> Should FamilyGraph become an official CDCF candidate project under a bounded, evidence-producing incubation plan?

Gate 1 is not production approval. It is not broad endorsement. It is not a declaration that FamilyGraph is safe for all Catholic institutions. The CDCF lifecycle states that incubation requires Criterion 1 mission alignment and a plan for satisfying Criteria 2–6; graduation requires all eight criteria and operational readiness for wide deployment.

### Gate 1 status board

| Criterion | Incubation question | Current finding | Gate 1 disposition | Required response |
|---|---|---|---|---|
| **C1 Mission Alignment** | Does the project serve a Catholic institutional need without exceeding canonical scope? | Yes, with language and authority boundaries | **Pass with conditions** | Bound “source of truth” claims and prohibited uses |
| **C2 Human Accountability** | Is there a credible plan for named-human accountability? | Partial control surface; incomplete accountability | **Plan required** | Named-user and authority design |
| **C3 Transparency** | Can reviewers understand scope, operation, and limits? | Strong docs; several scope clarifications needed | **Partial** | Correct threshold docs and AI/LLM boundary language |
| **C4 Independent Validation** | Is there a credible plan for independent validation? | No completed validation; plan needed | **Plan required** | Matching and sanitizer validation protocol |
| **C5 Vulnerable Populations** | Does the project acknowledge and plan for vulnerable-family risks? | Risks identified; no evidence package | **Plan required** | Child / complex-family risk plan |
| **C6 Deployment Governance** | Is there a credible plan for deployment controls and stopping rules? | Not yet sufficient | **Plan required** | Pilot protocol, escalation triggers, correction process |

---

### Gate 1 Card C1 — Mission Alignment and Canonical Scope

| Field | Review content |
|---|---|
| **Finding** | FamilyGraph addresses a real and reusable Catholic institutional identity problem. |
| **Strength** | It does not appear to automate sacraments, doctrine, pastoral judgment, or canonical eligibility. |
| **Concern** | “Source of truth” language can imply authority over facts that belong to school, parish, diocesan, civil, or family authorities. |
| **Gate 1 requirement** | Replace broad authority language with bounded registry language and list prohibited inferences. |
| **Suggested disposition** | Pass with conditions. |

**Required prohibited-use examples**

- sacramental eligibility inference;
- canonical standing inference;
- ministry fitness inference;
- custody decision-making;
- school enrollment decision-making;
- donor targeting based on sensitive family structure;
- external AI processing of child data without separate approval.

---

### Gate 1 Card C2 — Human Accountability

| Field | Review content |
|---|---|
| **Finding** | Human review exists, but named-human accountability is not yet demonstrated. |
| **Strength** | Conflict workflow can preserve operator judgment. |
| **Concern** | A generic operator or shared credential cannot satisfy affected-family accountability. |
| **Gate 1 requirement** | Submit a named-human accountability design for live pilot. |
| **Gate 2 requirement preview** | Implement and test named authentication, role authority, reason recording, appeal ownership, and remediation ownership. |
| **Suggested disposition** | Plan required before incubation; implementation required before live-family-data pilot. |

---

### Gate 1 Card C3 — Transparency of Scope and Operation

| Field | Review content |
|---|---|
| **Finding** | Documentation is unusually strong for an early project. |
| **Strength** | Architecture, security, API, and session notes provide meaningful review surface. |
| **Concern** | Threshold discrepancy and AI/LLM boundary language can mislead adopters. |
| **Gate 1 requirement** | Correct documentation and add a one-page scope boundary. |
| **Gate 2 requirement preview** | Provide complete data inventory, data-flow diagrams, authority matrix, and deployment profile documentation. |
| **Suggested disposition** | Partial; remediable. |

---

### Gate 1 Card C4 — Independent Validation

| Field | Review content |
|---|---|
| **Finding** | Internal tests do not substitute for independent validation. |
| **Strength** | Test coverage appears serious and useful for engineering confidence. |
| **Concern** | Matching and sanitizer performance are unproven for representative Catholic parish and school populations. |
| **Gate 1 requirement** | Submit validation plan with reviewer independence, datasets, metrics, and thresholds. |
| **Gate 2 requirement preview** | Complete validation and publish results, limitations, and remediation. |
| **Suggested disposition** | Plan required. |

---

### Gate 1 Card C5 — Vulnerable Populations

| Field | Review content |
|---|---|
| **Finding** | Children, complex families, protected addresses, and multilingual communities are foreseeable affected groups. |
| **Strength** | The project recognizes family and school context. |
| **Concern** | No child-impact assessment or subgroup performance evidence is present. |
| **Gate 1 requirement** | Submit vulnerable-family risk plan and high-risk merge classes. |
| **Gate 2 requirement preview** | Complete child-impact assessment, scenario testing, subgroup analysis, and safeguarding review. |
| **Suggested disposition** | Plan required. |

---

### Gate 1 Card C6 — Deployment Governance

| Field | Review content |
|---|---|
| **Finding** | Technical deployment exists; deployment governance is incomplete. |
| **Strength** | Local-first posture and scoped API architecture support subsidiarity. |
| **Concern** | No complete pilot protocol, escalation threshold, stopping rule, or family correction process. |
| **Gate 1 requirement** | Submit pilot governance note: who owns deployment, when to pause, how families report errors, and what stops the system. |
| **Gate 2 requirement preview** | Demonstrate live governance record, incident exercise, correction propagation, and reviewer telemetry. |
| **Suggested disposition** | Plan required. |

---

### Gate 1 Recommendation

| Field | Entry |
|---|---|
| **Recommended status** | Conditional incubation may be considered after the Gate 1 response package is received. |
| **Not approved** | Production endorsement, wide institutional deployment, diocesan aggregation, external-AI workflows with real family data, or Gate 2 graduation. |
| **Gate 1 response package** | C1 scope correction; C2 accountability design; C3 documentation corrections; C4 validation plan; C5 vulnerable-family plan; C6 pilot governance note. |
| **Review standard** | Plans may satisfy incubation. Evidence is required for pilot and Gate 2. |
| **TAC action** | Invite Chris response, assign reviewer lanes, identify independent reviewers, and record conflicts / recusals. |

---

## Gate 2 Graduation Analysis: Active CDCF Project Readiness

Gate 2 answers a different question:

> Has FamilyGraph demonstrated operational readiness and long-term sustainability such that it can become an active CDCF project considered ready for wide-scale deployment across Catholic institutions?

On the current evidence, the answer is **no**.

That is not a condemnation of the project. It is a recognition that Gate 2 requires implemented controls, independent evidence, sustainable governance, and deployment maturity. Gate 2 cannot be satisfied by plans alone.

### Gate 2 status board

| Criterion | Gate 2 standard | Current status | Required before graduation |
|---|---|---|---|
| **C1 Mission Alignment** | Scope remains bounded across real deployments | Partial | Prohibited-use policy and authority boundaries tested in pilot |
| **C2 Human Accountability** | Named humans exercise accountable judgment | Not met | Authentication, RBAC, reason recording, appeal and repair ownership |
| **C3 Transparency** | Independent reviewers and adopters can understand operation and limits | Partial | Data inventory, flow diagrams, deployment profiles, AI-export boundaries |
| **C4 Independent Validation** | Claimed capabilities independently tested | Not met | Matching, sanitizer, security, and deployment reviews completed |
| **C5 Vulnerable Populations** | Children and vulnerable families specifically evaluated and protected | Not met | Child-impact assessment, subgroup tests, safeguarding review |
| **C6 Deployment Governance** | Live governance process tested | Not met | Pilot record, stopping rules, incident exercise, correction propagation |
| **C7 Data Stewardship** | Data lifecycle, privacy, security operations, breach response mature | Not met | Retention, deletion, backup, key, breach, legal, support procedures |
| **C8 Maintenance and Sustainability** | Project governed by durable maintainers / PMC | Not met | PMC or equivalent, maintainer succession, release process, support model |

---

### Gate 2 Card C7 — Data Stewardship

| Field | Review content |
|---|---|
| **Finding** | Security engineering exists, but institutional data stewardship is incomplete. |
| **Gate 2 requirement** | Data inventory, retention schedule, deletion process, backup/restore evidence, key custody, breach response, legal review, support-access rules. |
| **Why it matters** | Local-first architecture moves stewardship duties to the institution. Without operational procedures, locality becomes unmanaged risk. |
| **Evidence required** | Versioned policies, restore drill, key recovery procedure, incident tabletop, downstream deletion handling. |
| **Suggested disposition** | Not met. |

---

### Gate 2 Card C8 — Maintenance, Sustainability, and Commons Governance

| Field | Review content |
|---|---|
| **Finding** | The open-source artifact is promising, but durable stewardship is not established. |
| **Gate 2 requirement** | Named maintainer, backup maintainer, PMC path, release authority, security response, supported-version policy, commercial/open-source boundary, adopter exit plan. |
| **Why it matters** | A family identity registry becomes infrastructure. CDCF cannot graduate infrastructure that depends on unclear single-maintainer continuity. |
| **Evidence required** | Maintainer statement, governance charter, release process, security disclosure process, licensing/IP path, support boundaries. |
| **Suggested disposition** | Not met. |

---

### Gate 2 Evidence Case

Gate 2 should require an assurance case organized around these claims.

| Claim | Evidence required |
|---|---|
| **A. Identity resolution works for approved use** | Independent benchmark, calibrated thresholds, subgroup and family-structure analysis |
| **B. Human judgment remains real** | Named users, review records, override rates, reasons, escalation, reliance telemetry |
| **C. Families can correct errors** | Notice, intake, appeal, deadlines, correction test, downstream propagation |
| **D. Children and vulnerable families are protected** | Child-impact assessment, high-risk merge policy, safeguarding review |
| **E. AI export does not create unacceptable disclosure risk** | Sanitizer evaluation, AI destination policy, data-processing terms, prohibited data classes |
| **F. The system remains correctable** | Rollback, split, restore, connector pause, incident exercise, system reform records |
| **G. The project is sustainable** | PMC, maintainers, release integrity, security response, SBOM, support/deprecation plan |

---

### Gate 2 Non-Negotiables

FamilyGraph should not graduate while any of the following remain unresolved:

| Blocking condition | Reason |
|---|---|
| No named-human accountability for consequential actions | Cannot preserve institutional responsibility |
| No independent validation of matching | Cannot justify family-data linkage |
| No vulnerable-family safeguards | Children and complex households bear the downside risk |
| No family correction and appeal process | Affected persons cannot contest representation |
| No downstream correction playbook | Errors may persist outside the source registry |
| No data lifecycle and breach plan | Local control lacks operational stewardship |
| No maintainer succession | Commons infrastructure becomes single-person dependency |
| No AI-export governance | Pseudonymization may become permission theater |
| No stopping rules | Monitoring can become motivated continuation |

---

### Gate 2 Reviewer Assignment

| Gate 2 domain | Primary reviewer lane | Suggested evidence owner |
|---|---|---|
| Matching validation | Data science / knowledge graph / software engineering | Independent technical reviewer |
| Sanitizer and AI export | AI governance / NLP / privacy | Independent AI safety or privacy reviewer |
| Security and release | Security / DevOps / open source | Security reviewer / maintainer |
| Human influence telemetry | AI governance / human factors | TAC governance reviewer |
| Child and safeguarding review | School / diocesan / safeguarding | Safeguarding authority |
| Data stewardship | Privacy / legal / institutional operations | Deploying institution |
| Maintenance and PMC | Open-source governance / CDCF Board | Project owner / CDCF |

---

### Gate 2 Recommendation

| Field | Entry |
|---|---|
| **Current Gate 2 status** | No-go / not ready. |
| **Reason** | Gate 2 requires evidence, not plans. FamilyGraph has not yet demonstrated independent validation, named-human accountability, vulnerable-family protection, deployment governance, data stewardship, or durable project governance. |
| **Path forward** | Use Gate 1 incubation to produce the Gate 2 assurance case. |
| **Board communication** | Do not present incubation as endorsement or production readiness. |

---

## Open Source and Commercial Boundary

**Observation: The Apache-2.0 license was applied on June 3, 2026.** The session notes record that the project was developed as UNLICENSED from April 27 through June 3, 2026. The open-source decision was made six weeks into development, in the same session that scrubbed real data from test fixtures and softened the sanitizer language before public release. The license commitment is real, legally binding, and documented. It is also recent.

**Observation: Chris has stated explicitly he does not intend to continue developing FamilyGraph.**

The WhatsApp session records: "I don't really see spending a lot more time on familygraph. If others want to run with it and develop it further, I'm 100% open to it. I'm more interested in the app layer."

C8 at Gate 2 requires a named maintainer who accepts public accountability and documentation of what happens to CDCF-endorsed deployments if the maintainer is unavailable. That question is already live, not hypothetical.

**Inference: The commercial/open-source boundary requires explicit documentation.**

The session notes record that Chris is "thinking very seriously about commercializing the education parts but open sourcing a lot of the church infrastructure." FamilyGraph and the parent-engagement application (ParishBrain) are architecturally coupled in the business spec and share the same integration contract. If the education layer is commercialized under different terms than the church infrastructure layer, deploying institutions need to know which components they depend on and under what terms.

**Required before formal TAC finding:** A written statement from Chris clarifying the scope of any intended commercial layer, confirming that FamilyGraph's core identity infrastructure will remain Apache-2.0 or equivalent, and identifying a named backup maintainer or describing a succession path for the open-source layer.

---

## Response Dashboard for Chris and TAC Reviewers

This replaces a long conditions list with a response dashboard. Chris can use the **Owner Response** column directly in a pull request or issue. TAC members can comment by finding ID.

### How to use this dashboard

1. Chris responds in the **Owner Response** column or links to a GitHub issue / pull request.
2. TAC reviewers add comments under the relevant finding ID.
3. A finding remains `OPEN` until evidence is provided and reviewed.
4. A plan may satisfy incubation readiness; implementation and independent evidence are required for live-family-data use or Gate 2.
5. Disputed findings stay visible. Do not erase the disagreement; add counterevidence.

### Priority legend

| Priority | Meaning |
|---|---|
| **P0** | Blocks live-family-data pilot or broad endorsement |
| **P1** | Blocks Gate 2 or production readiness |
| **P2** | Should be addressed during incubation |
| **P3** | Documentation or maintainability improvement |

### Review status legend

| Status | Meaning |
|---|---|
| `OPEN` | Finding awaiting response |
| `OWNER RESPONSE RECEIVED` | Chris has responded |
| `EVIDENCE REQUESTED` | More proof needed |
| `REMEDIATION PROPOSED` | Fix proposed but not verified |
| `REMEDIATION VERIFIED` | Fix reviewed against evidence |
| `DISPUTED` | Reviewer and owner disagree |
| `ACCEPTED RISK` | Risk accepted by proper authority |
| `CLOSED` | No further action required |
| `SUPERSEDED` | Replaced by later finding |

---

### Executive action board

| ID | Priority | Action | Why it matters | Required evidence | Owner Response | TAC Review Lane | Status |
|---|---:|---|---|---|---|---|---|
| FG-RSP-01 | P1 | Correct and bound project claims | Prevents overtrust in “source of truth,” “AI-safe,” or “local-first” language | Updated README / product spec / integration doc | — | AI governance + product | OPEN |
| FG-RSP-02 | P0 | Provide independent validation plan | Matching and sanitization claims require evidence outside the development loop | Validation protocol, sample design, metrics, reviewer independence | — | AI safety + data science | OPEN |
| FG-RSP-03 | P0 | Implement named-human accountability plan | A dashboard actor or shared token cannot carry family-data responsibility | Auth design, role map, MFA, action attribution | — | Security + governance | OPEN |
| FG-RSP-04 | P0 | Define family correction and appeal process | Families need a path to contest identity errors and disclosures | Process doc, timelines, audit linkage, downstream correction | — | Safeguarding + operations | OPEN |
| FG-RSP-05 | P0 | Create field-level authority matrix | Prevents local software from overriding school, diocesan, legal, or family authority | Matrix by field and source | — | Canonical + data governance | OPEN |
| FG-RSP-06 | P0 | Add vulnerable-family safeguards | Children, protected addresses, and custody-sensitive records require higher thresholds | High-risk merge rules and escalation triggers | — | Safeguarding + AI governance | OPEN |
| FG-RSP-07 | P0 | Add deployment stopping rules | Prevents “monitoring” from becoming motivated continuation | Pilot protocol with suspension thresholds | — | TAC + institution | OPEN |
| FG-RSP-08 | P1 | Add data stewardship plan | Retention, deletion, backup, breach, and key custody must be institutionalized | Data lifecycle and incident response docs | — | Privacy + security | OPEN |
| FG-RSP-09 | P1 | Add maintenance and succession plan | Project cannot become CDCF infrastructure around one maintainer | Maintainer roster, PMC path, release process | — | Open source + Board | OPEN |
| FG-RSP-10 | P1 | Add human influence telemetry | Proves whether human review is judgment or confirmation | Telemetry schema and sample records | — | AI governance | OPEN |
| FG-RSP-11 | P1 | Add downstream correction playbook | One wrong merge may propagate across apps | Event, rollback, acknowledgement, and retry process | — | Systems architecture | OPEN |
| FG-RSP-12 | P1 | Add release-integrity package | Institutions need reproducible trust in what they run | SBOM, signed release, checksums, VDP, supported versions | — | Security + DevOps | OPEN |

---

### FG-RSP-01 — Correct and Bound Project Claims

| Field | Content |
|---|---|
| **Question for Chris** | What exactly is FamilyGraph authoritative for, and what does it never decide? |
| **Why this matters** | The phrase “source of truth” can overstate institutional authority. A registry may reconcile records without owning every fact’s moral, legal, school, parish, or diocesan authority. |
| **Requested action** | Replace broad “source of truth” language with “governed institutional identity registry” or equivalent bounded language. |
| **Minimum content** | Identity equivalence, household membership, guardianship, access authority, directory visibility, consent, EIM status, and school context must be separated. |
| **TAC reviewer prompt** | Does the revised language prevent downstream apps from treating FamilyGraph as authority over fields it merely records? |

---

### FG-RSP-02 — Independent Validation Plan

| Field | Content |
|---|---|
| **Question for Chris** | How will we know the matcher and sanitizer work for real Catholic parish and school populations? |
| **Why this matters** | Internal tests establish software consistency. They do not establish population-level safety. |
| **Requested action** | Submit a validation plan before incubation; complete validation before broad deployment. |
| **Minimum metrics** | Precision, recall, false-merge rate, missed-match rate, severity-weighted child / custody / protected-address errors, sanitizer direct-identifier recall, contextual re-identification examples. |
| **TAC reviewer prompt** | Are the test populations representative enough for the intended deployment scope? |

---

### FG-RSP-03 — Named-Human Accountability

| Field | Content |
|---|---|
| **Question for Chris** | Can every consequential action be traced to a named person with a defined institutional role and authority? |
| **Why this matters** | Human accountability fails when a token, shared workstation, or generic actor stands in for a responsible person. |
| **Requested action** | Provide authentication and authorization design. |
| **Minimum content** | Named users, roles, MFA for privileged users, role separation, mandatory reasons for high-risk actions, session revocation, credential lifecycle. |
| **TAC reviewer prompt** | Would this record satisfy an affected family, school leader, pastor, diocesan office, or incident reviewer? |

---

### FG-RSP-04 — Family Correction, Appeal, and Repair

| Field | Content |
|---|---|
| **Question for Chris** | What happens when a family says the system is wrong? |
| **Why this matters** | A rollback button is not an appeal process. Families need a visible route to correction. |
| **Requested action** | Add a family error and correction process. |
| **Minimum content** | Intake, reviewer, evidence required, timeline, escalation, correction, downstream propagation, notification, closure record. |
| **TAC reviewer prompt** | Could a non-technical parent use this process without understanding the database? |

---

### FG-RSP-05 — Field-Level Authority Matrix

| Field | Content |
|---|---|
| **Question for Chris** | Which source is authoritative for each field, and who may override it? |
| **Why this matters** | Provenance says where data came from. It does not say who has authority over it. |
| **Requested action** | Create an authority matrix. |
| **Minimum content** | Field, authoritative source, proposing source, reviewer role, conflict resolver, retention, disclosure rule, matching eligibility, AI-export eligibility. |
| **TAC reviewer prompt** | Are school, parish, diocesan, family, and legal authorities properly separated? |

---

### FG-RSP-06 — Vulnerable-Family Safeguards

| Field | Content |
|---|---|
| **Question for Chris** | Which records must never be auto-merged or disclosed without heightened review? |
| **Why this matters** | Children, protected addresses, custody-sensitive relationships, and safe-environment statuses change the severity of error. |
| **Requested action** | Add high-risk record classes and mandatory escalation rules. |
| **Minimum content** | Minors, contested custody, guardianship conflict, foster / adoptive cases, protected address, conflicting DOB, shared contact, consent change, EIM / safe-environment data. |
| **TAC reviewer prompt** | Does the safeguard protect the least powerful family in the dataset, not only the average case? |

---

### FG-RSP-07 — Deployment Stopping Rules

| Field | Content |
|---|---|
| **Question for Chris** | What evidence forces the institution to pause, restrict, or stop the system? |
| **Why this matters** | Without predefined thresholds, monitoring can become a way to continue despite warning signs. |
| **Requested action** | Add pilot stopping rules. |
| **Minimum triggers** | Unauthorized disclosure, child-to-wrong-household attachment, inability to identify actor, sanitizer direct-identifier leakage, key compromise, failed downstream correction, unexplained auto-merge spike. |
| **TAC reviewer prompt** | Are the thresholds concrete enough that a pastor, principal, or operator knows when to stop? |

---

### FG-RSP-08 — Data Stewardship and Security Operations

| Field | Content |
|---|---|
| **Question for Chris** | Who owns the data lifecycle after deployment? |
| **Why this matters** | Local-first architecture transfers stewardship duties to the institution. |
| **Requested action** | Add data lifecycle and incident-response documentation. |
| **Minimum content** | Retention, deletion, legal hold, backup encryption, restore test, key custody, breach response, safeguarding escalation, support access, version support. |
| **TAC reviewer prompt** | Could a parish or school operate this safely after the original developer leaves? |

---

### FG-RSP-09 — Maintenance, Succession, and Commercial Boundary

| Field | Content |
|---|---|
| **Question for Chris** | Who maintains FamilyGraph, what remains open source, and what happens if the original maintainer steps away? |
| **Why this matters** | CDCF infrastructure cannot depend on unclear stewardship or commercial coupling. |
| **Requested action** | Provide maintainer and licensing statement. |
| **Minimum content** | Maintainer, backup maintainer, PMC path, release authority, support boundary, commercial layer boundary, license continuity, adopter exit path. |
| **TAC reviewer prompt** | Is this viable as a commons project rather than a single-founder artifact? |

---

### FG-RSP-10 — Human Influence Telemetry

| Field | Content |
|---|---|
| **Question for Chris** | Can the system show where human counsel, judgment, and command occurred? |
| **Why this matters** | Human review becomes ceremonial when the record shows only acceptance, not reasoning. |
| **Requested action** | Add telemetry specification and sample records. |
| **Minimum fields** | Evidence viewed, recommendation, reviewer role, review time, reason, accept / reject / override / escalate, downstream effect, appeal, remediation, system change. |
| **TAC reviewer prompt** | Could this data reveal automation bias or overreliance? |

---

### FG-RSP-11 — Downstream Correction Playbook

| Field | Content |
|---|---|
| **Question for Chris** | How does a corrected identity propagate to every consuming application? |
| **Why this matters** | A corrected source record does not repair harm if downstream apps keep stale identity data. |
| **Requested action** | Add downstream correction protocol. |
| **Minimum content** | Event type, consuming app acknowledgement, failed-delivery retry, manual reconciliation, audit of completion, owner for unresolved corrections. |
| **TAC reviewer prompt** | Can the institution prove that the correction reached every dependent system? |

---

### FG-RSP-12 — Release Integrity and Supply Chain

| Field | Content |
|---|---|
| **Question for Chris** | How does an institution know that the release it installed is authentic, supported, and inspectable? |
| **Why this matters** | Open-source trust requires release discipline, not only public code. |
| **Requested action** | Add release-integrity package. |
| **Minimum content** | SBOM, signed tags or releases, checksums, vulnerability disclosure policy, supported-version matrix, emergency patch process. |
| **TAC reviewer prompt** | Would a school or diocese be able to respond quickly to a dependency vulnerability? |

---

### Evidence package checklist

| Evidence type | Incubation | Live-family-data pilot | Gate 2 |
|---|---:|---:|---:|
| Corrected project claims | Required | Required | Required |
| Independent validation plan | Required | Required | Required |
| Independent validation results | Planned | Partial / scoped | Completed |
| Named-user accountability | Design | Required | Required |
| Family correction process | Design | Required | Required |
| Field authority matrix | Design | Required | Required |
| Vulnerable-family safeguards | Design | Required | Required |
| Stopping rules | Design | Required | Required |
| Data stewardship plan | Plan | Risk-based minimum | Completed |
| Security operations plan | Plan | Risk-based minimum | Completed |
| Maintenance and succession | Plan | Named support | Completed |
| Human influence telemetry | Specification | Required subset | Completed |
| Downstream correction playbook | Specification | Required subset | Completed |
| Independent review reports | Plan | Scoped | Completed |

---

### TAC reviewer assignment board

| Review lane | Suggested reviewers / expertise | Primary finding IDs |
|---|---|---|
| Software correctness and test design | Software engineers, open-source maintainers, QA reviewers | FG-AUTO-01, FG-AUTO-03, FG-ARCH-02, FG-RSP-02 |
| Security and deployment | Linux / cloud / DevOps / security reviewers | FG-ARCH-01, FG-ARCH-04, FG-ARCH-05, FG-ARCH-06, FG-RSP-08, FG-RSP-12 |
| AI governance and AI safety | AI governance, AI safety, human-influence review | FG-AUTO-01, FG-AUTO-02, FG-AUTO-04, FG-RSP-07, FG-RSP-10 |
| Data science / knowledge graph | AI, knowledge graph, matching, computational modeling | FG-AUTO-01, FG-AUTO-05, FG-RSP-02, FG-RSP-11 |
| Safeguarding and vulnerable families | School, diocesan, safe-environment, pastoral operations | FG-AUTO-04, FG-ARCH-03, FG-RSP-04, FG-RSP-06 |
| Canonical / ecclesial review | Ecclesial Advisory Council and canonical advisors | FG-RSP-01, FG-RSP-05 |
| Privacy / legal / data protection | DPO, privacy counsel, education law reviewers | FG-AUTO-02, FG-RSP-05, FG-RSP-08 |

---

## Architectural Strengths

The following design decisions reflect governance-aware engineering that the vetting criteria are designed to identify.

| Architecture | Location | Why It Matters |
|---|---|---|
| entity_changes writes are transactionally atomic | `server/integration/` (v13 hardening) | A history.record() failure rolls back the data write. No path exists where an archive, reinstate, or merge operation lacks a corresponding change record. |
| PII vs. pseudonym is a deployment posture | `server/api/safe.js`; dashboard toggle | AI workflows are architecturally forced to use pseudonyms. Export of PII requires explicit consent and tier-2 audit logging. The posture is enforced at the API layer, not merely documented. |
| Scoped API keys with named actors | `server/auth/middleware.js`; `server/auth/api-keys.js` | Every consuming application authenticates with the minimum required capability. The `X-Family-Graph-Actor` header forces consuming apps to identify themselves in every audit row. |
| Sticky identity decisions with reason recording | `server/identity/conflicts.js`, `resolution_notes` field | The system preserves operator judgment over time, reducing conflict queue depth and building a documented decision history. |
| Supply chain protection | `scripts/preinstall-sfw-check.js`; `CLAUDE.md` | Every dependency install routes through Socket Firewall's risk database before touching disk. This is an enforced control, not a recommendation. |
| Ecclesiastical titles in sanitizer detection | `server/sanitize/ner.js`, `COMMON_TITLES` array | `Fr`, `Sr`, `Rev`, `Father`, `Sister`, `Brother` are in the title recognition list. General-purpose sanitizers do not carry this coverage. |
| Connector credential never returned by API | `server/api/settings.js` | The settings endpoint reduces credential ciphertext to `_set: true` flags. The base64 ciphertext is never returned to callers, preventing length inference and existence attacks. |
| SSRF protection on Google Sheets fetch | `server/sources/sheets-url.js` | The URL parser enforces `docs.google.com` host exactly, constructs the export URL itself rather than fetching user-supplied URLs, validates each redirect hop against an allowlist, and enforces a 10MB body cap and 30-second timeout. |

---

## Additional Pressure-Test Modules to Add During Incubation

The previous supplemental analysis identified several review modules that should remain visible. They are not all required before Gate 1, but they should guide the incubation work.

---

### Pressure-Test Module PT-01 — Central Substitution Risks

| Attractive claim | What it does not prove | Required evidence |
|---|---|---|
| Local-first | Proper authorization, family rights, competent administration | Deployment profile, operator authority, backup/key/incident plan |
| Encrypted | Safe access, safe export, appropriate collection | Threat model, key lifecycle, access control, export logs |
| Human-reviewed | Independent judgment | Human influence telemetry |
| Auditable | Reconstructable institutional decision | Audit coverage matrix |
| Reversible | Family-accessible repair | Appeal and downstream correction process |
| Pseudonymized | Anonymous or AI-approved | Sanitizer benchmark and destination policy |
| Open source | Secure or maintained | Independent review, release integrity, maintainer plan |
| Catholic | Morally legitimate | Catholic governance controls and authority boundaries |
| Source of truth | Legitimate authority | Field-level authority matrix |
| Pilot-tested | Generalizable safety | Independent validation and scope limits |

---

### Pressure-Test Module PT-02 — AI-Safety Failure Taxonomy Applied to FamilyGraph

| Failure mode | FamilyGraph-specific question | Evidence needed |
|---|---|---|
| Objective failure | Does record unification subordinate family protection? | Approved purpose and prohibited-use statement |
| Specification failure | Are identity, household, guardianship, access, and consent separated? | Ontology and authority matrix |
| Generalization failure | Does matching work outside the pilot institution? | Multi-population validation |
| Correction failure | Can errors be found, reversed, propagated, and used to reform the system? | Appeal and repair tests |
| Interpretability failure | Can reviewers see why a match was recommended? | Match explanation and evidence packet |
| Evaluation failure | Do tests cover real family failure modes? | Adversarial test corpus |
| Authority drift | Do downstream apps treat FamilyGraph as more authoritative than approved? | Integration policy and app constraints |
| Accountability failure | Can CDCF reconstruct who decided what and why? | Decision record and telemetry |
| Human influence erosion | Does the system shape reviewers into confirmers? | Reliance monitoring |

---

### Pressure-Test Module PT-03 — Goodhart Metrics

| Dangerous metric | Failure mode | Safer countermetric |
|---|---|---|
| Duplicate reduction | Aggressive merging | High-risk false-merge rate |
| Auto-match rate | Fewer human reviews | Mandatory-review compliance |
| Conflict queue clearance | Speed over judgment | Review quality and reversal rate |
| Import success | Bad semantic mapping | Mapping error rate |
| Record completeness | Overcollection | Data minimization exceptions |
| Connector coverage | Attack surface expansion | Connector risk score |
| Review throughput | Confirmation behavior | Evidence-view rate and reason quality |
| Low reversal rate | Families cannot discover errors | Family complaint and correction outcomes |
| High confidence scores | Uncalibrated certainty | Calibration curves |
| Number of deployments | Scaling before evidence | Deployment readiness score |

---

### Pressure-Test Module PT-04 — Red-Team Propositions

These are hypotheses to test, not accusations.

| ID | Proposition | Reviewer lane |
|---|---|---|
| RT-01 | The primary value of cross-system linkage is also the principal privacy hazard. | Privacy / security |
| RT-02 | Local operation may hide weak institutional practice rather than only reduce vendor risk. | Governance / operations |
| RT-03 | The system may centralize practical identity authority while claiming subsidiarity. | Catholic governance |
| RT-04 | Pseudonymization may increase confidence in external AI use more than it reduces re-identification risk. | AI safety / privacy |
| RT-05 | Human conflict review may become an automation-bias channel. | AI governance / human factors |
| RT-06 | Reversible merging may encourage riskier initial merges. | Product / governance |
| RT-07 | Audit logging may protect the institution more than the family unless appeal rights exist. | Legal / safeguarding |
| RT-08 | One canonical identity error may propagate across every consuming application. | Systems architecture |
| RT-09 | Open-source installations may become unsupported after maintainer turnover. | Open-source governance |
| RT-10 | Catholic mission trust may lower scrutiny among Catholic adopters. | TAC / Board |

---

### Pressure-Test Module PT-05 — Pilot Decision Thresholds

The pilot should use predetermined thresholds rather than vague monitoring.

| Evidence | Required action |
|---|---|
| Protected-address disclosure to unauthorized person | Immediate suspension and incident response |
| Child attached to unauthorized household | Suspend matching / merge functions |
| Consequential action lacks named actor | No live deployment |
| Sanitizer misses direct identifier in approved test | External AI export disabled |
| False-merge rate exceeds approved threshold | Restrict or suspend matching |
| Subgroup performance disparity exceeds threshold | Revalidate and restrict deployment |
| Downstream correction fails | Disable propagation |
| Backup restore fails | No production data |
| Near-total recommendation acceptance with minimal reasons | Automation-bias review |
| Maintainer support lapses | Freeze new deployments |
| Security remediation SLA missed | Disable affected function or require upgrade |
| Field authority conflict lacks resolver | Do not ingest or reconcile that field |

---

## Reviewer Self-Governance Record

The evaluating member should complete this section before recommending a formal TAC disposition.

### Reviewer declarations

- [ ] I have disclosed personal, institutional, financial, authorship, and collaborative relationships relevant to this project.
- [ ] I have identified which claims I personally reproduced and which rely on another reviewer or AI-assisted analysis.
- [ ] I have separated observations from inferences, risks, and recommendations.
- [ ] I have searched for evidence that weakens my preferred conclusion.
- [ ] I have recorded corrections to earlier drafts rather than silently removing them.
- [ ] I have not treated Catholic identity, open-source status, local deployment, encryption, or developer reputation as proof of safety.
- [ ] I have not treated missing evidence as proof that harm has occurred.
- [ ] I have defined what evidence would update my disposition toward approval.
- [ ] I have defined what evidence would require restriction or suspension.
- [ ] I have preserved dissent and invited factual correction from the project owner.
- [ ] I have avoided making a legal, canonical, security-certification, or Board-authority claim beyond my role.
- [ ] I have considered the family least able to detect, explain, or contest an error.

### Current reviewer confidence

| Proposition | Confidence | Basis | Evidence that would change it |
|---|---:|---|---|
| The project addresses a real cross-system identity problem | High | Repository scope and institutional context | Evidence that intended systems already provide equivalent governed interoperability |
| The architecture contains meaningful privacy and provenance controls | High | Code and documentation observations | Independent review showing controls fail materially in deployment |
| Current evidence establishes safe broad deployment | Low | Missing independent validation and governance artifacts | Completed assurance package and successful independent pilot |
| A bounded incubation path could improve the project | Moderate to high | Gaps are identifiable and partly remediable | Maintainer declines stewardship or project scope expands without controls |
| Children and complex families face material linkage-related risk | High plausibility; occurrence unproven | Data model, deployment context, foreseeable misuse | Empirical evidence demonstrating controls reduce risk below approved thresholds |

### Correction log

| Version | Prior statement | Correction | Reason |
|---|---|---|---|
| 1.0 → 1.1 | “Conditional-go” could be read as approval | Reframed as possible conditional incubation; endorsement and broad deployment deferred | Incubation is not certification |
| 1.0 → 1.1 | Three documentation conditions were described as sufficient | Expanded to an assurance and governance response package | Several findings require architectural, operational, and independent evidence |
| 1.0 → 1.1 | FamilyGraph described through an AI-components frame | Reclassified as identity-governance infrastructure with automated and AI-adjacent functions | Governance should follow function and consequence |
| 1.0 → 1.1 | General audit atomicity risk was previously overgeneralized in an earlier draft | Limited transactional guarantee to `entity_changes`; retained separate `audit_events` finding | Repository evidence supports the narrower claim |
| 1.1 → 1.2 | Automated and technical sections were essay-like and difficult to route among TAC reviewers | Converted to issue-card, architecture-card, response-dashboard, and reviewer-assignment format | Chris and TAC reviewers need fast comprehension, concrete evidence, and immediate action paths |
| 1.2 → 1.3 | Methodology, human control, and Gate analysis still blurred philosophical method, incubation readiness, and graduation readiness | Converted to method cards, human-control cards, Gate 1 incubation cards, Gate 2 graduation cards, and pressure-test modules | The memo must show what is needed now, what is needed before live use, and what is needed before CDCF endorsement |

---

## Decision and Comment Record

### Project owner response

> Add response here or link to a repository issue / pull request.

### TAC reviewer comments

| Reviewer | Role | Finding IDs | Position | Comment / evidence |
|---|---|---|---|---|
| — | — | — | — | — |

### Independent reviewer comments

| Reviewer | Discipline | Scope | Independence disclosure | Report |
|---|---|---|---|---|
| — | — | — | — | — |

### Provisional TAC recommendation

| Field | Entry |
|---|---|
| Recommendation | — |
| Conditions | — |
| Dissent | — |
| Recusals | — |
| Vote or consensus method | — |
| Date | — |
| Repository commit reviewed | — |

### Board disposition

| Field | Entry |
|---|---|
| Decision | — |
| Authority | — |
| Conditions | — |
| Effective date | — |
| Public communication approved | — |

---

## Note on ParishBrain

ParishBrain (`parishbrain.com`) is a consuming application built on top of FamilyGraph. It is not submitted here and has not been evaluated. When ParishBrain is ready for CDCF submission, it will require a separate Gate 1 intake with particular attention to C5 subgroup performance for any AI outputs, C6 escalation conditions for AI-mediated decisions, and the LLM integration architecture that FamilyGraph's sanitizer is designed to support. That evaluation should follow FamilyGraph's Gate 1 and Gate 2 reviews.

---

*Prepared by Mark Julius Banasihan, TAC AI Governance Specialist. June 2026.*

*Working pre-finding memo. This document invites factual correction, maintainer response, TAC review, independent evidence, and Board disposition. It is not a certification, legal opinion, canonical judgment, or CDCF endorsement.*
