# Week 4 · Can this supplier run our support desk?

The support director wants to move DunaWorks' service desk to a cloud supplier called HídDesk. An engineer asks where the database runs. Privacy counsel asks whether HídDesk will reuse ticket text to train a model. The AI incident lead asks how engineers will find reports of missing applicants if the supplier disappears on Monday morning. All three are reviewing the same purchase. Each needs different evidence.

DunaWorks and HídDesk are fictional. DunaWorks is a Hungarian developer of AI recruiting software with German and US operations. Start with its German product support team and recruiters reporting ranking errors. The exercise supplies its own deadlines and recovery targets. The source notes identify the EU rules and guidance used for the legal concepts.

> Magyarul: Három külön kérdésünk van. Mire használhatja a szolgáltató az ügyfél adatait? Ki férhet hozzájuk? Hogyan folytatjuk a munkát, ha leáll a rendszer?

**Five hours.** Use 50 minutes for the chapter, 70 for the source readings, two hours for the supplier assessment and one hour for a practitioner walkthrough and notes. Your deliverable is a decision record that privacy, security and service operations can each challenge.

### Chapter map

- [Draw the data flow before sending a questionnaire](#draw-the-data-flow-before-sending-a-questionnaire)
- [Follow one person's request through the system](#follow-one-persons-request-through-the-system)
- [Security and resilience use different clocks](#security-and-resilience-use-different-clocks)
- [Two incidents on the same Tuesday](#two-incidents-on-the-same-tuesday)
- [Workshop: decide whether to allow real tickets](#workshop-decide-whether-to-allow-real-tickets)
- [Worked review and founder conversation](#worked-review-and-founder-conversation)
- [Vocabulary and original readings](#vocabulary-and-original-readings)

## Draw the data flow before sending a questionnaire

**Personal data** is information relating to an identified or identifiable person. A business email identifying Anna, a recruiter, can qualify. A ticket identifier can become personal data when a service log links it to Anna. The **purpose** explains why information is used. Investigating a missing shortlist entry and improving a vendor's general model are two distinct purposes even if the input is the same ticket.

| Movement in the fictional service | Data and purpose | Question for the decision |
| --- | --- | --- |
| Customer contact to German service desk | Name, work email, model version, description of the ranking error | Can the form discourage unrelated personal details? |
| Service desk to HídDesk EU tenant | Agent assignment and ticket history for coordination | Which entity decides why and how records are processed? |
| HídDesk to mail supplier | Recipient and message for status updates | Which fields reach the mail provider, and where is support access possible? |
| Ticket store to backup | Recovery copy of tickets, including deleted live records until expiry | What is the retention schedule? What happens on restore? |
| Optional vendor training feed | Full ticket text proposed for general product improvement | Who decides this purpose, on what basis, and can the feed stay disabled? |

Under the EU General Data Protection Regulation (GDPR), a **controller** (*adatkezelő*) determines, alone or jointly with others, why and how personal data are processed. A **processor** (*adatfeldolgozó*) processes personal data on the controller’s behalf. A **subprocessor** is another processor engaged by a processor. Assign roles for an activity. In the support-contact example, assume DunaWorks directs support and HídDesk acts on its documented instructions. If HídDesk chooses its own training purpose, reopen the role and legal analysis before enabling the feature. A contract label cannot settle the facts.

A **lawful basis** is the justification under the GDPR for a particular processing operation. Identify whose data is involved and why DunaWorks needs it. A contract with Anna's employer does not automatically establish contractual necessity for Anna personally. Privacy counsel records the assessment, any required balancing and information for the person. An EU hosting address also leaves open who can access the data, from where, and under what arrangements.

## Follow one person's request through the system

Anna asks for access to her data and correction of a note giving the wrong contact details. The **data subject** (*érintett*) is the person the data concerns. The request reaches the general support mailbox. A trained agent records receipt, routes it promptly and checks identity proportionately. A privacy owner determines the applicable right, timing and scope, searches relevant systems and coordinates a response. A customer-facing employee should know where to route a request even if the person never uses the term GDPR. See the EDPB readings on basics and individuals' rights.

A **record of processing activities (RoPA)** describes processing across activities. For the AI product support desk, record purpose, people and data categories, recipients, retention, transfers where relevant and security information as appropriate to the role. It helps find the right systems. It will not by itself retrieve Anna's note. For the actual request, link search results, redactions needed to protect others, corrections, recipient follow-up where relevant and the approved response.

**Retention** means deciding how long to keep information for its purpose and how to implement expiry. Ask what happens in the active store, search index, exports and backup. Imagine a record deleted on Tuesday reappears when Monday's backup is restored. Engineering needs a way to reapply the deletion or restriction before normal access resumes. Privacy needs evidence that the procedure works.

A **data protection impact assessment (DPIA)** examines a proposed processing operation, why the processing is necessary for its purpose, whether its extent is proportionate, the risks to individuals’ rights and freedoms, and the safeguards for those risks. For example, could the support team diagnose ranking errors with a ticket ID instead of a full applicant file? GDPR Article 35 requires one when processing is likely to result in high risk to people's rights and freedoms. The deployment team screens the actual use, records its rationale and seeks specialist input where needed. A supplier questionnaire describes a vendor. A DPIA analyzes what this controller proposes to do to or with people's data.

## Security and resilience use different clocks

**Information security** protects confidentiality, integrity and availability. Examples include preventing access by the wrong support agent, detecting unauthorized edits and keeping ranking incident tickets accessible. The NIST Cybersecurity Framework 2.0 gives six useful verbs. Govern assigns decision rights. Identify maps systems and dependencies. Protect limits access. Detect catches unusual exports. Respond coordinates investigation and containment. Recover restores the service and checks that the data can be trusted. Use these as organizing questions, not as a score awarded by counting tools.

**Operational resilience** asks whether people can keep an important service running through disruption and recover it. Begin with the triage of ranking incidents. It depends on identity, ticket storage, email, trained staff and a model engineer on call. Two independent ticket databases behind the same unavailable identity provider still leave incident reviewers locked out.

A **recovery time objective (RTO)** is a target for restoring an activity or service after disruption. A **recovery point objective (RPO)** describes tolerable data loss measured in time. DunaWorks sets an illustrative RTO of four hours and an RPO of 30 minutes for triage. A restore that takes three hours from a backup two hours old can meet the time objective while missing the data objective. Check whether the measured interval includes locating the backup, restoring access and reconciling incoming incident reports.

A supplier's ISO/IEC 27001 certificate concerns an information security management system in a stated scope. A SOC 2 Type 2 report describes a specific system, criteria, test period and results. Look for service boundaries, excluded dependencies, exceptions and controls the customer must operate. Ask for an actual restore test with timestamps. Neither the certificate date nor a promise of daily backup answers the 30-minute recovery-point question.

## Two incidents on the same Tuesday

**Scenario A, service outage.** At 08:10 the ticket interface stops loading. Incident triage has a read-only offline list from 08:00. The incident lead opens a timeline, assigns an owner, switches triage to the fallback and logs new jobs for reconciliation. At 10:40 the service is restored from 08:00. Staff reconcile subsequent jobs and at 11:00 confirm normal triage. For this exercise the service recovered within 2 hours 50 minutes and its restored data point was 10 minutes before disruption. Record the fallback's blind spots too. Privacy checks whether personal data was lost, corrupted, disclosed or rendered unavailable in circumstances amounting to a personal data breach.

GDPR Article 4(12) treats a security compromise as a **personal data breach** when it results in accidental or unlawful destruction, loss or alteration of personal data, or unauthorized disclosure of or access to those data. This includes data in transit, in storage or otherwise processed. [GDPR, Article 4](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)

**Scenario B, unauthorized disclosure.** At 08:10 a supplier analyst reports that another customer downloaded an export containing names and ranking incident notes. The service is still running. Contain further access, preserve logs and involve security and privacy promptly. Establish whose data was exposed, sensitivity, recipients, whether copies remain and likely effects on people. Record when the processor and controller each became aware, who took which action and why. A working website gives little comfort to the people whose notes were disclosed.

Under GDPR Articles 33 and 34, a processor informs its controller without undue delay after becoming aware of a personal data breach. The controller documents breaches and assesses the risk. It notifies the competent supervisory authority without undue delay and, where feasible, within 72 hours of awareness unless risk to individuals' rights and freedoms is unlikely. High risk generally also requires communication to affected people without undue delay, subject to the Article 34 exceptions. Record the rationale and any reasons for late notification. Contractual, sectoral and customer duties can have different triggers. [EDPB breach guidance](https://www.edpb.europa.eu/sme/assess-the-risks/data-breaches_en)

**Sector lens.** The EU NIS2 Directive addresses cybersecurity in covered sectors. Check the activity, size rules and exceptions, entity, jurisdiction and national implementation. The Digital Operational Resilience Act (DORA) addresses digital resilience in the financial sector, including management of technology suppliers and an oversight framework for critical providers. A financial customer may impose contract terms on DunaWorks. Record separately the customer's duty, DunaWorks' contractual promise and any direct duty applicable to DunaWorks itself.

## Workshop: decide whether to allow real tickets

You have a 30-day pilot request. The sponsor wants live tickets immediately. The supplier sent the following synthetic packet. No additional facts are implied. Divide the two hours into 20 minutes for the data map, 35 for questions and evidence, 30 for the two incident routes, and 35 for the decision and peer challenge.

| Item | Evidence supplied |
| --- | --- |
| P1 / proposed contract | EU hosting commitment for live tickets. Mail subprocessor unnamed. General training option defaults to on. |
| P2 / ISO certificate | Valid and names HídDesk's hosting operation. The service desk support entity is outside its stated scope. |
| P3 / access procedure | Vendor says support staff must use approved temporary access. No completed access record in packet. |
| P4 / recovery test | Restore took three hours. Restored backup was two hours old. Customer-side triage and reconciliation were excluded. |
| P5 / tenant settings | Screenshot shows live retention of 180 days. No backup expiry or post-restore deletion procedure supplied. |

1. Draw the five flows and mark which people and systems can see ticket text. List facts the packet supports and three facts a reviewer must still obtain.
2. For each of privacy, security and continuity, draft one precise request, name an owner and explain the decision the answer could change.
3. Decide among synthetic-only pilot, live pilot with conditions and hold. State what is authorized today, which uses are excluded and who can authorize progression. Draft an expiry date and a trigger for reopening.
4. Write the first three actions for each Tuesday incident. Which teams would act in both? Which notification decision needs privacy expertise?

**Reusable decision record.** Record service, purpose, processing roles, data flows, access locations, evidence IDs and limitations, risk to people, service dependency, mitigations, reviewer, decision, conditions, expiry and re-review trigger. Keep factual observations distinguishable from your assessment.

## Worked review and founder conversation

**Decision.** Authorize a 30-day synthetic-ticket pilot in a separate tenant, subject to disabling training and using invented contacts. No production connector is authorized. The service owner records expiry. Reopen on a proposed live import, service change or new subprocessor. The sponsor does not have authority under the exercise's internal rules to accept all three types of risk.

**Privacy.** The privacy lead requests the mail supplier's identity, processing terms, access locations, training setting, backup expiry and rights-request support. Require a copy of applicable processor terms and a settings record for the intended tenant. A screenshot of the 180-day setting supports a claim about the live store only. Test correction and deletion using a synthetic contact; observe what reappears after restore.

**Security.** The security reviewer asks for a redacted completed support-access record showing request, approver, duration, scope and revocation. P2 can support the hosting review, but the support team's practices still need evidence. P3 is a procedure. Until there is an execution sample, the reviewer cannot conclude that temporary access expired as required.

**Continuity.** The three-hour technical restore leaves at most one hour under the illustrative four-hour service target for all remaining work. Whether triage can recover within four hours is unknown because staff did not participate. The measured two-hour rollback misses the 30-minute data objective. Require a timed end-to-end drill, evidence of the recovered point and reconciliation of intervening jobs. Name operations as owner and service management as witness.

**Incident answer.** For A, log and assess, start offline triage, then restore and reconcile. For B, stop further exposure, establish facts and awareness times, then have the controller assess notifications and document its reasoning. Security and operations may assist both. A single event may activate both paths.

**Ask a practitioner** to show the last supplier review that waited on another team. Which answer unlocked the decision? Who can accept residual risk? A possible pilot would let a third-party risk analyst extract cited supplier claims and send *one* targeted follow-up per unresolved decision. The head of procurement risk might fund it. Test on approved redacted packets. Measure days waiting, accepted evidence, material gaps missed and time per accepted review.

## Vocabulary and original readings

| English term | Plain meaning | Magyarul |
| --- | --- | --- |
| Controller / processor | Determines the purposes and means of the activity alone or jointly / processes personal data on that controller’s behalf | adatkezelő / adatfeldolgozó |
| Personal data breach | Security compromise resulting in destruction, loss, alteration, unauthorized disclosure or unauthorized access to personal data | adatvédelmi incidens |
| Data subject | Person the data relates to | érintett |
| Lawful basis | Legal justification for specified processing | adatkezelési jogalap |
| DPIA | Examines necessity, proportionality, risks to rights and freedoms, and safeguards for the proposed processing | adatvédelmi hatásvizsgálat |
| Operational resilience | Ability to sustain and restore important services | működési ellenálló képesség |
| RTO / RPO | Target restoration time / tolerable rollback in time | helyreállítási célidő / adatvesztési tűréshatár időben kifejezve |

- **European Data Protection Board**, Data protection guide for small business, live guide reviewed 17 November 2026. Spend 30 minutes on roles, rights and breach response. The legal references are to Regulation (EU) 2016/679, especially Articles 4–6, 12–22, 28, 30 and 32–35. [Basics](https://www.edpb.europa.eu/sme/learn-the-basics/data-protection-basics_en) · [Individuals' rights](https://www.edpb.europa.eu/sme/be-compliant/respect-individuals-rights_en) · [Breach response](https://www.edpb.europa.eu/sme/assess-the-risks/data-breaches_en)
- **US National Institute of Standards and Technology**, SP 1300, NIST Cybersecurity Framework 2.0: Small Business Quick-Start Guide, February 2024. Spend 20 minutes following one service through the six functions. US voluntary guidance. [Quick-start guide](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.1300.pdf)
- **European Commission**, NIS2 and financial cyber resilience overviews, reviewed 17 November 2026. Spend 20 minutes identifying affected entities and supplier relationships. Refer to Directive (EU) 2022/2555, its national implementation, and Regulation (EU) 2022/2554 when assessing actual customers. [NIS2](https://digital-strategy.ec.europa.eu/en/policies/nis2-directive) · [DORA](https://finance.ec.europa.eu/digital-finance/cyber-resilience_en)

**Pass condition.** Explain how a supplier could preserve confidentiality and still fail the triage recovery objective. Identify the evidence that would allow each reviewer to change their decision.
