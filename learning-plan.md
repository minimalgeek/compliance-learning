**Corporate compliance: a 30-hour founder’s learning plan**

Prepared 22 October 2026. Intended audience: a technical founder exploring compliance automation. Perspective: large companies and multinational groups, with EU examples and widely used US corporate-compliance concepts.

The outcome is working literacy: understand the main specialties, follow how work gets done, interview practitioners intelligently, and choose a narrow product hypothesis. “80%” is a prioritization heuristic, not a measurable promise of legal coverage. Specialist competence comes after selecting a domain, customer segment, and jurisdiction.

Spend five hours per week for six weeks. For weeks 1–5, allocate two hours to targeted reading, two hours to a practical exercise, and one hour to a practitioner conversation plus notes. The reading times are caps; stop when you can complete the exercise. Week 6 has its own five-hour schedule. Start arranging interviews during week 1.

A useful organizing question is: **Which requirement applies to this business activity, who performs the control, and how can someone verify that it worked?**

Corporate compliance draws obligations from laws and regulations, customer and supplier contracts, and internal commitments. Voluntary standards and assurance schemes can also become commercially important through procurement and contracts. Keep their authority separate: a company policy, an auditor’s request, and a statutory obligation have different sources and consequences.

The DOJ’s Evaluation of Corporate Compliance Programs is a strong first reading because it examines program design, resources and authority, and practical effectiveness. It is US prosecutorial guidance for a specific purpose; use it to learn a program’s anatomy, then investigate the rules relevant to your market.

Read: [DOJ compliance guidance, September 2024](https://www.justice.gov/criminal/criminal-fraud/page/file/937501/dl).

The field is easiest to survey through business activities:

| Area | Business question | Common work and artifacts | Typical participants |
| --- | --- | --- | --- |
| Ethics and conduct | Are employees and intermediaries acting properly? | Code of conduct, gifts and conflicts disclosures, training, whistleblowing reports, investigations | Chief compliance officer, legal, HR, business managers |
| Bribery, competition, and trade | Can we sell, pay, collaborate, or export this way? | Intermediary due diligence, approval records, competition guidance, sanctions and export reviews | Compliance, legal, sales, procurement, trade specialists |
| Financial crime | Who is the customer, and is activity suspicious? | Customer due diligence, beneficial-owner checks, monitoring alerts, investigation and escalation records | AML teams, financial-crime operations, relevant regulated businesses |
| Financial reporting and fraud controls | Can we rely on the financial records? | Payment approvals, reconciliations, segregation of duties, control tests, audit findings | Finance, controller, SOX team, internal and external auditors |
| Privacy and data protection | May we use this personal data for this purpose? | Processing inventories, impact assessments, data-subject requests, processor reviews, breach records | Privacy team, data protection officer, legal, product, IT |
| Cybersecurity and technology assurance | Are information and systems appropriately protected? | Access reviews, security controls, incident response, supplier assessments, SOC reports and ISO audit evidence | CISO, IT, security GRC, engineering, auditors |
| Operational resilience and third parties | Can critical services survive disruption or supplier failure? | Service inventories, dependency maps, continuity tests, vendor reviews, remediation plans | Operations, procurement, resilience and risk teams |
| People, environment, supply chain, and products | Do operations and products meet their applicable duties? | Employment and safety processes, permits, supplier checks, product technical records, environmental and reporting data | HR, safety, sustainability, quality, procurement, product specialists |
| AI governance and regulatory change | What uses or rule changes create new duties? | AI inventories, use-case assessments, obligation registers, change assessments, assigned actions | Legal, compliance, privacy, model risk, product owners |

This is a teaching map. Companies distribute these responsibilities differently. Financial-crime duties depend heavily on activity and jurisdiction; customer AML programs are especially relevant to regulated sectors and other designated businesses. Sanctions and trade restrictions have a different scope. Knowing one does not establish the other’s applicability.

**Week 1: understand the organization and its compliance program.**

Learn governance, risk, compliance, internal control, and assurance as separate concepts. Learn how legal advice, business ownership, compliance oversight, and internal audit interact. Include leadership behavior, incentives, training, reporting channels, investigation, and remediation in your picture of the program.

Use the IIA’s Three Lines Model: business management runs activities and manages their risks; specialist second-line roles provide expertise, monitoring, and challenge; internal audit provides independent assurance. The board oversees the system. Reporting lines vary, and internal audit’s independence matters.

Targeted reading, two hours total:

- DOJ guidance: read the opening questions and skim the sections on risk assessment, policies, training, reporting, third parties, leadership, resources, and testing.
- [IIA Three Lines Model](https://www.theiia.org/globalassets/documents/resources/the-iias-three-lines-model-an-update-of-the-three-lines-of-defense-july-2020/three-lines-model-updated-english.pdf): focus on the role descriptions and relationships.
- [ISO 37301 public overview](https://committee.iso.org/sites/tc309/home/projects/published/iso-37301-compliance-management.html): understand the purpose of a compliance management system. The free overview is enough for this stage.

Two-hour exercise: invent a 2,000-person multinational company selling software and industrial equipment. Give it EU and US operations, distributors, cloud vendors, employees, and public-sector customers. Create a one-page map of its activities, plausible obligation areas, responsible teams, and external reviewers. Record uncertainty instead of assuming every regulation applies.

Interview: speak to one compliance professional or internal auditor. Ask them to describe their last completed piece of work, who provided inputs, and who reviewed the result.

Pass condition: explain who runs a control, who challenges it, and who independently assesses it. Identify five factors that change a company’s compliance scope: activities, legal entities, jurisdictions, data, and counterparties.

**Week 2: learn controls, evidence, testing, and assurance.**

This is the most reusable technical material. Learn inherent risk, residual risk, preventive and detective controls, manual and automated controls, segregation of duties, control design, operating effectiveness, findings, remediation, and retesting.

Learn the difference between a control definition, a completed execution, its supporting evidence, and an evaluator’s conclusion. A policy establishes an expectation. A test examines whether the relevant activity satisfied it. The existence of a document alone leaves scope, timing, and completeness unresolved.

Targeted reading, two hours total:

- [COSO internal-control overview](https://www.coso.org/guidance-on-ic): identify the five components—control environment, risk assessment, control activities, information and communication, and monitoring.
- [SEC explanation of internal controls](https://www.sec.gov/files/info/smallbus/404guide/controls.shtml): use the concepts to understand controls over financial reporting. This is introductory historical guidance, not a current determination of which SOX provisions apply.
- [AICPA SOC overview](https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services) and [ISO/IEC 27001 overview](https://www.iso.org/standard/27001): identify what each covers. SOC 2 is an attestation report; ISO/IEC 27001 is a certifiable management-system standard. Their scopes matter. Some detailed AICPA examples require an account or membership; paid material is optional.

Two-hour exercise: create a risk-and-control matrix with five rows. Include a source requirement or policy, business risk, control, owner, frequency, evidence, test, finding, and remediation. Use synthetic payment approvals, employee departures, supplier onboarding, privileged access, and expense claims.

Run this deliberately small control test:

- Fictional company policy: disable departing employees’ access to three named critical systems within 24 hours of effective departure.
- Inputs: the complete HR departure population for a month, identity records, access-change logs, and approved exceptions.
- Test: match each departure to all three systems and compare departure and disablement timestamps.
- Plant one missing system record, one late removal, and one mismatched identity.
- Record separate outcomes for pass, failure, approved exception, and insufficient evidence.
- Assign an owner and due date for failures; require a retest before closure.

A clean result depends on the completeness of the HR population and system data. A handful of successful examples cannot establish that every required event was covered. Label this a toy exercise; actual testing methods depend on scope and assurance requirements.

Interview: ask an auditor or control owner to describe evidence they rejected and why.

Pass condition: explain why a well-designed control can fail in execution, and why incomplete evidence can prevent a conclusion.

**Week 3: survey ethics, conduct, third parties, and financial crime.**

Learn the practical vocabulary around bribery, gifts and hospitality, conflicts of interest, competition risks, sanctions, export controls, customer due diligence, and suspicious-activity escalation. Include whistleblowing confidentiality, non-retaliation, case handling, and root-cause analysis.

Focus on the lifecycle of onboarding a distributor, approving a payment, receiving a report, investigating concerns, and correcting a failure. Learn which decisions need specialist review.

Targeted reading, two hours total:

- Revisit the DOJ sections on third-party management, confidential reporting, investigation, and remediation.
- [OFAC compliance framework](https://ofac.treasury.gov/media/16331/download): skim its components and root-cause examples. It addresses US sanctions compliance; it does not substitute for EU or other applicable regimes.
- [FATF risk-based approach for banking](https://www.fatf-gafi.org/content/dam/fatf-gafi/guidance/Risk-Based-Approach-Banking-Sector.pdf.coredownload.pdf): read the explanation of the risk-based approach. This 2014 conceptual guidance is optional orientation, not a current local AML rulebook.
- [DOJ’s SAP bribery case summary](https://www.justice.gov/archives/opa/pr/sap-pay-over-220m-resolve-foreign-bribery-investigations): identify the activities and intermediary relationships involved. Avoid spending your learning time memorizing penalty amounts.

Two-hour exercise: map onboarding a high-risk sales intermediary. Include intake, risk classification, due diligence, unresolved questions, approval, contract controls, payment checks, periodic review, and escalation. Add a simplified investigation workflow for a report about that intermediary.

Interview: speak to ethics/compliance, procurement risk, or financial-crime operations. Ask which inputs generate the most follow-up and which judgments require an experienced reviewer.

Pass condition: distinguish supplier due diligence, customer AML checks, and sanctions screening. Explain how a concern becomes a documented investigation and a remediation action.

**Week 4: survey privacy, security, and operational resilience.**

Learn privacy vocabulary: personal data, controller and processor, purpose, legal basis, retention, data-subject rights, processing inventories, impact assessments, and breach handling. Learn security and resilience vocabulary: assets, identity and access, incident response, supplier risk, recovery, testing, and critical-service dependencies.

Targeted reading, two hours total:

- [EDPB guide for small business](https://www.edpb.europa.eu/sme_en): focus on data protection basics, compliance activities, and individuals’ rights. The simpler explanations are useful before studying multinational complexity.
- [NIST CSF 2.0 small-business quick-start guide](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.1300.pdf): use it to understand the cybersecurity lifecycle.
- Skim the Commission’s [NIS2 overview](https://digital-strategy.ec.europa.eu/en/policies/nis2-directive) and [DORA overview](https://finance.ec.europa.eu/digital-finance/cyber-resilience_en). Learn the problems they address and the importance of scope. National implementation, sector, legal entity, and applicable text require follow-up for a real customer.

Two-hour exercise: assess a fictional cloud supplier processing customer contact details. Produce a small data-flow map, supplier-question list, evidence request, proposed mitigations, and a decision record. Include security, privacy, and continuity questions separately. Trace one possible outage and one possible personal-data incident through different response paths.

Interview: speak to privacy operations, security GRC, or third-party risk. Ask where a supplier review waits for other teams and how approvals are documented.

Pass condition: distinguish security assurance, privacy obligations, and service resilience. Explain why an ISO certificate or SOC report has to be checked for relevant scope and does not settle every supplier question.

**Week 5: learn applicability, regulatory change, and ongoing operations.**

Survey the remaining specialties through applicability: employment and safety, environmental duties, supply-chain due diligence, product regulation, tax, and AI governance. Recognize the categories and responsible experts. Detailed legal requirements belong in the specialization you choose next.

Learn how a regulatory development becomes an internal change: authoritative source, status and version, applicability review, impacted activities and controls, owner, due date, implementation evidence, testing, and reporting. Record whether something is a proposal, adopted law, guidance, or an internal interpretation.

Targeted reading, two hours total:

- [EU AI Act overview](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai): identify the roles and use cases that drive scope. Check the current official text and implementation information when a specific use case matters.
- Revisit the public ISO 37301 overview and the DOJ material on continuous improvement.
- Choose one relevant official regulator or government portal for your hypothetical company’s employment, safety, environmental, or product obligations. Read one overview or enforcement notice. Record its jurisdiction and business scope.

Two-hour exercise: choose a real published regulatory development from an official source. Create a one-page impact assessment with source and version, affected entity/activity, applicability rationale, unknowns for an expert, existing controls, gaps, assigned actions, and verification. The learning goal is a reviewable assessment, not a claim that the hypothetical company is compliant.

Add an AI-use inventory with five fictional uses. Record owner, purpose, affected people, data, vendor, applicable-role questions, and reviewer. Treat classification as a hypothesis until checked.

Interview: ask a compliance lead how changes are monitored, who decides applicability, and how completed implementation is verified.

Pass condition: show why “a regulation mentions AI” is insufficient to identify an affected company, product, or required action. Explain how to maintain a dated, reviewable interpretation.

**Week 6: turn the learning into a product hypothesis.**

Spend one hour on the existing product landscape, 90 minutes on three short interviews, 30 minutes on a scorecard, and two hours on one thin prototype.

Use these official pages to understand existing product categories. This is a learning sample, not a vendor ranking or a complete competitive analysis:

| Example | What to inspect |
| --- | --- |
| [Vanta](https://www.vanta.com/) | Security assurance, evidence collection, controls, and customer-facing trust workflows |
| [OneTrust](https://www.onetrust.com/solutions/third-party-management/) | Third-party intake, assessment, mitigation, and monitoring |
| [NAVEX](https://help.navexglobal.com/epim/content/overview/overview.htm) | Whistleblowing intake and investigation case workflows |
| [ServiceNow GRC](https://www.servicenow.com/products/governance-risk-and-compliance.html) | Risk, policy, controls, compliance, and enterprise workflow coordination |

For each, record the user, triggering event, inputs, decisions, output, integrations, and advertised automation. Product claims describe vendor positioning; customer interviews must establish whether those capabilities solve the target customer’s problem.

Across the six weeks, aim for eight conversations: three potential users of the same narrow workflow, one budget owner, one assurance reviewer, and several adjacent operators or implementers. Roles can overlap. Eight is a discovery target, not proof of market demand.

Ask for a walkthrough of a recent real example, with sensitive information removed:

1. What triggered this task, and how often does it happen?
2. Which systems, documents, and people supplied the inputs?
3. Where did the work wait, get repeated, or require follow-up?
4. What had to be checked, and who made the final decision?
5. What made the evidence acceptable or unacceptable?
6. What happened after a failure or an exception?
7. What tools are already paid for, and what work remains outside them?
8. Who owns the budget, deployment decision, and acceptance of the output?
9. What data access and integrations would a pilot require?
10. Which measurable result would justify a paid pilot?

Treat these as hypotheses worth testing:

| Workflow hypothesis | Small initial product | Possible success measure | Question to resolve |
| --- | --- | --- | --- |
| Evidence validation | Flag missing scope, dates, approvals, or source records in a specific audit request | Reviewer time and independently confirmed detection of gaps | Will reviewers accept the output and its provenance? |
| Supplier assessment assistance | Extract cited facts, identify missing information, and prepare follow-ups | Analyst time per completed assessment and rework rate | Which checks can be standardized for this customer segment? |
| Regulatory change triage | Suggest affected policies and controls with source references | Time to a reviewed impact assessment and missed-impact rate | Who supplies and approves the applicability interpretation? |
| Findings remediation | Coordinate owners, evidence, deadlines, and retesting | Verified closure time and reopened findings | Is this painful enough beyond the customer’s existing ticketing system? |

Score each hypothesis from 1–5 for frequency, effort, budget access, data access, integration burden, reviewer acceptance, measurable benefit, and differentiation from the customer’s current tools. Define the direction of each score consistently. Use scores to expose assumptions rather than manufacture certainty.

Build a prototype for one buyer, one workflow, and one bounded decision. Use synthetic or approved data. Compare it against the current process on a small set of representative cases, including missing evidence and an exception. A workflow mockup or a manually assisted prototype is enough at this stage.

Pass condition: write a one-page opportunity memo with target customer, buyer, current process, repeated pain, current tools, proposed output, human decision, required data, baseline metric, and paid-pilot proposal. Label what interviews established and what remains an assumption.

The recurring data objects are a useful guide for a technical founder:

| Object | Minimum useful information |
| --- | --- |
| Obligation | Authoritative source, version, jurisdiction, scope, interpretation owner |
| Risk | Business activity, failure scenario, impact, assessment rationale |
| Control | Intended outcome, owner, procedure, frequency or trigger, scope |
| Execution | What happened, when, by whom or which system, result |
| Evidence | Source, collection time, covered period, population, access restrictions |
| Test | Scope, method, inputs, evaluator, result, limitations |
| Finding or exception | Reason, severity, decision authority, owner, due date, status |
| Remediation | Planned change, completion evidence, verification, retest |
| Report | Audience, reporting period, conclusions, open issues, supporting references |

One control may support several requirements, and one requirement may need several controls. Reuse requires checking scope and purpose. Evidence needs a defined period and population. A link between two documents does not establish equivalence or effectiveness.

For an AI-assisted product, make source references, missing-information states, review history, and authorized approvals part of the workflow. Use deterministic checks where the criterion is explicit. Evaluate language-model suggestions against examples reviewed by a practitioner. Measure reviewer workload, material misses, false alerts, rework, and final output acceptance. A high document-processing rate alone says little about business value.

Keep a small glossary rather than memorizing acronyms:

| Term | Working meaning |
| --- | --- |
| GRC | Coordinating governance, risk management, and compliance |
| Obligation register | A maintained inventory of applicable requirements and their ownership |
| Inherent / residual risk | Exposure before controls / exposure remaining after considering controls |
| Risk-and-control matrix | A mapping of risks to controls, owners, and testing |
| Design / operating effectiveness | Whether a control is suitable / whether it worked as required |
| Assurance | An assessment intended to give stakeholders confidence, with stated scope and limits |
| Segregation of duties | Dividing incompatible responsibilities to reduce error or abuse |
| Third-party due diligence | Gathering and assessing information before and during a business relationship |
| RoPA / DPIA | Record of processing activities / data protection impact assessment |
| KYC / CDD | Know your customer / customer due diligence |
| Finding / remediation | An identified weakness / the work to correct and verify it |
| Attestation | A stated assertion; its meaning and assurance level depend on context |

Defer professional certifications, full standards, article-by-article legal study, comprehensive country matrices, detailed penalty calculations, and complex GRC implementations. Buy deeper training when a target workflow creates a concrete knowledge gap.

You are ready to specialize when you can explain a compliance workflow from trigger to verified closure, recognize a gap in evidence, identify the business owner and reviewer, and describe a repeated customer problem with a measurable cost.

Start with the DOJ’s opening questions and the IIA role descriptions. Draw the hypothetical company map, then arrange the first practitioner conversation. The strongest next investment is access to real work and its reviewers.

