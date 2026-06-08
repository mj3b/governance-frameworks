# TAC Working Memo: FamilyGraph
## CDCF Gate 1 Incubation Evaluation and Assurance Review — Version 1.2

---

| Field | Detail |
|---|---|
| **Document type** | TAC Working Memo — Governed Pre-Finding Analysis and Request for Response |
| **Version** | 1.2 |
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

## Methodology Note

### Purpose of the method

The CDCF criteria determine **what must be evaluated**. The method below governs **how this reviewer moves from repository evidence to a provisional judgment**.

This distinction matters. A criteria checklist can still produce symbolic compliance when terms such as “human oversight,” “validation,” “auditability,” “safe,” or “local-first” remain undefined. The method therefore requires every material claim to resolve into observable mechanisms, identifiable actors, evidence, authority, and decision consequences.

### Source hierarchy

The review uses sources according to function:

1. **Primary repository evidence:** source code, migrations, tests, specifications, security documentation, integration contracts, session notes, release history, and deployment instructions.
2. **CDCF authority:** published governance criteria, lifecycle, bylaws, manifesto, standards, and Board-adopted policies.
3. **Catholic moral and ecclesial sources:** used to assess human dignity, prudence, subsidiarity, solidarity, common good, and institutional responsibility.
4. **Legal and regulatory sources:** used to identify questions requiring counsel; this memo does not substitute for legal advice.
5. **Technical standards and independent research:** used to test security, privacy, identity-resolution, AI-risk, and assurance claims.
6. **Diagnostic reasoning sources:** rationality, cognitive-failure, and AI-safety concepts help locate failure mechanisms. They do not independently prove that a repository is safe, unsafe, lawful, or unlawful.

### Analytical sequence

The assessment applies seven lenses in sequence.

#### 1. Concept discipline

Each governance claim is translated into an operational test.

Example:

> “Human oversight” means a named and authenticated person can inspect the relevant evidence, understands the decision context, has time and competence to judge, can reject or escalate the system output, records an independent reason, and remains accountable for correction.

A label that cannot be translated into an actor, mechanism, condition, evidence standard, or consequence is treated as incomplete.

#### 2. Map–territory comparison

Documentation, dashboards, tests, and policies are the project’s map. Runtime behavior, operator conduct, family experience, errors, appeals, disclosures, and recovery outcomes are the territory.

The review compares the two and records any discrepancy. Strong documentation raises confidence only when operational evidence supports it.

#### 3. Bayesian evidence updating

For every material belief, the review records:

- the starting assumption;
- the supporting evidence;
- contrary evidence;
- the present confidence;
- the evidence that would change the judgment;
- the action threshold associated with that change.

This prevents a favorable or unfavorable first impression from becoming a protected conclusion.

#### 4. Cognitive failure-mode review

The assessment tests for predictable institutional reasoning failures, including:

- motivated stopping;
- motivated continuation;
- authority bias;
- founder halo;
- belief as institutional attire;
- cached assumptions;
- scope drift;
- documentation substitution;
- metric defense;
- treating absence of reported incidents as evidence of safety.

These are review hazards, not allegations of bad faith.

#### 5. Human influence telemetry

For every consequential automated or algorithmically assisted action, the review asks whether the decision record shows:

- evidence access;
- output interpretation;
- independent judgment;
- override authority;
- reason recording;
- appeal ownership;
- remediation ownership;
- system-change authority.

A human appearing in the workflow does not by itself establish meaningful human control.

#### 6. Catholic governance integration

The technical design is tested against:

- **human dignity:** the person remains a subject of rights and institutional concern, not merely an entity to be reconciled;
- **prudence:** counsel, judgment, and command remain practically exercisable;
- **subsidiarity:** authority remains at the proper level, with higher coordination where competence, safeguarding, law, or ecclesial authority requires it;
- **solidarity:** review begins from the family least able to detect or contest error;
- **common good:** administrative efficiency remains subordinate to trustworthy institutions and family protection;
- **institutional repentance:** after harm, the institution can acknowledge, reconstruct, repair, and reform.

#### 7. Adversarial assurance review

The reviewer asks how the system could fail even when every participant acts in ordinary good faith. High-severity claims are tested against misuse, configuration drift, staff turnover, weak institutional capacity, vulnerable-family cases, connector failure, compromised credentials, and downstream propagation.

### Epistemic labels

Every material statement should be classified as one of the following:

- **Observation:** directly reproducible from an identified repository artifact or authoritative source.
- **Inference:** a conclusion derived from stated observations through an inspectable reasoning chain.
- **Risk:** a forward-looking possibility with stated likelihood, severity, and affected parties.
- **Unknown:** a question for which the reviewed evidence is insufficient.
- **Correction:** a prior claim that has been narrowed, revised, or withdrawn.
- **Recommendation:** a proposed control or governance action, not an observed defect.
- **Decision:** an authorized institutional disposition. This memo contains no final CDCF decision.

### Burden of proof

The burden changes with the claim.

- The reviewer bears the burden of accurately describing the repository.
- The project bears the burden of substantiating claims of safety, validation, privacy protection, broad readiness, or compliance.
- CDCF bears the burden of applying its criteria consistently, disclosing conflicts, and recording the authority behind any decision.
- A deploying institution bears responsibility for its configuration, operators, source authority, data practices, and legal obligations.
- Families should not bear the burden of discovering hidden system errors after deployment.

### Review limitations

This review is bounded by the repository archive and evidence available at the review date. It does not constitute:

- a penetration test;
- a legal opinion;
- a canonical judgment;
- an accessibility audit;
- empirical validation of the matcher;
- empirical validation of pseudonymization;
- certification of any deployment;
- confirmation that undocumented operational practices do or do not exist.

A missing artifact is recorded as missing evidence, not proof that the underlying practice never occurs.

### AI assistance disclosure

AI tools assisted with code navigation, issue discovery, source comparison, and drafting. Their outputs were treated as hypotheses requiring human review. No model output should become a formal finding merely because it is detailed or persuasive. Before adoption, code-level claims should be reproduced, citations checked, uncertainty retained, and contradictory evidence considered.

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

## Human Control Architecture

The governing question for identity infrastructure is: where does human judgment remain capable of changing an identity decision for the people that decision affects?

FamilyGraph's conflict resolution workflow is designed to preserve operator judgment. The conflict queue surfaces both records, the confidence score, the reasons the matching engine flagged the conflict, and a free-form notes field for the operator to record their reasoning [`server/api/conflicts.js`]. Sticky decisions carry that reasoning forward permanently: a future import will not re-flag a pair the operator has already resolved. Override authority requires no friction. The assignment workflow routes conflicts to named operators with a configurable time-to-live, after which the assignment expires and the conflict returns to the open queue.

**Where human control is architecturally genuine:**

Evidence access for identity decisions is strong. The conflict queue surfaces both records and the evidence behind the flag. Operators see confidence score and reasons before deciding.

Override authority is not ceremonial. Operators can reject, dismiss, or force-merge any conflict without additional documentation burden. Thresholds are configurable per institution via the profiles table.

Reason recording exists and is surfaced in the UI. The `resolution_notes` field is present and visible. It is not required. Requiring reason recording for contested identity decisions would strengthen the governance record, particularly for cases involving custody flags or EIM-certified individuals.

**Where human control reaches a boundary:**

The affected-family layer has no documented accountability path. FamilyGraph's oversight architecture is designed for institutional operator review. The families whose records are being managed have no documented channel to report and contest an identity error. The institutional operator is the accountable human, which is correct for infrastructure of this type. But that operator needs documented guidance on receiving, investigating, and correcting a parishioner's report, and that guidance does not currently exist.

The automated EIM sweep operates without human review or notification. When a certification lapses, the status changes silently. No operator notification accompanies the change. No audit record is written. A pastor or school administrator who checks the ministry roster the day after a certification expires sees `expired` with no context about when the change occurred.

---

## Gate 1 Criterion Analysis

---

### C1 — Mission Alignment and Canonical Scope

| | |
|---|---|
| **Status** | ✅ Pass |
| **Finding type** | Observation |
| **Canonical grounding** | CDCF Bylaws Article I §2.1; *Antiqua et Nova* §42 |

FamilyGraph solves a structurally identical problem across every Catholic institution that runs more than one management system. The business spec documents this explicitly: the value proposition is not specific to St. Theresa's. Any developer can read the integration guide and build a consuming application without consulting the author. The integration contract (`FAMILYGRAPH_INTEGRATION.md`) is designed as a generic, app-agnostic document.

FamilyGraph does not simulate sacramental functions. The business spec explicitly excludes sacramental records from scope. EIM certification tracking is present because diocesan safe-environment compliance requires it; FamilyGraph makes no canonical determinations about certification validity.

The universality test passes. FamilyGraph's value proposition holds across the Catholic institutional ecosystem.

---

### C2 — Human Accountability Architecture

| | |
|---|---|
| **Status** | ⚠️ Partial Gap |
| **Finding type** | Observation (conflict workflow strength); Observation (accountability gap) |
| **Canonical grounding** | *Antiqua et Nova* (genuine human control); Canon 627 (authority tied to specific individuals) |

The conflict resolution workflow preserves human judgment by design. Ambiguous identity matches are queued for operator review with full evidence, confidence scores, and reasons. Sticky decisions carry operator reasoning forward against future imports. Override authority requires no friction.

The accountability gap is at the affected-family layer. The current contact path for any identity issue routes to a single individual's personal email (`christreadaway@gmail.com`, per `SECURITY.md`). For a CDCF-endorsed production deployment across multiple Catholic institutions, that is insufficient as an institutional accountability structure. The people whose family records contain errors have no documented path to report and receive correction.

**Required for Gate 2:** A governance note specifying who an affected family contacts when their identity record contains an error, the institutional operator's obligation to investigate and correct, and how the correction is logged in the audit trail.

---

### C3 — Transparency of Scope and Operation

| | |
|---|---|
| **Status** | ✅ Pass with two corrections required |
| **Finding type** | Observation (documentation quality); Observation (threshold discrepancy) |
| **Canonical grounding** | *Antiqua et Nova* (evaluation requires information) |

The business spec, product spec, security model, integration contract, and schema documentation are detailed and internally consistent. The sanitizer limitation disclosure in the README is present and accurate. The session notes are an unusually complete decision log that any reviewer can read to understand why architectural choices were made.

Two documentation corrections are required.

The product spec environment variable table shows `FAMILY_GRAPH_AUTO_MERGE = 0.92`. The system runs at 0.85, confirmed in `tests/_helpers.js` and the session notes (v9 follow-up section). The product spec is stale documentation that does not reflect current behavior.

The WhatsApp submission described FamilyGraph as infrastructure "which can sit on a local LLM to keep data off frontier models." That characterizes a consuming application's architectural decision, not FamilyGraph itself. Any CDCF project description should draw this boundary precisely: FamilyGraph produces pseudonymized output and makes data LLM-safe. It does not implement LLM integration. That integration belongs to the consuming application and requires its own evaluation.

---

### C4 — Independent Validation of Claimed Capabilities

| | |
|---|---|
| **Status** | ❌ Gap |
| **Finding type** | Observation + Inference |
| **Canonical grounding** | Proportionate validation standard; validation stakes scale with data sensitivity |

Three validation gaps require attention. They differ in what the validation covers.

**Gap 1: Implementation and test suite were generated by the same system.**

The session notes confirm that Claude Code wrote both the FamilyGraph implementation and the test suite. The 489 passing tests confirm internal consistency. They do not confirm fitness for the specific populations, naming conventions, or institutional contexts Catholic parishes and schools represent. Tests written by the same AI system that wrote the code reflect that system's assumptions about what it built. The standard developer-test limitation applies with additional specificity here: the test harness reflects one system's model of correct behavior, not an independent party's verification of real-world performance.

This is not a claim that the code is incorrect. The session notes document rigorous bug-finding during development: 5 failures in the first test pass, corrected; threshold misconfiguration discovered and fixed; FACTS mapping bug caught by end-to-end tests. The development process was genuinely iterative. The validation gap is that no party independent of the development process has evaluated the system's behavior.

**Gap 2: Identity matching against Catholic parish and school naming conventions.**

The matching engine's nickname and compound-name coverage is documented for English-language equivalents. It has not been evaluated against the naming conventions of the specific populations Catholic institutions serve at scale. A false auto-merge in these cases creates a family record error that propagates to every consuming application. A false new-person creation defeats the purpose of FamilyGraph without any error signal.

**Gap 3: PII sanitizer failure rate against parish and school population data.**

The `compromise` NLP library's `#Person` detection accuracy for non-English names is unvalidated in the Catholic institutional context. The README's limitation disclosure is accurate and present. It does not replace an evaluation of whether that limitation materializes at consequential rates for the specific communities Catholic institutions serve.

**Required for Gate 1 (plan) and Gate 2 (completion):** A concrete validation plan naming the evaluation method (community-specific benchmarking, third-party technical assessment, or structured red-team assessment against a representative name corpus), the populations to be covered, and a timeline for completion before Gate 2. A written plan satisfies C4 at Gate 1. Completed results are required at Gate 2.

---

### C5 — Impact on Vulnerable Populations

| | |
|---|---|
| **Status** | ⚠️ Partial |
| **Finding type** | Inference |
| **Canonical grounding** | Preferential option for the poor; Pope Leo XIV on technology; *Antiqua et Nova* on algorithmic bias |

Catholic institutions disproportionately serve populations that commercial identity resolution pipelines have historically underperformed on: recent immigrants and non-English-speaking families, families in poverty, elderly parishioners, and children. FamilyGraph's deployment context places these populations inside the system by design.

The business spec reflects awareness of this. The system accepts any list format specifically because many parishes "keep records in spreadsheets or on paper." This is institutional awareness of the operator's resource constraints. It is not a formal subgroup analysis.

The AI domain extension under C5 requires either documented subgroup performance analysis or an explicit acknowledgment paired with a concrete plan. The README limitation statement is the acknowledgment. The plan does not yet exist.

The C4 validation exercise covers both gaps: the same evaluation that tests matching algorithm accuracy against non-English naming conventions constitutes the C5 subgroup analysis.

**Required for Gate 2:** Documented subgroup performance results from the C4 validation exercise, with attention to the naming convention populations described under C4.

---

### C6 — Deployment Governance Specification

| | |
|---|---|
| **Status** | ❌ Gap |
| **Finding type** | Observation |
| **Canonical grounding** | Canon 1609 (structured deliberation, capacity to revise judgments, transparent appeal); *Antiqua et Nova* on subsidiarity |

FamilyGraph's technical deployment architecture is subsidiarity-compatible by design. Local-first, loopback default, no cloud dependency, no phone-home, scoped API keys, operator-controlled configuration. An institution can deploy, maintain, and shut down FamilyGraph without any dependency on a central authority. This is architecturally correct under *Antiqua et Nova* §42's requirement that technology management respect subsidiarity at every level.

Two governance elements are absent.

**Absent element 1: Escalation condition for systematic matching failures.**

If a parish import produces a large number of unexpected auto-merges, such as all families sharing a common surname incorrectly merged, the current documentation gives the operator no defined threshold for pausing the sync, no escalation path, and no upstream notification mechanism. The operator must discover the error through the conflict queue or through family complaints, whichever comes first.

**Absent element 2: Affected-person process for institutional operators.**

Operators need documented guidance on receiving, logging, investigating, and correcting a parishioner's report of an identity record error. The audit trail and entity_changes log architecture supports reconstruction of what changed and when. The process documentation for using that capability in response to a family complaint does not exist.

**Required for Gate 1:**

(a) A brief governance note specifying the trigger under which an operator should pause a connector sync and manually review auto-merges before consuming applications propagate results.

(b) A brief process note describing how an institutional operator responds to a parishioner's report of an identity record error, including how the investigation and correction are logged.

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
