# Week 7 · Inside an AI compliance team

“Can we ship on Friday?” Éva asks the engineer to open applicant number 21. The dashboard says *All applicants*. The vacancy contains 300 fictional applications. Whichever tab he opens, he can reach only the first 20. The test suite passed that morning. Its largest vacancy had twelve applicants.

DunaWorks is a Hungarian-headquartered software developer with 2,000 employees and German and US operations. It builds and markets an AI recruitment platform under its own name. The employers who buy it employ the recruiters. Éva is the provider’s AI compliance officer. Her immediate task is to get the right decision made about this build. Her longer-term task is to make the company better at catching the next problem.

> Magyarul: A megfelelőségi szakértő utánajár, melyik előírás melyik üzleti döntést érinti, ki tud változtatni a működésen, és milyen bizonyíték alapján lehet az ügyet lezárni.

**Five-hour field guide.** Allow 75 minutes for the chapter, 45 for the original readings, 90 for the case workshop, 45 to design a pilot and 45 for a practitioner interview and notes. You will produce an ownership map, a reasoned release recommendation and an evaluation plan for one automation. All company policies, people, events, targets and results are fictional.

### Chapter map

**I. People, terminology and provider responsibilities**

- [Who can change what?](#who-can-change-what)
- [What the officer does between releases](#what-the-officer-does-between-releases)
- [The vocabulary of rules and exposure](#the-vocabulary-of-rules-and-exposure)
- [The vocabulary of controls and cases](#the-vocabulary-of-controls-and-cases)
- [From a signal to an owned case](#from-a-signal-to-an-owned-case)
- [Which AI rules reach this product?](#which-ai-rules-reach-this-product)
- [Inside the provider’s evidence file](#inside-the-providers-evidence-file)

**II. A release, an incident and the management response**

- [Monday: walk the workflow with a recruiter](#monday-walk-the-workflow-with-a-recruiter)
- [Tuesday: choose controls for different harms](#tuesday-choose-controls-for-different-harms)
- [Wednesday: build evidence someone else can test](#wednesday-build-evidence-someone-else-can-test)
- [Thursday: decide, escalate and document dissent](#thursday-decide-escalate-and-document-dissent)
- [After launch: complaints, incidents and recovery](#after-launch-complaints-incidents-and-recovery)
- [How the team reduces risk across the company](#how-the-team-reduces-risk-across-the-company)

**III. Automation, workshop and reference**

- [Design the platform around decisions and evidence](#design-the-platform-around-decisions-and-evidence)
- [Choose a pilot and measure it honestly](#choose-a-pilot-and-measure-it-honestly)
- [Workshop: take the officer’s chair](#workshop-take-the-officers-chair)
- [Answer key and a reusable decision record](#answer-key-and-a-reusable-decision-record)
- [English–Hungarian desk glossary](#englishhungarian-desk-glossary)
- [Original readings and where to look](#original-readings-and-where-to-look)

## Who can change what?

At 09:30 Éva has three calls to make. Product can say what the shortlist promises. A recruiter at a pilot customer can demonstrate what users do under time pressure. QA, the quality assurance team, can establish what this build actually did. Asking each one “Is the feature compliant?” would give her three opinions and little usable evidence.

The Institute of Internal Auditors’ **Three Lines Model** helps explain who is accountable. Business management delivers the product and manages its risks. Specialist functions such as compliance advise, monitor and challenge. Internal audit can independently assess both. The board oversees management. A “line” describes a role; headcount and reporting structures vary. [IIA role descriptions](https://www.theiia.org/globalassets/documents/resources/the-iias-three-lines-model-an-update-of-the-three-lines-of-defense-july-2020/three-lines-model-updated-english.pdf)

| Decision | Who does the work at DunaWorks? | Who answers for the outcome? |
| --- | --- | --- |
| Define the product and proposed use | Product manager documents recruiter tasks, target markets and system limits. An engineering lead confirms implementation. | Product director owns product risk and resources. |
| Interpret the rule | Counsel interprets the legal text. Privacy and employment specialists supply their assessments. Éva translates approved interpretations into review questions. | Named legal reviewer signs the interpretation. Head of compliance owns the review procedure. |
| Run a safeguard | Engineering builds it. QA tests the release candidate. Customer success teaches recruiters how to use it. | Named control owner ensures it operates and failures are followed up. |
| Decide a disputed launch | Éva records dissent and escalates. Risk committee considers scope, options and authority. | Delegated executive records a decision within their mandate. Applicable legal duties still bind the company. |
| Assess the program | Internal audit selects its own sample and can examine whether Éva’s team challenged product leadership. | Head of internal audit reports independently to the governing body under its charter. |

**Agent opportunity.** Route the specific question to the role with evidence or authority. Populate a decision record from the current delegation register, including entity, scope and expiry. If the product director is also the proposed independent reviewer, flag the conflict. The platform should preserve who actually decided and which delegation applied that day.

## What the officer does between releases

Monday’s queue also contains a recruiter’s complaint, a contract renewal for the underlying model and a request for updated customer guidance. Éva starts with possible harm already occurring. She asks support when the complaint was received, whether the feature is live and who can contain it. A compliance analyst takes the renewal. The routine document update can wait until the new behavior is understood.

| Rhythm | What the team does and leaves behind | Agent opportunity and review |
| --- | --- | --- |
| Daily intake | Analyst identifies duplicates, impact, urgency and missing facts. Éva assigns an owner and selects the investigation or change-review route. | Group related signals while retaining each original receipt time. Suggest priority with a reason. Éva can override it. |
| Weekly case meeting | Product, engineering, legal and compliance resolve a short list of blocked decisions. Minutes name the decision owner, evidence needed and next review date. | Build the agenda from cases awaiting decisions. Draft precise questions and carry forward unresolved items. Meeting chair confirms assignments. |
| Monthly monitoring | Analyst tests a sample of releases, including ordinary changes that never reached the compliance queue. Éva investigates common omissions. | Reconcile deployment records to review records. Record the denominator and the sample rule. Reviewer checks unexplained omissions. |
| Quarterly planning | Head of compliance maps exposures across products and markets, weighs impact and likelihood, allocates specialists and reports recurring failures to executives. | Assemble exposures, coverage gaps, overdue actions and evidence behind trends. Management chooses priorities and funds work. |
| Annual and event-driven review | Leadership revisits decision authority, policies, staff competence and the monitoring plan. A new market or material product change can trigger an earlier review. | Identify stale owners, changed uses and training linked to obsolete procedures. Policy owner approves revisions and effective dates. |

A **compliance universe** (*a megfelelőségi vizsgálatok lehetséges teljes köre*) is the set of entities, products, activities and obligations the team could cover. A **risk-based monitoring plan** (*kockázatalapú ellenőrzési terv*) says which it will examine, when, and why. If four product squads ship weekly and Éva can inspect two releases a month, she can target changes affecting recruitment decisions and sample ordinary releases for blind spots. Record what went unexamined. That fact matters when management asks how much confidence to place in a green report.

## The vocabulary of rules and exposure

When a customer writes “the law requires all candidates to be visible,” Éva asks for the source. In this case, displaying every eligible applicant is DunaWorks’ approved product promise and internal control design. Counsel separately interprets legal duties. Keeping those origins distinct lets the company change a design responsibly and explain why the old design existed.

| Record and Hungarian term | Question it answers | DunaWorks example |
| --- | --- | --- |
| Obligation · kötelezettség | Who owes what, under which authority, for which use and period? | A signed customer term requires access to all eligible applications for the vacancy. Legal requirements have their own entries. |
| Policy · szabályzat | What rule has management adopted? | Changes affecting applicant visibility need a documented release review. |
| Procedure · eljárásrend | How does a named operator perform the work? | QA opens the candidate build with recruiter permissions and traverses each page. |
| Intended purpose · rendeltetés | What use, users and conditions does the provider describe? | Help employers prioritize applications for recruiter review. Compare sales claims, instructions and product design. |
| Risk scenario · kockázati forgatókönyv | Through what mechanism might someone suffer harm? | A qualified applicant is ranked low and becomes unreachable to the recruiter. |
| Inherent / residual risk · eredendő / fennmaradó kockázat | What is the exposure before safeguards, and what remains afterward? | Making everyone reachable addresses visibility. Recruiters might still review only the first twenty. |
| Risk appetite / tolerance · kockázatvállalási hajlandóság / kockázattűrés | What exposure will management take, and what boundary triggers action? | Management permits a synthetic pilot. Its release rule requires full eligible-ID coverage before live rollout. |

**Try the distinction.** “Unfair recruitment” is too broad for an engineer to act on. “A parser gives no score to a nonstandard CV; the query drops unscored records; a recruiter cannot consider the candidate” is testable at three points. Product can design a fallback, QA can plant an unscored example and compliance can ask whether it remains visible.

**Agent opportunity.** Draft a register entry with the source passage, version, business activity and interpretation owner. Mark whether the source is law, contract or internal policy. Extract possible risk scenarios from changes to the intended purpose. A reviewer links the relevant records and approves the interpretation. Similar wording alone gives the platform no basis to merge two obligations.

## The vocabulary of controls and cases

Éva asks, “Did the control work?” QA sends a test plan; engineering sends a completed run. Both are useful, but the plan describes a method and the completed run is evidence about a particular build. A data model that stores both as “documents attached” hides the difference.

| Object and Hungarian term | Minimum useful record in the shortlist case |
| --- | --- |
| Control · kontroll, kockázatot mérséklő intézkedés | C-4: recruiter can reach every eligible ID independently of rank. Owner, scope, expected behavior and trigger. |
| Control execution · a kontroll végrehajtása | Release test R-88: operator, release candidate, tenant configuration, time, inputs and actual result. |
| Evidence · bizonyíték, alátámasztó adat | Source export, fixture manifest and recruiter-view observations with versions, collection time, scope and access rights. |
| Test / assessment · ellenőrzési próba / értékelés | Compare expected and reachable sets. Evaluator records method, result, uncertainty and limitations. |
| Finding · vizsgálati megállapítás | F-21: 280 eligible IDs unreachable on build A in staging. Link criterion, observed condition, consequence and owner. |
| Remediation / retest · helyesbítés / ismételt ellenőrzés | Fix pagination and verify the corrected release with a boundary case and the original 300-ID population. |
| Exception · jóváhagyott eltérés | A competent owner permits a precisely scoped departure from an internal rule until a date, with conditions. Preserve its authority. |
| Incident / complaint · incidens / panasz | A customer reports an adverse event or concern. Preserve original report, exposure, facts, awareness times and response. |

A **design assessment** (*a kontroll kialakításának értékelése*) asks whether the safeguard could address the risk if performed as specified. **Operating effectiveness** (*a kontroll működési eredményessége*) asks whether it worked in the stated scope and period. A passing run on build B supports one release decision. Evidence from a single run leaves the operating history of fifty releases unknown.

**Agent opportunity.** Give each object an ID and link it to the exact version examined. One risk can require several controls; one control can support several obligations. A finding can reopen. A complaint can create a separate incident case linked to the original finding. Preserve historical conclusions when a policy, build or interpretation changes so an auditor can reconstruct yesterday’s decision.

## From a signal to an owned case

A **signal** (*jelzés*) is an input worth examining. A **case** (*ügy*) groups facts and decisions about a defined question. A **task** (*feladat*) is work assigned inside the case. A pull request, a revised product document and a customer support ticket can refer to the same feature. They arrive from different people, at different times, with different access rights.

Take the shortlist PR. An analyst opens case AI-17, records the EU hiring product and release candidate, and asks whether the change alters applicant visibility. The responsible reviewer is Éva. The analyst links the PR and specification. A task goes to QA for a recruiter-view test. A separate model-risk review remains with the evaluation lead.

| Case transition | Evidence or authority for the transition | Agent opportunity |
| --- | --- | --- |
| Received → triaged | Analyst establishes product, urgency, possible harm and affected release | Suggest a matching case and route. Keep ambiguous matches separate for review. |
| Triaged → awaiting evidence | Reviewer names the missing fact, its source and owner | Request the missing build or fixture under the case’s permissions. Track response and age. |
| Assessed → action open | A finding cites the criterion and observed failure | Draft a remediation ticket linked to the finding. Owner confirms due date and scope. |
| Action open → awaiting retest | Owner supplies a new build and describes the correction | Trigger the authorized test on the new version. Keep the original failed run. |
| Verified → closed | Reviewer accepts the evidence for the named finding. Release authority separately decides launch. | Draft the closure and release records. Record each authorized decision independently. |
| Closed → reopened | New complaint, regression or invalidated assumption changes the evidence | Alert the former owner and show the triggering fact alongside the old conclusion. |

**Other exits matter.** A duplicate can be linked and retired; a reasoned out-of-scope decision records why; an inconclusive review stays open or is escalated with its limitation visible. An “approved exception” needs scope, expiry and an authorized decision. A missed due date tells the agent whom to notify. It supplies no evidence that the underlying work passed.

> Magyarul: A „lezárt fejlesztői jegy”, a „visszaellenőrzött megállapítás” és az „engedélyezett éles kiadás” három külön döntést jelent. Más személy más bizonyíték alapján hozhatja meg őket.

## Which AI rules reach this product?

DunaWorks develops and markets the system under its own name, making it the **provider** (*szolgáltató*) in this exercise. An employer uses it to recruit under its authority and is the **deployer** (*alkalmazó*). Buying an upstream model does not transfer the finished product’s provider role to the model vendor. Write down the entities, EU market, intended purpose, product version and actual customer workflow. [EU AI Act, Article 3](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?qid=1789944163546&uri=CELEX%3A02024R1689-20260727)

Recruitment, application filtering and candidate evaluation are listed in Annex III, point 4(a). Here ranking directly influences which candidates receive attention. Counsel records a working high-risk classification, considers Article 6 including its limited derogation and profiling provision, and signs the scope decision against the facts. As checked on 17 November 2026, the Commission gives **2 December 2027** for the Annex III employment high-risk rules. Identify the placing-on-market date, transitional provisions and applicable rule for the specific system. Privacy, employment, contracts and other AI Act provisions have their own applicability and timing. [Annex III](https://ai-act-service-desk.ec.europa.eu/en/ai-act/annex-3) · [Article 6](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-6) · [Commission timeline](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)

**What lands on Éva’s desk?** A legal memo becomes a list of work. For example, data and model leads own evaluation records; product and engineering own documentation, oversight features and logs; quality management coordinates procedures and controlled changes. The provider needs a reasoned assessment of applicable conformity assessment, declaration, marking, registration and lifecycle obligations. Passing the shortlist test addresses one narrow design claim. The next section follows the evidence those teams maintain.

**Regulatory change** (*jogszabályváltozások követése*). Counsel dates an interpretation and identifies assumptions that could invalidate it. A move from ranking candidates to automatically rejecting them triggers fresh review of purpose, product claims and impact. An amended date triggers a scheduling review. These are different events.

**Agent opportunity.** Watch authorized official sources and versioned product documents. Diff the operative provision or changed purpose, retrieve impacted decisions and draft questions for counsel. The output should show issuer, law version, effective date, evidence and uncertainty. Counsel determines applicability; Éva coordinates owners and deadlines for the approved interpretation.

## Inside the provider’s evidence file

A customer asks sales, “Has your AI been certified?” Sales forwards the question to Éva. She asks which product version, market, claim and assurance scheme the customer means. A customer security questionnaire, an internal release test and a statutory conformity assessment each answer a different question. She gives sales a scoped response it can substantiate.

**Conformity assessment** (*megfelelőségértékelés*) is the procedure for demonstrating compliance with applicable requirements. For the standalone Annex III point 4 hiring system in this example, Article 43(2) points to internal control under Annex VI, without a notified body. Check the applicable text, timing and precise product facts. Before market entry the provider needs to assemble and maintain the relevant technical documentation, assess conformity and address the applicable declaration, marking and registration steps. An internal route still requires substantive evidence. [Articles 11, 43, 47–49 and Annexes IV and VI](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?qid=1789944163546&uri=CELEX%3A02024R1689-20260727)

| Evidence area | Who supplies what? | Agent opportunity and reviewer |
| --- | --- | --- |
| Purpose and architecture | Product describes intended users and limits; engineering identifies the model, data flows, integration and build. | Compare approved product descriptions, model references and sales claims. Product resolves inconsistent promises. |
| Data and evaluation | Model lead records data origin, limitations, population coverage, evaluation design, results and known weaknesses. Privacy checks permitted handling. | Link each claim to its evaluation version; flag changes to data or model after the run. Evaluator assesses representativeness and material gaps. |
| Human oversight and performance | Design lead demonstrates how recruiters see, interpret and override recommendations; QA records accuracy, robustness and relevant security tests for the system and its context. | Assemble test records by requirement and scope; expose conditions never tested. Specialists judge adequacy. |
| Quality and lifecycle | Quality lead owns controlled procedures, change history, monitoring and corrective actions. Authorized provider representatives handle formal attestations. | Build a versioned evidence index, list outstanding items and prepare drafts. Accountable staff verify the dossier and sign within their authority. |

**A concise customer answer.** “We can share the approved description and evaluation summary for the named release under the agreed access terms. Please identify the certification scheme or legal declaration your request refers to.” An agent can retrieve exactly what may be shared and which version is current. Éva checks that a sales answer stays within the evidence.

## Monday: walk the workflow with a recruiter

**09:15, release call.** The PR description promises a faster default list. The specification promises access to all eligible applicants. Éva asks the engineer to demonstrate the build and a pilot recruiter to describe a busy morning. “If I have a hundred applications and an hour, I start with the first screen,” the recruiter says. Éva writes down two hypotheses: the system may technically hide candidates, and users may systematically overlook people who remain accessible. Each needs its own test and owner.

**10:10, evidence request to QA.** “For build A, please provide the complete synthetic vacancy manifest, our eligibility rule, recruiter role, feature settings, and all IDs reachable through the two tabs. Include candidates without scores. Tell me if pagination or export limits prevent a complete result. QA can use synthetic IDs for this test.” This is an **evidence request** (*bizonyítékbekérés*). It states the claim a reviewer must be able to verify.

**11:00, population agreed.** QA confirms one synthetic EU vacancy has 300 distinct eligible applications. Withdrawn applications were excluded before freezing the manifest. Zero-score and unscored applications remain eligible. “All” means reachable in this vacancy through the recruiter’s normal interface with ordinary permissions. Administrator database access answers a different question. Product owns that definition. QA captures the manifest before reading the result.

**13:00, intake decision.** Build A’s recruiter view exposes twenty distinct eligible IDs. All 300 were expected. The test environment is documented and the run covers every page the interface exposes. Éva opens F-21 for the missing 280. She does not infer that 280 real people were rejected. The test used synthetic applications in staging. Release operations checks whether any customer had a live flag; unknown exposure would change triage priority.

**Agent opportunity.** Detect the PR against the shortlist component, retrieve the approved specification and draft a narrowly scoped evidence request. Record received facts as observed, reported or inferred. An unexecuted diff is a lead; QA’s reproducible run establishes the behavior of this build. Give customer-support evidence its own visibility rules even if its case reference is shared with engineering.

## Tuesday: choose controls for different harms

Éva asks the product director to describe the affected person before assigning a severity. An inaccessible profile can cost an applicant an interview. High volume increases the number of people exposed. Production exposure, likelihood of repetition and reversibility affect priority. A numeric score without these facts gives management little basis for choosing an action.

| Failure scenario | Treatment, owner and test | Agent opportunity |
| --- | --- | --- |
| Shared query hides everyone below rank 20 | Engineering keeps the recommended list capped and makes the full queue independently pageable. QA tests reachable ID sets at 19, 20, 21 and 300. | Propose boundary fixtures, execute approved checks and attach build-specific evidence. |
| Unscored CVs disappear | Parsing failures enter an accessible manual-review queue. Product defines what recruiters see; QA plants a valid unscored record. | Reconcile parser outcomes with both queues. Route unmatched IDs and record denominator. |
| Qualified applicants with unfamiliar titles rank lower | Evaluation lead defines comparable qualification examples and assesses ranking performance across relevant groups where data use is lawful and suitable. Product reviews evidence of harm and options. | Draft paired examples; version the evaluation dataset, model and criteria. A specialist validates comparability, legal basis, metrics and conclusions. |
| Recruiters treat rank as a hiring decision | Product designs an override and explains limits; customer success runs a task-based usability test with pilot recruiters under realistic time pressure. | Assemble authorized usage summaries and test scripts. Surface evidence of whether recruiters could find, understand and use the alternative view. |
| Upstream model changes after evaluation | Vendor manager identifies affected versions and notice terms. Model owner qualifies the update, tests regressions and documents rollback. | Compare vendor notice and deployed model inventory; reopen affected tests. Mark missing version evidence explicitly. |

**Risk treatment** (*kockázatkezelési intézkedés*) can mean avoiding the use, changing the design, reducing exposure through rollout limits, or accepting a remaining exposure within delegated authority. A contract can allocate responsibilities and some financial consequences. It cannot restore an applicant’s missed opportunity. The director can disable ranking and ship other features if fixing it would miss the launch date.

**Challenge for the officer.** Training is useful when a recruiter needs to learn how to reach another view. It cannot make an inaccessible record appear. Tie every mitigation to the mechanism of harm and ask what observation would show the mitigation failed.

## Wednesday: build evidence someone else can test

**Control C-4.** Each eligible application for a vacancy must be reachable through the customer recruiter view regardless of rank or score. Engineering owns implementation; QA owns the release test; Éva reviews evidence for high-impact changes. The rule is fictional. Its wording matters: “all eligible” gives QA a population, “recruiter view” fixes the identity, and “regardless of score” makes the unscored case necessary.

| Test element | Worked instruction |
| --- | --- |
| Expected population | Freeze eligible synthetic IDs from the submission manifest using the approved eligibility rule and time window. Record excluded withdrawals. |
| Observed population | Use an ordinary recruiter login on the release candidate. Traverse every exposed page in the full queue. Capture IDs, duplicate rows and access errors. |
| Compare | Compute expected IDs missing from the view and unexpected IDs present. Count duplicate rows separately. Equal counts can hide substitution. |
| Decide | A complete trusted run with missing IDs establishes a failure. An interrupted traversal leaves the result inconclusive. An unexpected applicant from another tenant triggers separate access and privacy triage. |
| Preserve | Attach the run ID, candidate build, model/config version where relevant, vacancy, test identity, time, manifest, output, method and reviewer. Restrict access to evidence. |

**The fix.** Engineering decouples the capped query from the full-queue endpoint. Build B returns 300 rows. One ID appears twice; one eligible applicant is absent. The count matches and the set fails. Build C returns 300 distinct expected IDs, no extras and no duplicates. QA verifies the unscored fixture is among them. The comparison supports closing the observed visibility defect on build C in this configuration. A different customer integration or build needs its own evidence.

**Root cause** (*kiváltó ok*) explains how the weakness survived: both views shared a capped query and the largest automated fixture had twelve records. **Correction** restores the queue. **Corrective action** reduces recurrence by adding boundary tests and a release check for shared-query changes. A reviewer can verify the correction today and leave the recurrence-prevention action open until it has run.

**Agent opportunity.** Use deterministic set comparison for the outcome. Let an agent assemble the manifest and run references, explain a failed pair, request missing context and draft the finding. A green run on a superseded commit or a different feature flag cannot support this release decision.

## Thursday: decide, escalate and document dissent

Sales has promised the new shortlist on Friday. The product director asks whether the VP can “sign off the risk.” Éva first asks what decision the VP is empowered to take. DunaWorks’ fictional delegation permits the director to release unaffected functionality with ranking disabled. An exception to the internal release policy requires committee approval. Counsel checks whether any applicable external duty limits the available options.

**Release memo AI-17.** Requested decision: ship build C to the contracted pilot scope or keep ranking disabled. Criterion: every eligible candidate reachable by an ordinary recruiter. Only 20 of 300 eligible IDs were reachable on build A; B returned 300 rows with one duplicate and one omission; C matched all 300 distinct IDs. Evidence: QA runs A–C against the frozen manifest. Limitation: synthetic staging test, one integration, one role. Separate open question: meaningful human oversight under peak workload. Owner: product director. Recommendation: ship the pagination fix; keep ranking disabled for live customers pending the workload review. Decision required Thursday at 16:00 under internal release procedure.

**Meeting record.** The director accepts the recommendation. Release operations verifies the live flag is off, records the build and rollout scope, and gives support the decision. Éva closes F-21 only when the reviewer accepts the fix for the tested scope. The workload action retains its own owner, due date and acceptance test. Support should be able to tell a customer precisely what changed.

**What if the director disagrees?** Éva records the alternative, her evidence and unresolved risk, and requests a decision from the named escalation authority. An exception request states the internal rule, reason, alternatives, expiry, affected customers, interim safeguards, monitoring owner and revocation trigger. The committee can decline. Expiry triggers fresh action; silence cannot renew it. A product executive cannot vote away a binding legal requirement.

**Agent opportunity.** Assemble the decision packet, verify signatory delegation and detect that an earlier run refers to build B. Route the draft to the committee if authority is insufficient. Record who approved which version and any dissent. If a new commit or flag change lands after approval, flag the scope change and request review before carrying the decision forward.

## After launch: complaints, incidents and recovery

Six weeks later, assume a separate workload study was reviewed and a limited live pilot authorized. A customer writes, “Candidates transferred from another vacancy disappear from All applicants.” The shortlist fix passed, but the original manifest contained only direct submissions. Éva creates a linked case for a different ingestion path. She asks the customer when the issue started and whether anyone might still be waiting for review.

| Stage | What people do | Agent opportunity |
| --- | --- | --- |
| Triage and contain | Support records receipt, affected versions and customer. Incident lead decides whether to disable the affected path or provide a safe manual queue. | Group related reports, preserve original times, identify authorized contacts and show which tenants used that build. |
| Establish exposure | Engineering compares transfer records with destination queues. Customer operations checks which hiring decisions are still reversible. | Reconcile pseudonymous IDs in the approved environment. Flag missing transfer history and distinguish confirmed from possible exposure. |
| Assess reporting | Legal and privacy assess actual facts, roles, jurisdictions, applicable dates and contractual or statutory notification triggers. Preserve awareness times and reasons. | Retrieve current reporting procedures and draft a timeline. Qualified staff decide reportability, recipients, timing and communications. |
| Correct and restore | Fix the transfer path. Reconcile the affected population and coordinate re-review of recovered applications with the employer. | Track recovery and customer acknowledgement separately from software deployment. List cases with unknown outcomes. |
| Learn and verify | Éva checks that subsequent tests include transfers. Product updates guidance. Quality lead checks whether other ingress paths have the same blind spot. | Reopen affected controls, propose new regression fixtures and collect evidence from the next relevant release. |

A **complaint** is a signal from someone affected. A **confirmed incident** establishes that an event occurred. A **reportable serious incident** has a legal definition and conditions that need assessment. For high-risk systems the AI Act distinguishes post-market monitoring from serious-incident reporting. Counsel checks the applicable law and reporting clock for the event. The company should preserve facts while that assessment is underway. [AI Act Articles 72 and 73](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-72) · [Serious-incident reporting](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-73)

> Magyarul: A hiba javítása és a következmények rendezése külön feladat. A javított verzió már megjelenítheti az áthelyezett jelölteket, de ettől a korábban kimaradt pályázatokat még nem vizsgálta meg a munkáltató.

## How the team reduces risk across the company

A month later Éva finds a pattern: three squads test the happy path with fewer records than the limits in their production queries. Chasing three tickets will fix three releases. Changing the testing procedure can catch the same problem in future products. This is where the head of compliance earns a place at the executive meeting: she can show management which investment would reduce repeated risk.

| Program activity | A concrete artifact and owner | Agent opportunity and check |
| --- | --- | --- |
| Policy and quality management | Quality lead maintains versioned development and release procedures, approval authorities and records of change. | Find which controls and training reference a superseded procedure; owners approve updates. |
| Advice and training | Engineers practice finding a test that cannot cross a product limit. Support staff practice routing a candidate complaint. | Generate role-specific scenarios from verified incidents. Assess task performance and follow-up; attendance records only establish presence. |
| Model and supplier governance | Evaluation lead tracks model/data versions, known limits, vendor changes and performance across intended uses. Procurement records contractual commitments. | Diff release notices, map affected products and draft evidence requests. Specialist reviews material changes and model findings. |
| Documentation and customer support | Product maintains intended purpose, operating limits, oversight instructions and release-specific technical records. | Compare product documentation, customer-facing claims and tested behavior. Show conflicting passages with versions for review. |
| Oversight and assurance | Head of compliance reports exposures, resources and issues outside delegation. Internal audit can sample cases and challenge the monitoring program. | Prepare a permission-scoped evidence index and trace each reported count back to records. Preserve audit’s control over sample and opinion. |

**A management report worth reading.** “Three of 12 sampled releases lacked a fixture crossing their configured limit. Two have been retested; one remains open with the ranking team. The twelve were selected from 48 releases using targeted criteria. We cannot infer the defect rate in the other 36. We request two engineering days per squad for a shared boundary-test harness; QA will sample again next month.”

The first figure is a **risk indicator** (*kockázati mutató*): it helps direct attention. A **performance indicator** (*teljesítménymutató*) describes how the program runs, such as median days to accepted retest. Fast closure can coexist with weak testing. Pair cycle time with reopenings, overdue high-impact findings and verified coverage. The agent can calculate these against an explicit denominator; management decides what deserves investment.

## Design the platform around decisions and evidence

An **Agentic Compliance Platform** here means software that can use approved tools, follow a case through several steps, request missing inputs and resume when evidence arrives. Its user is the compliance analyst or officer; control owners supply evidence, designated reviewers sign conclusions, and the head of compliance or quality is a candidate buyer. Validate that buying arrangement with the actual customer.

| Trigger and input | Agent-assisted work | Deterministic work and human authority |
| --- | --- | --- |
| New PR or specification revision | Identify the changed product promise, cite old and new passages and propose affected controls. | Match repository, feature, version and tenant. Product confirms meaning; compliance decides materiality. |
| Evidence arrives | Identify the relevant claim and check whether the evidence packet addresses it. Draft the smallest missing request. | Validate source identity, permitted access, period, build and fixture. Reviewer handles scope ambiguity. |
| Retest finishes | Summarize deviations, propose linked findings and identify other releases possibly affected. | Compute missing, unexpected and duplicate IDs. QA attests to the run; Éva reviews the claim in scope. |
| Decision or exception comes due | Assemble options, limitations, dissent and outstanding evidence into a short memo. | Check authority, expiry and current version. Named human accepts, declines or escalates. |
| Complaint or rule change arrives | Retrieve related cases, summarize changed facts and propose reopening. | Preserve original receipt time and prior decision. Incident lead or legal reviewer determines the route. |

**Follow one event.** A recruiter specification in Drive says that unscored applications remain visible. A tenant-authorized GitHub webhook identifies a commit that adds a score filter. The agent cites the specification revision and the changed query. It requests a recruiter-role run including an unscored applicant. The two sources establish a discrepancy worth testing. QA supplies evidence of what the build actually does. Repeated delivery with the same event identity should update the existing task once. When QA replies three days later, the case resumes against that commit. If a subsequent commit superseded it, keep the old evidence and ask whether the change invalidates the test. The system should remember the unresolved question across the wait. A ticket marked “done” cannot substitute for the missing result.

**Access is part of evidence quality.** The agent can compare a selected Google Drive or Notion specification, an approved PR, a QA artifact and a Jira ticket using tenant-scoped permissions. Store source/version pointers, access labels and authorized excerpts. On revoked access, prevent new retrieval and apply the tenant’s retention policy to retained copies. Keep raw applicant records and restricted complaint details out of a broad engineering ticket. An inaccessible source is an explicit state. A reviewer needs to know that the platform could not inspect it.

## Choose a pilot and measure it honestly

**Pilot question.** Can a compliance analyst produce an acceptable release-evidence packet faster while reliably detecting gaps that could change a release decision? Start with one recruitment product, one approved repository, one policy, one QA system and synthetic records. The output is a draft packet and a recommended next action. Product leadership keeps release authority.

**Compare approaches.** The baseline analyst uses the existing ticket, PR diff and test results. The assisted analyst receives the same inputs plus citations, version checks and reconciled ID sets. Alternate the order across reviewers or use matched unseen cases. Include an ordinary low-risk edit as well as failures, approved exceptions, inaccessible evidence and superseded builds. Agree a reference result and severity with a practitioner before running the comparison. Label disputes and adjudicate them.

| Measure | How to calculate and interpret it |
| --- | --- |
| Material misses | Count reference cases needing a hold or evidence request that the tool clears. Report by severity, input completeness and failure type. |
| Useful routing | Count correct escalations among all escalations and detected material cases among all reference material cases. Track false alerts and their cost. |
| Citation correctness | Open each sampled citation with reviewer permissions. Confirm it resolves to the claimed version and supports the exact statement. |
| Unknown handling | Count unavailable-source cases correctly sent for evidence. A confident pass on incomplete input is an error. |
| Reviewer effort | Compare active minutes to an accepted packet, including corrections. Track elapsed waiting separately and record rework. |
| Decision integrity | Check for unauthorized approvals, duplicate tasks after retries and stale evidence accepted for new builds. Each failure deserves investigation. |

**Commercial interpretation.** Suppose median active preparation falls from 24 to 15 minutes over 20 comparable cases. The observed median difference is nine minutes. If the tool cleared even one build with missing IDs, inspect that failure before proposing broader use. Twenty synthetic cases reveal failure modes; real permissions, case mix, reviewer acceptance and purchasing authority still need evidence.

**Ask the buyer.** “Show me the last release packet you challenged. Which evidence changed the outcome? Who could grant a pilot access to those systems? What would you pay to improve: analyst preparation time, review delay, or defects discovered before rollout?” If evidence is already collected quickly but no one has time to retest, a collection assistant addresses the wrong bottleneck.

## Workshop: take the officer’s chair

Use the following independent exercise after reading the case. You are responsible for recommending whether **build D** may enable ranking for one pilot tenant. The director wants a response by 16:00. This internal deadline creates urgency. Your tenant boundary, testing criterion and decision authority stay the same.

| Packet item | Contents |
| --- | --- |
| P1. Approved requirement | Full queue must expose all eligible IDs to a recruiter, including unscored applicants. Withdrawn applications are excluded. |
| P2. Frozen manifest | Seven submitted IDs: A, B, C, D, E, F, G. F was withdrawn before cutoff. E has no score. All belong to the pilot vacancy. |
| P3. Recruiter run on build D | The complete traversal returns A, B, C, D, D, G. Role, tenant, commit and feature configuration match. |
| P4. Administrator screenshot | Admin can retrieve E directly in the database. Screenshot has today’s date. |
| P5. Fix and test | A merged PR restores E to the recruiter view. Attached passing test identifies build C. No new recruiter run on D or its successor is attached. |
| P6. Exception and support | Sales cites a signed exception for an internal demo using synthetic records only. Support separately reports one missing transferred applicant in a live customer; source history requested. |

**90-minute case lab.** Spend 15 minutes listing each record type and owner. Spend 20 deriving expected and observed sets and the decision for D. Use 20 to draft an evidence request of at most 80 words. Use 20 to draft a release memo of at most 120 words. Spend 15 explaining what you would do about the complaint and what your report to leadership may claim.

In the release memo, propose one FordoX risk decision: Accept, Remediate, Escalate or Block. Record the evidence for residual risk, the applicable tolerance or missing approval, the decision authority and the reassessment trigger. Explain separately what should happen to the live pilot. [FordoX taxonomy](../../taxonomy.md)

**45-minute design lab.** Pick a trigger. Write the platform’s exact inputs, two permitted tool actions, its durable case state, the stopping condition and the human decision. Predict its behavior if the evidence is delivered twice or source access is revoked. Name one acceptance test for each. State the current manual baseline you would measure and who can authoritatively label a material miss.

**45-minute practitioner interview.** Walk through a recent release using an approved redacted example. Identify the person who could order a change, who actually challenged the evidence, and whose sign-off closed the finding. Ask for one decision that could be automated and one that still needed a person. Record observed facts separately from assumptions, including why a buyer might decline the proposed pilot.

## Answer key and a reusable decision record

**Reconciliation.** Expected eligible set = A, B, C, D, E, G. The six rows in P3 contain five distinct IDs, A, B, C, D, G. E is missing; D is duplicated; no unexpected ID is present. The complete matching run establishes failure on build D. P4 establishes that E exists in storage. The approved claim concerns recruiter access. The test for build C and the merged fix leave the corrected candidate’s behavior unresolved.

**Build D risk decision.** Recommend **Remediate** to the accountable risk owner. The approved pilot criterion permits zero missing eligible IDs. E is missing, and D appears twice. This run establishes a visibility control failure on build D. It supplies neither subgroup outcomes nor the frequency of harm across vacancies. Leave the residual rating unresolved and request the approved risk tolerance if a numerical or categorical comparison is required. The zero-omission test criterion alone cannot supply that rating.

Engineering repairs the query. QA reruns the full traversal on the corrected candidate with the scoped recruiter role. The compliance reviewer can close the finding when that evidence satisfies the criterion. The risk owner reassesses remaining exposure, records the relevant tolerance and decision, and escalates anything outside delegated authority. The release director keeps live ranking on hold pending that review and makes a separate rollout decision. Record the build, accountable person, date, rationale and next review point. Reopen on a changed eligibility rule, queue configuration or new affected applicant path.

**A suitable evidence request.** “QA: on the candidate containing the merged fix, run the full queue as an ordinary pilot recruiter against the frozen manifest. Attach commit, tenant, flag, role, all returned IDs, pagination completion and comparison with the six eligible IDs. Include E with no score. Record any duplicate separately. If the run cannot finish, identify the missing evidence.”

**A suitable memo.** “Hold live ranking for the pilot. On build D, six rows contained five distinct eligible IDs. E was missing and D appeared twice. Admin access and a passing test on C do not verify recruiter behavior on the corrected build. The existing exception covers a synthetic demo only. Engineering owns the change; QA owns retest. I will review the new run, then the director can decide rollout within the approved scope. Support is investigating a separate live transfer issue; customer exposure is unknown.”

**Complaint disposition.** Open or link a restricted incident-assessment case. Preserve receipt time, route for timely containment and impact assessment, ask for the source and destination history using authorized access, and involve the employer for candidate follow-up where warranted. A product defect and a possible live impact can coexist with different evidence states. The fact pattern alone cannot settle the legal reporting decision.

**Platform answer.** On new test completion, retrieve the approved manifest and candidate run. Use tenant/build/role checks and set comparison; attach one analysis per unique run. Duplicate notification reuses the analysis. If access is revoked before collection, stop retrieval and mark the evidence unavailable. A source-permission failure must never become a passing result. Authorized humans decide finding closure and launch.

**Reusable record.** Capture question → governing criterion/source/version → entity/product/build → expected and observed behavior → evidence and limits → affected people → recommendation and alternatives → authority and decision → owner/due date → retest and reopening trigger. A peer should be able to reconstruct the conclusion and name one new fact that would change it.

## English–Hungarian desk glossary

These are working translations for conversations with practitioners. Use the official legal wording when drafting a legal interpretation.

| Term | Magyarul | How to recognize it |
| --- | --- | --- |
| Compliance officer / function | megfelelőségi szakértő / megfelelőségi terület | Person / organizational function that advises, monitors, challenges and escalates. |
| Governance / accountability | vállalatirányítás / elszámoltathatóság | Who has authority, and who must explain the outcome? |
| Risk owner / control owner | kockázatgazda / kontrollgazda | Who can change the exposure? Who ensures a specific safeguard operates? |
| Delegation / escalation | hatáskör átruházása / döntés magasabb szintre emelése | Who may decide today? Who handles matters beyond that mandate? |
| Applicability / obligation register | alkalmazandóság / kötelezettségnyilvántartás | Why a provision reaches this activity; where the dated interpretation lives. |
| Provider / deployer | szolgáltató / alkalmazó | DunaWorks supplies the branded system; the employer uses it to recruit. |
| Intended purpose / foreseeable misuse | rendeltetés / észszerűen előrelátható rendellenes használat | Expected recruiting workflow and a credible way it may be misused. |
| Preventive / detective control | megelőző / feltáró kontroll | Design keeps all eligible applicants reachable; reconciliation detects omissions. |
| Evidence provenance / scope | a bizonyíték eredete / vizsgálati kör | Source, version, period, population, permissions and collection method. |
| Finding / evidence gap | megállapítás / hiányzó bizonyíték | Demonstrated deviation versus an unanswered question. |
| Root cause / corrective action | kiváltó ok / helyesbítő intézkedés | Why a defect escaped, and what reduces repetition. |
| Exception / risk acceptance | jóváhagyott eltérés / kockázatvállalás | Authorized departure from an internal rule / decision about remaining exposure. |
| Monitoring / independent assurance | folyamatos nyomon követés / független bizonyosságot nyújtó értékelés | Routine management review / independent assessment of a defined claim. |
| Post-market monitoring | forgalomba hozatal utáni nyomon követés | Systematic learning from performance and events after release to customers. |

**Pass condition.** Explain in either language how one shortlist change produces a signal, case, risk, control test, finding, corrective action, verified closure and a separate release decision. For each, identify its owner, its evidence, what an agent could do, and what would make the agent stop.

## Original readings and where to look

**1. Roles and independence · 10 minutes.** Institute of Internal Auditors, *The IIA’s Three Lines Model*, July 2020, updated September 2024. Read the role descriptions for the governing body, first- and second-line management, and internal audit. Identify the person who operates a control and the person who can independently assess its operation. [IIA position paper](https://www.theiia.org/globalassets/documents/resources/the-iias-three-lines-model-an-update-of-the-three-lines-of-defense-july-2020/three-lines-model-updated-english.pdf)

**2. AI provider scope and timing · 12 minutes.** European Parliament and Council, Regulation (EU) 2024/1689, consolidated text dated 27 July 2026. Read Article 3 on roles and intended purpose, Article 6 and Annex III point 4(a) on classification, and Articles 111 and 113 on transition and application. The Commission timeline was checked on 17 November 2026. Use current official sources for a new product decision. [Consolidated text](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?qid=1789944163546&uri=CELEX%3A02024R1689-20260727) · [Application timeline](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)

**3. Provider work and records · 10 minutes.** In the same regulation, trace one requirement from risk management through quality management, testing and technical documentation. Articles 9–15 address requirements for high-risk systems. Articles 16–17 concern provider obligations and quality management. Article 43 addresses conformity assessment. Review the conditions and applicable procedure for the particular system. [Article 9](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-9) · [Article 16](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-16) · [Article 17](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-17)

**4. After release · 8 minutes.** Compare Article 72 on collecting and analyzing evidence over a system’s life with Article 73 on serious incidents. Write down the additional facts required to move from a customer complaint to a reporting decision. [Article 72](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-72) · [Article 73](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-73)

**5. Operating vocabulary · 5 minutes.** US National Institute of Standards and Technology, *AI Risk Management Framework Playbook* accompanying AI RMF 1.0 (2023), live resource reviewed 17 November 2026. Govern, Map, Measure and Manage offer a voluntary vocabulary for organizing work. Map one DunaWorks task to each and name the person who can act on the result. [NIST Playbook](https://airc.nist.gov/airmf-resources/playbook/)
