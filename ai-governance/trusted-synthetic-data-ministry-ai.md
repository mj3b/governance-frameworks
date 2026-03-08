# Trusted Synthetic Data for Ministry-Scale AI

> **Document type:** Research memo

> **Status:** Working draft - U.S.A. C-DART 1 discussion

> **Relationship:** Supplementary research underlying [CDCF AI Vetting Criteria v0.1](./ai-vetting-criteria.md)

---

## Table of Contents

1. [The Core Argument](#the-core-argument)
2. [What Synthetic Data Is](#what-synthetic-data-is)
3. [The Market Signal](#the-market-signal)
4. [The Catholic Data Paradox](#the-catholic-data-paradox)
5. [What Catholic Institutions Could Build](#what-catholic-institutions-could-build)
6. [The Three-Layer Stack](#the-three-layer-stack)
7. [The Federated Architecture Imperative](#the-federated-architecture-imperative)
8. [The CDCF Role: Validation Standards, Not Data Commons](#the-cdcf-role-validation-standards-not-data-commons)
9. [Relationship to the CDCF Vetting Criteria](#relationship-to-the-cdcf-vetting-criteria)
10. [Bibliography](#bibliography)

---

## The Core Argument

Catholic institutions collectively hold one of the largest concentrations of sensitive data stewardship in America. They serve the same overlapping populations across healthcare, education, social services, and parish life in a way no secular institution can replicate. That cross-domain view is also completely inaccessible for AI development because the data is protected by HIPAA, FERPA, diocesan privacy norms, and the pastoral trust of the people it concerns.

Trusted synthetic data resolves that tension. AI systems can now generate statistically faithful but entirely artificial versions of sensitive datasets, preserving the population-level patterns that make data valuable for model training while eliminating the individual-level records that make it legally and ethically off-limits. This technology crossed the production threshold in 2025. The question for Catholic institutions is whether they develop the governance infrastructure to use it on their own terms, or whether their unique cross-domain data position remains permanently unavailable for the AI development that could serve their missions most effectively.

---

## What Synthetic Data Is

Synthetic data is algorithmically generated data that mirrors the statistical properties, distributions, and relationships of a real dataset without containing any actual records from real individuals. A synthetic patient cohort drawn from a hospital system's electronic health records preserves the clinical patterns, demographic distributions, comorbidity relationships, and outcome rates of the real population while containing zero real patients. No individual record can be traced back to a real person because no individual record from a real person was used to generate it.

The distinction between synthetic data and anonymized data is consequential. Anonymized datasets remove or mask identifying fields, but the underlying records still correspond to real individuals, and re-identification attacks have demonstrated that anonymization alone provides insufficient protection for sensitive populations. Synthetic data generates new records from learned distributions. Re-identification risk is dramatically reduced when datasets are fully synthetic, because synthetic records carry no real-world counterparts, but privacy still requires careful design and independent testing before the data can be trusted for consequential use.

Quality validation is the critical governance requirement. A synthetic dataset is valuable for AI training only if it accurately preserves the statistical properties of the source data. Validation frameworks measure fidelity — the degree to which synthetic distributions match real distributions — and privacy, the degree to which synthetic records resist membership inference attacks. Both dimensions require rigorous, independent validation before synthetic data can be trusted for consequential AI development.

---

## The Market Signal

Two market signals establish that synthetic data has crossed from experimental to production-grade infrastructure.

NVIDIA acquired Gretel, the leading synthetic data generation platform, for more than $320 million in 2025.[^1] NVIDIA's acquisition thesis was explicit: synthetic data is essential infrastructure for AI development in regulated industries where real data is legally inaccessible or practically unavailable at the scale AI training requires. The acquisition positioned synthetic data generation as a foundational capability within NVIDIA's enterprise AI stack rather than a niche privacy tool.

The U.S. Department of Veterans Affairs, through the Veterans Health Administration, has deployed MDClone as a synthetic data engine to support multiple clinical and research use cases.[^2] The VHA deployment demonstrated that synthetic data generation can operate at national health system scale under federal regulatory oversight, with validated fidelity sufficient to support clinical AI development and outcomes research.

These signals matter for Catholic institutions because they establish that the technology is production-ready and that the regulatory and governance questions — while real — are solvable. The VA deployment answers the question of whether synthetic health data can meet federal data governance requirements. The NVIDIA acquisition signals that major enterprise AI infrastructure investment is flowing into this capability.

---

## The Catholic Data Paradox

Catholic institutions face an acute version of the AI-data paradox: they hold exactly the data AI needs, and they hold it in a configuration no secular institution can replicate.

**Catholic healthcare** is the largest group of nonprofit healthcare providers in the United States: 650 hospitals and more than 2,200 total facilities caring for one in seven American patients daily, with approximately 19 million emergency visits and 5.6 million hospital admissions annually.[^3] The three largest Catholic health systems — CommonSpirit Health, Ascension, and Trinity Health — collectively operate more than 370 hospitals with combined revenues exceeding $90 billion.[^3] [^4] This data is protected by HIPAA and is largely inaccessible for cross-institutional AI development without extended IRB processes and data sharing agreements that rarely scale.

**Catholic education** enrolls 1.68 million students across 5,905 schools with more than 150,000 professional staff.[^5] These FERPA-protected records include academic performance, behavioral data, family information, and, uniquely, sacramental records. The accelerating trend toward diocesan centralized management — which has grown from 2.4 percent of elementary schools in 1990 to 18 percent in 2023 — creates both opportunity and risk: centralization enables system-wide analytics but concentrates sensitive data in ways that amplify governance obligations.[^5]

**Catholic social services and parishes** encompass 168 Catholic Charities agencies that served more than 28 million meals and provided emergency housing to 295,000 people in 2024, while responding to 52 disasters.[^6] Their data includes immigration records, counseling records, housing data, and case management information for some of America's most vulnerable populations. Thousands of parishes hold additional data on the same families across giving patterns, sacramental participation, and community engagement.

The cross-domain overlap is the distinctive asset. A family that receives care at a Catholic hospital, educates their children at a Catholic school, receives services from Catholic Charities, and participates in parish life appears in four separate Catholic data systems. No secular institution has that cross-domain view of the same overlapping populations. That view is precisely what makes Catholic data potentially valuable for AI development, and precisely what makes its governance obligations most serious.

---

## What Catholic Institutions Could Build

Synthetic versions of Catholic institutional data would unlock AI development that is currently structurally impossible.

**Healthcare.** Synthetic EHR cohorts across 650 hospitals would enable diagnostic AI development, clinical operations optimization, and multi-system research on population patterns without triggering PHI sharing workflows or extended IRB delays.[^3] Catholic hospitals disproportionately serve underrepresented and underserved populations that commercial AI training datasets consistently underrepresent. A synthetic Catholic health data commons would enable AI models trained on populations that actually reflect the communities Catholic healthcare serves.

**Education.** Synthetic student records across 5,905 schools would allow diocesan education offices to build early-warning systems for at-risk students, retention models, and system-wide performance benchmarking without real student data ever leaving its source system.[^5] The sacramental and pastoral context within Catholic school data creates dimensions of student and family life that no secular education dataset captures.

**Social services.** Synthetic case management data across 168 Catholic Charities agencies would enable program effectiveness analysis, cross-agency learning, and neighborhood-level modeling of vulnerability and need — including predictive models for homelessness, food insecurity, and family crisis — without exposing individual client identities.[^6] The combination of social services data with parish community data creates a neighborhood-level picture of human need that has no secular equivalent. This use case is a direct technical execution of the Church's Preferential Option for the Poor: AI systems built on this infrastructure would see and serve the marginalized without exploiting their data, ensuring that the most vulnerable populations benefit from AI development rather than being rendered invisible by datasets that consistently underrepresent them.

**Research partnerships.** Academic medical centers and public health researchers face chronic data access constraints for studies on underserved and minority populations. Catholic health systems serve those populations at scale. A governed synthetic data infrastructure would position Catholic institutions as research partners for NIH-funded studies, public health initiatives, and academic collaborations, generating both research impact and institutional revenue without exposing real patient data.

A governance obligation follows from each of these use cases. The USCCB's AI principles are direct: automated decision-making systems used in healthcare, education, and social services can reinforce existing biases or introduce a utilitarian approach that displaces necessary human considerations.[^7] The USCCB further teaches that technology should "supplement what human beings do, not replace them or their moral judgments."[^7] Models trained on Catholic synthetic data must be designed to supplement the judgment of doctors, teachers, and social workers, and the CDCF certification criteria for applications using synthetic data should require that human professionals retain ultimate decision-making authority.

U.S. Catholic institutions also serve large populations of Latin American descent, particularly in healthcare and social services. The Latin American and Caribbean Episcopal Council has called for AI applications to be critically evaluated in particular local contexts to determine whether they genuinely promote human dignity and the common good.[^8] The federated synthetic data framework provides exactly the mechanism needed to safely develop and evaluate AI serving these specific demographic communities, ensuring that context-specific needs shape the models rather than being obscured by them.

---

## The Three-Layer Stack

A Catholic synthetic data infrastructure operates across three layers that correspond to the same institutional capacity levels described in the governance-as-code memo.

**Infrastructure layer.** Production synthetic data generators — including platforms like NeMo, MDClone, and SAS — deployed into Catholic health systems and other large entities with standard templates and controls for PHI/PII-sensitive pipelines. This layer handles the technical generation and fidelity validation of synthetic datasets. It requires meaningful data engineering capacity and is appropriate for large Catholic health systems and university research centers.

**Governance platform layer.** A Catholic-specific synthetic data governance framework that encodes quality validation standards, ERD alignment requirements, diocesan and USCCB hierarchy compliance, and access-control patterns as reusable policy and process. This is where the CDCF is positioned to make its most distinctive contribution: serving as the steward of the validation standards and certification criteria that make synthetic Catholic data trustworthy for downstream use, rather than operating as a data commons itself.

**Application layer.** Ready-made tools that run on synthetic datasets: diocesan dashboards for education analytics, Catholic Charities program evaluation tools, and parish community health models. These applications consume validated synthetic data without requiring the institutions using them to manage the generation infrastructure directly.

---

## The Federated Architecture Imperative

A critique raised in C-DART 1 session discussions warrants direct acknowledgment: data heterogeneity across legally independent Catholic institutions would make a pooled Catholic data commons technically unsound. Catholic hospitals, schools, and Charities agencies operate under different legal entities, different regulatory frameworks, and different diocesan governance structures. Their data schemas, data quality, and data governance norms are incompatible in ways that would produce noise rather than signal if combined naively.

That critique is accurate, and it has a specific architectural response: federated synthetic data generation rather than pooled data commons.

In a federated architecture, synthetic data generation occurs locally at each institution using its own source data. The generated synthetic datasets — rather than the real data — are what move between institutions or become available for research and AI development. Each institution retains full control over its source data. The CDCF's role in this architecture is to establish the validation standards and certification criteria that ensure synthetic datasets generated at different institutions are interoperable and trustworthy, without requiring those institutions to share or pool their underlying real data.

This reframes the CDCF's contribution from data infrastructure operator — a role that would require legal authority, technical capacity, and governance structures the Foundation currently lacks — to standard-setter and validator, a role that aligns precisely with what the CDCF is designed to do.

---

## The CDCF Role: Validation Standards, Not Data Commons

The CDCF is positioned to make three specific contributions to Catholic synthetic data infrastructure that require governance expertise rather than data operations.

**Validation standards.** Defining the fidelity and privacy thresholds that a synthetic dataset must meet to be certified as trustworthy for Catholic institutional use. What statistical distance from the source distribution is acceptable? What privacy attack resistance is required? What domain-specific validation criteria apply to health, education, and social services data respectively? These questions require expertise in both data science and Catholic institutional governance, and their answers should be shared standards rather than solved independently by each institution.

**Certification criteria.** Defining what a synthetic data generation process must demonstrate to receive CDCF certification. This parallels the vetting criteria for AI tools: a generation platform that meets CDCF certification criteria gives Catholic institutions assurance that synthetic data produced on that platform meets the shared validation standard.

**Interoperability requirements.** Defining the data standards and schema conventions that allow synthetic datasets generated at different Catholic institutions to be combined or compared for multi-institutional research. This is the technical complement to the governance interoperability that the vetting criteria provide for AI tools.

---

## Relationship to the CDCF Vetting Criteria

Criterion 7 of the [CDCF AI Vetting Criteria](./ai-vetting-criteria.md) addresses training data governance directly: a tool trained on data from Catholic institutions carries an obligation to those institutions and to the populations they serve, and the terms under which that data was used must be disclosed and evaluated as part of the graduation review.

That criterion anticipates a future in which Catholic institutions are actively developing AI tools trained on Catholic institutional data. Trusted synthetic data infrastructure is what makes that future possible at scale. An institution that deploys validated synthetic data generation can develop AI tools for its own use and contribute to shared Catholic AI development without the legal exposure and governance burden that use of real institutional data would require.

The three research memos — fragmentation, governance-as-code, and trusted synthetic data — form an integrated argument. Fragmentation establishes why shared governance standards are urgent. Governance-as-code provides the deployment enforcement architecture. Trusted synthetic data provides the data infrastructure that allows Catholic institutions to develop AI worthy of that governance architecture.

---

## Bibliography

[^1]: Paresh Dave, "Nvidia Reportedly Acquires Synthetic Data Startup Gretel," *TechCrunch*, March 19, 2025, https://techcrunch.com/2025/03/19/nvidia-reportedly-acquires-synthetic-data-startup-gretel/. NVIDIA declined official comment; no corporate press release has been issued.

[^2]: U.S. Department of Veterans Affairs, Veterans Health Administration, "Synthetic Data to Improve Veteran Care," VA News, December 2020, https://news.va.gov/81908/synthetic-data-improve-veteran-care/.

[^3]: Catholic Health Association of the United States, *Catholic Health Care in the United States* (Washington, DC: Catholic Health Association, 2024), https://www.chausa.org/about/facts---statistics.

[^4]: CommonSpirit Health, *Audited Consolidated Financial Statements as of and for the Years Ended June 30, 2024 and 2023* (Chicago: CommonSpirit Health, 2024), https://www.commonspirit.org/content/dam/shared/en/pdfs/investor-resources/2024-CommonSpirit-Health-Annual-Report.SECURED.pdf.

[^5]: National Catholic Educational Association, *United States Catholic Elementary and Secondary Schools 2023–2024: The Annual Statistical Report on Schools, Enrollment and Staffing* (Arlington, VA: NCEA, 2024), https://www.ncea.org/NCEA/NCEA/Who_We_Are/About_Catholic_Schools/Catholic_School_Data/Catholic_School_Data.aspx.

[^6]: Catholic Charities USA, *Pathways Forward: 2024 Annual Report* (Alexandria, VA: Catholic Charities USA, 2025), https://www.catholiccharitiesusa.org/publications/2024-annual-report/.

[^7]: United States Conference of Catholic Bishops, *Joint Letter on Artificial Intelligence Principles and Priorities*, June 9, 2025, https://www.usccb.org/resources/joint-letter-artificial-intelligence-principles-and-priorities.

[^8]: Latin American and Caribbean Episcopal Council (CELAM), *Inteligencia Artificial: Una mirada pastoral desde América Latina y el Caribe* (Bogotá: CELAM, May 2025), https://adn.celam.org/celam-presenta-documento-inedito-sobre-inteligencia-artificial-una-mirada-pastoral-desde-america-latina-y-el-caribe/.
