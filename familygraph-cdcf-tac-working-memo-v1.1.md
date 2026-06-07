# TAC Working Memo: FamilyGraph
## CDCF Gate 1 Incubation Evaluation and Assurance Review — Version 1.1

---

| Field | Detail |
|---|---|
| **Document type** | TAC Working Memo — Governed Pre-Finding Analysis and Request for Response |
| **Version** | 1.1 |
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

## Automated and AI-Adjacent Components

FamilyGraph is principally an identity-governance and institutional data system, not a general-purpose AI system. It contains deterministic matching, scoring, import mapping, pseudonymization, and optional external-AI workflow support. AI-governance scrutiny applies where these functions shape consequential judgments about persons or create confidence that data is safe to send to an external model. They differ in architecture, risk level, and governance maturity.

### Classification rule

Controls are applied according to function and consequence rather than branding:

- deterministic software still requires governance when it creates or propagates consequential identity assertions;
- a confidence score is not an empirically calibrated probability unless validation demonstrates that relationship;
- pseudonymization is a privacy control, not proof of anonymity or permission to disclose;
- human review is meaningful only when the human can inspect evidence, exercise authority, record reasons, and correct downstream effects.

### Component 1: Identity Matching Algorithm

The matching engine scores incoming records against the existing ledger and routes each to one of three outcomes: auto-merge, conflict queue, or new person. It is a rules-based probabilistic scoring system, not a trained ML model. The scoring logic is fully documented in `server/identity/matching.js` and auditable by any reviewer.

**The scoring architecture** [`server/identity/matching.js`, `scoreMatch()`]:

| Signal Type | Trigger Condition | Confidence Assigned |
|---|---|---|
| Definitive (auto-merge) | Exact email; exact phone; exact name + exact DOB; address line ≥ 0.85 similarity with name overlap | 0.95 |
| Definitive veto | Different state; address similarity < 0.5; conflicting zip + address < 0.7 | Drops below auto-merge threshold |
| Soft additive | Last name (suffix-aware); first name (nickname/compound/phonetic-aware); DOB; address; zip; city | Capped at 1.0 |

**Observation: The threshold documentation is inconsistent across the codebase.** `server/identity/matching.js` states default thresholds of `autoMerge: 0.85, review: 0.30`. The product spec environment variable table shows `FAMILY_GRAPH_AUTO_MERGE = 0.92`. The test helper file (`tests/_helpers.js`) confirms the operational defaults as `{ autoMerge: 0.85, review: 0.30 }`. The session notes (`session_notes.md`, v9 follow-up section) explain the root cause: `config.js` retained old threshold values (0.92/0.7) after the v9 matching rewrite recalibrated to (0.85/0.30), and the product spec was not updated. The system runs at 0.85/0.30. The product spec's environment variable table is stale documentation. An operator configuring their institution against the product spec would set thresholds that do not match actual behavior. This requires correction in the documentation before any institution-wide deployment guidance is issued.

**Observation: The implementation and test suite were generated by the same system.** The session notes document that Claude Code wrote both the matching algorithm and the test cases that verify it. This means the tests reflect Claude Code's assumptions about what it built rather than an independent party's verification of actual behavior. The test suite confirms internal consistency. It does not confirm fitness for the specific populations FamilyGraph will serve. This is a material consideration in the C4 independent validation assessment: developer-authored tests and AI-generated tests both carry the same limitation relative to independent validation. Neither substitutes for external evaluation.

**Observation: The name normalization function handles diacritics correctly.** [`server/crypto/encryption.js`, `normalizeName()`]: Uses `String.prototype.normalize('NFKD')` followed by `replace(/\p{M}+/gu, '')` to strip combining diacritics. García normalizes to garcia correctly. This is a real-world requirement for Spanish-surname parishes.

**Inference: The nickname and compound-name library does not address naming conventions for the largest Catholic immigrant communities.** [`server/identity/matching.js`, `NICKNAME_GROUPS` array and `firstNameMatchesCompound()`]: The documented equivalences cover English-language nicknames (Tim/Timothy, Bob/Robert, Mary/Marie) and compound names using the English conjunction "and." The session notes reference "Tim == Timothy, Bob == Robert, Mary == Marie" and "Timothy & Mary" compound matching as the examples. Vietnamese naming order conventions, Korean family-name-first conventions, Filipino compound surnames (dela Cruz, Santos), and Polish patronymic patterns common in historically Catholic immigrant communities are not addressed. For parishes serving these communities, this creates a risk of false new-person creation rather than correct auto-merge, producing identity fragmentation of the type FamilyGraph is designed to solve. The reasoning: name matching that fails on community-specific patterns reverts to lower-confidence soft-signal scoring, which may fall below the review threshold and silently create duplicate records.

**Risk: Operator threshold misconfiguration.** The threshold is configurable per institution via the profiles table [`server/identity/matching.js`, `thresholds.autoMerge`]. No documentation guides operators on what threshold values are appropriate for their community's naming composition. A parish with many families sharing a common surname faces different auto-merge accuracy at 0.85 than a parish with high name diversity. No guidance exists on this calibration decision. [NIST AI RMF: GOVERN 6.1, MAP 1.5]

---

### Component 2: PII Sanitizer

The sanitizer converts documents into pseudonymized versions for AI workflow use. An operator drops a file into the watch folder; the sanitizer replaces PII with stable identifiers; the operator uses the sanitized output with an LLM.

**Observation: The sanitizer runs four detection layers in sequence** [`server/sanitize/ner.js`, detection pipeline]:

| Layer | Method | Coverage | Documented Gap |
|---|---|---|---|
| 1. Structured PII | Regex patterns for email, phone, SSN-shaped, DOB, US street address | High for standard US formats | International phone formats; non-US address patterns |
| 2. Registry lookup | HMAC-SHA256 match against every active person's name in the ledger | High for known names | Zero coverage for names not yet in the ledger |
| 3. NER entity detection | `compromise` JS library, `#Person` and `#Place` entity tags | Moderate; general English corpus | Non-English names; community-specific patterns |
| 4. Capitalized-token heuristic | Two-to-three capitalized tokens not in stopword list | High recall, low precision | High false-positive rate for organization names and headings |

**Observation: The ecclesiastical title list includes Catholic-specific titles.** [`server/sanitize/ner.js`, `COMMON_TITLES` array]: `Fr`, `Sr`, `Rev`, `Father`, `Sister`, `Brother` appear in the title recognition list. This is domain-specific design awareness. A document referencing "Father Michael" will have "Father" flagged as a title prefix, protecting the name tokens around it.

**Observation: The `compromise` library uses general English corpus training.** [`server/sanitize/ner.js`, NER layer, `nlp = require('compromise')`]: The library's `#Person` entity detection reflects the distribution of English-language names in its training data. The session notes (`session_notes.md`, open-source prep section) record that the anonymization language was explicitly softened to best-effort because "no automated system detects every possible identifier." This confirms developer awareness of the limitation.

**Inference: Sanitizer miss rates for community-specific names are unvalidated and likely higher than for English-language names.** The reasoning runs from the `compromise` library's training distribution through NLP literature on entity recognition performance across language communities to the conclusion that parishes in metropolitan areas with large immigrant populations face higher residual PII risk when using the sanitizer. An operator at a parish serving primarily Vietnamese, Korean, or Filipino families who trusts the sanitizer for LLM workflow output has no independent basis for that trust.

**Risk: Gradual trust erosion through invisible failure.** The sanitizer's failure mode is silent: an unsanitized name passes through the pipeline and reaches the LLM without any signal to the operator. The operator review requirement in the README is a disclosure, not a control. A community-specific review protocol, specifying how an operator should sample-test sanitized output against their own community's naming patterns before trusting the pipeline, does not exist. [NIST AI RMF: MEASURE 2.5, MEASURE 2.11]

---

### Component 3: Column Auto-Mapper

The auto-mapper scores column headers from imported files against approximately 250 alias variants to identify field mappings [`server/sources/csv.js`, `autoMapFlat()`]. It is fully rule-based and deterministic. The import preview holds the Import button disabled when no identity columns are detected and exposes the proposed mapping for operator correction. Human judgment is required before any data is written. This is a well-governed human-in-the-loop design. Governance risk here is low.

---

## Technical Architecture Assessment

### Cryptographic Implementation

**Observation: The encryption implementation is correctly designed** [`server/crypto/encryption.js`]: AES-256-GCM with 12-byte random IV generated per call via `crypto.randomBytes(IV_LEN)`. No IV reuse. 16-byte GCM authentication tag. Tamper detection through GCM tag verification. Three separate 256-bit keys: `master` (Bearer token), `dataKey` (PII encryption), `hmacKey` (searchable HMAC). All keys generated via `crypto.randomBytes(32)`. Key material stored at `~/.family-graph/secret.key` with mode 0600. The cryptographic architecture matches its documentation.

**Risk: The dataKey cannot be rotated in v1.** [`server/crypto/secret.js`, `rotate()` function]: The `rotate()` function regenerates only the master Bearer token. The `dataKey` and `hmacKey` are unchanged on rotation. The comment states explicitly: "data-encryption key cannot be rotated without re-encrypting the database, which is a v2 concern." If the secret.key file is compromised, all historical PII in the database is permanently accessible. For a system designed to be a permanent family registry holding PII for children and families across decades, the absence of key rotation in v1 is a documented architectural constraint that deploying institutions should understand before committing to the platform. [NIST AI RMF: MANAGE 2.2, GOVERN 3.1]

---

### Audit Architecture

**Observation: Two distinct audit mechanisms exist with different transactional guarantees.** This distinction was identified through implementation review and was not clear from documentation alone.

`audit_events` [`server/audit/index.js`, `record()`]: The general audit trail. This is a standalone synchronous INSERT executed by `db.prepare().run()`. It does not share a transaction with the data operation that triggered it. A write that succeeds followed by an audit INSERT failure leaves data without a corresponding audit record. The session notes describe robustness improvements to the audit recorder (circular structure handling, metadata size capping) but do not describe transactional coupling to data writes.

`entity_changes` [`server/integration/`]: The history log introduced in v13 for archive, reinstate, merge, and split operations. The session notes document explicit atomicity hardening: "Every write path that touches data AND writes a history row now runs inside a single `db.transaction(() => ...)`. Without this, a history.record() failure...would leave the data row written without an audit row." This guarantee applies to entity_changes, not audit_events.

The prior draft of this memo stated the transactional guarantee as applying to the audit trail generally. That was an overstatement. The correct claim is narrower: entity_changes operations are transactionally atomic with data writes. General audit_events are not.

**Observation: Audit retention is configurable, with one protected category.** [`server/audit/index.js`, `sweep()`]: Tier-1 (internal) events are swept based on the configurable `audit_retention_days` setting. Tier-2 (export-consent) events are never swept: "they are the operator's record of what PII has left the machine." This design decision protects the most consequential audit record.

---

### Safe API Surface

**Observation: The safe API surface enforces loopback origin, not credential.** [`server/api/safe.js`; `server/auth/middleware.js`, `loopbackOnly()`]: Every safe endpoint passes `includePii: false` to all data access calls, which is correct. The `loopbackOnly()` middleware enforces origin: `127.0.0.1`, `::1`, and `::ffff:127.0.0.1` are accepted; any other origin receives 403. However, there is no Bearer token requirement on this surface. Any application running on the same machine can call the safe API without credentials. The session notes describe this as intentional: "safe API surface enforces loopback origin." This design is appropriate for single-operator desktop deployment. Institutions deploying FamilyGraph on a shared server or in a multi-user environment should evaluate whether loopback-only origin control is sufficient for their access model.

---

### EIM Certification Sweep

**Observation: The EIM expiry sweep writes no audit record.** [`server/identity/eim.js`, `recomputeStatus()`]: The function executes a direct UPDATE on the persons table flipping `eim_status` from `certified` to `expired` for rows whose `eim_expires_on` has passed. There is no call to `audit.record()` in this function. EIM status changes triggered by the automated sweep are not logged in the audit trail. An operator reviewing audit_events cannot determine when a certification status changed or why.

The governance consequence is direct: if an operator or a diocese asks when a volunteer's EIM status changed from certified to expired, the audit trail cannot answer. For a feature whose stated purpose is to govern who can work with minors, the absence of an audit record on automated status changes is a gap. [NIST AI RMF: GOVERN 1.1, MANAGE 4.1]

---

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

## Required Response Package

The project owner should respond to the following conditions in the repository. Some conditions require a plan for incubation; others require implemented and independently verified controls before a live-family-data pilot or Gate 2.

### Condition 1 — Correct and Bound the Project Claims

**Required for incubation documentation**

- Correct the auto-merge threshold discrepancy.
- Distinguish identity equivalence, household association, guardianship, access authority, directory visibility, and consent.
- Replace unqualified “source of truth” language with a bounded statement of institutional authority.
- State clearly that FamilyGraph does not itself provide an LLM and that pseudonymized output remains personal data subject to governance.
- Identify prohibited inferences and prohibited uses.

### Condition 2 — Independent Validation Plan

**Plan required for incubation; completed evidence required before broad deployment**

Provide a versioned plan covering:

- identity-matching precision and recall;
- severity-weighted false-merge analysis;
- children and adult records separately;
- shared family phone and email patterns;
- naming conventions representative of intended Catholic communities;
- complex, blended, foster, adoptive, separated, and protected-address cases;
- sanitizer direct-identifier recall;
- contextual re-identification testing;
- independent reviewer identity and independence statement;
- predetermined acceptance, restriction, suspension, and rejection thresholds.

Developer-authored and AI-generated tests remain valuable software tests. They do not constitute independent institutional validation.

### Condition 3 — Named-Human Accountability Architecture

**Required before a live-family-data pilot**

Provide or implement:

- named user authentication;
- institutional role and authority attribution;
- MFA for privileged access;
- separate permissions for view, import, merge, split, export, consent, EIM, and administration;
- mandatory reasons for high-risk decisions;
- dual review for defined child, custody, protected-address, consent, and safe-environment cases;
- session and credential revocation;
- attribution of every consequential action to a named person;
- time-bound privilege elevation where needed.

### Condition 4 — Family Correction, Appeal, and Repair Process

**Required before a live-family-data pilot**

Document:

- how an adult, parent, eligible student, guardian, or authorized representative reports an error;
- who investigates;
- required evidence;
- response timelines;
- escalation;
- correction and split procedures;
- downstream propagation;
- disclosure assessment;
- affected-person notification;
- remediation ownership;
- rule or system reform after recurring failure.

A technical rollback function is not by itself an appeal or repair process.

### Condition 5 — Field-Level Authority and Vulnerable-Family Safeguards

**Required before a live-family-data pilot**

Create an authority matrix identifying, for every sensitive field:

- authoritative source;
- permitted proposing sources;
- authorized reviewer;
- conflict-resolution authority;
- validity period;
- disclosure rules;
- retention;
- correction rights;
- whether the field may be used for matching;
- whether it may be exported or processed through AI.

Define mandatory escalation or prohibition for:

- minors;
- contested custody;
- guardianship conflicts;
- protected addresses;
- foster and adoptive cases;
- shared contacts;
- conflicting dates of birth;
- multiple active households;
- safe-environment status;
- consent changes;
- records whose merge changes disclosure eligibility.

### Condition 6 — Deployment Governance and Stopping Rules

**Required before a live-family-data pilot**

Add a deployment decision record specifying:

- accountable executive;
- data steward;
- safeguarding owner;
- security owner;
- approved data domains;
- approved connectors;
- approved consuming applications;
- approved AI destinations;
- pilot population;
- prohibited uses;
- monitoring duties;
- review cadence;
- escalation path;
- incident authority;
- exit and data-destruction procedure.

Predetermine stopping rules. At minimum, immediate suspension should follow an unauthorized protected-address disclosure, an erroneous child-to-household attachment that creates access risk, inability to attribute a consequential action, direct-identifier leakage through an approved sanitizer test, key compromise, or failure to propagate a required correction.

### Condition 7 — Data Stewardship and Security Operations

**Required before Gate 2; critical controls may be required earlier by deployment scope**

Provide:

- retention and deletion schedule by data category;
- legal-hold process;
- controlled hard-deletion or cryptographic-erasure process;
- backup encryption and restore evidence;
- key custody, rotation, recovery, and succession plan;
- breach and safeguarding incident response;
- downstream deletion and correction handling;
- approved support-access procedure;
- supported-version policy;
- vulnerability intake and remediation targets;
- SBOM, release provenance, checksums, and signed release process.

### Condition 8 — Project Governance, Maintenance, and Commercial Boundary

**Required for Gate 2**

Provide:

- maintainer and backup maintainer;
- succession and retirement procedure;
- Project Management Committee or equivalent charter;
- contributor and release authority;
- security embargo authority;
- branch and review protections;
- conflict-of-interest disclosures;
- support boundaries;
- deprecation policy;
- adopter migration and export guarantees;
- written commercial/open-source boundary;
- confirmation of the licensing and intellectual-property path required for the intended CDCF project type.

### Condition 9 — Human Influence Telemetry

**Specification required during incubation; implementation proportionate to pilot risk**

For consequential matching, merge, split, consent, export, EIM, and correction events, preserve:

- evidence available to the reviewer;
- system output and explanation;
- reviewer identity and role;
- independent reason;
- review duration;
- acceptance, rejection, override, or escalation;
- authority exercised;
- downstream effects;
- appeal;
- remediation;
- system or policy change after failure.

This evidence should support analysis of whether operators are judging or merely confirming system suggestions.

### Condition 10 — Independent Deployment Review

**Required before broad institutional endorsement**

A review team independent of project development should examine, as applicable:

- application security;
- privacy and child-data governance;
- safeguarding;
- identity resolution;
- institutional operations;
- accessibility and multilingual use;
- legal applicability;
- canonical or ecclesial implications;
- deployment recovery and incident response.

The review should publish scope, methods, limitations, findings, dissent, and remediation status.

---

## Conditions Register

| ID | Condition | Incubation | Live Pilot | Gate 2 | Status | Owner | Evidence |
|---|---|---:|---:|---:|---|---|---|
| FG-CON-01 | Correct and bound project claims | Required | Required | Required | OPEN | Project owner | — |
| FG-CON-02 | Independent validation plan and results | Plan | Partial results | Completed | OPEN | Project owner + independent reviewers | — |
| FG-CON-03 | Named-human accountability | Design | Required | Required | OPEN | Project owner / deploying institution | — |
| FG-CON-04 | Family correction, appeal, and repair | Design | Required | Required | OPEN | Deploying institution | — |
| FG-CON-05 | Field authority and vulnerable-family safeguards | Design | Required | Required | OPEN | Project owner + domain authorities | — |
| FG-CON-06 | Deployment governance and stopping rules | Design | Required | Required | OPEN | Deploying institution / TAC | — |
| FG-CON-07 | Data stewardship and security operations | Plan | Risk-based minimum | Completed | OPEN | Project owner + institution | — |
| FG-CON-08 | Maintenance and commercial boundary | Plan | Named support | Completed | OPEN | Project owner / PMC | — |
| FG-CON-09 | Human influence telemetry | Specification | Required subset | Completed | OPEN | Project owner | — |
| FG-CON-10 | Independent deployment review | Plan | Scoped review | Completed | OPEN | CDCF / independent reviewers | — |

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
