# Week 2 · How do you know a control worked?

At DunaWorks, the head of IT opens an audit meeting with a green dashboard. “Every departure ticket closed in October.” The auditor asks to see who left. IT hands over its list of closed tickets. What would happen to someone who never got a ticket?

DunaWorks is the fictional equipment and software group from Week 1, headquartered in Hungary with operations in Germany and the US. This week you will build a test whose starting point is independent of the process being tested. You will leave with a five-row risk-and-control matrix, a set of reproducible results and a finding someone can actually close.

> Magyarul: A lezárt hibajegy azt bizonyítja, hogy valaki lezárta a jegyet. Azt, hogy minden kilépő minden hozzáférését időben megszüntették, más adatokkal is igazolni kell.

**Five hours.** Spend 50 minutes on the chapter and 70 on the original readings. Use 120 minutes for the matrix and departure test. Reserve 60 minutes for an interview and notes. All records, policies and times in the cases are fictional.

### Chapter map

- [Start with the risk and write a testable control](#start-with-the-risk-and-write-a-testable-control)
- [What counts as evidence?](#what-counts-as-evidence)
- [Build a five-row risk-and-control matrix](#build-a-five-row-risk-and-control-matrix)
- [Lab: test the October departures](#lab-test-the-october-departures)
- [Answer key: from one late account to verified closure](#answer-key-from-one-late-account-to-verified-closure)
- [What an assurance report buys the reader](#what-an-assurance-report-buys-the-reader)
- [Vocabulary and original readings](#vocabulary-and-original-readings)

## Start with the risk and write a testable control

A **risk** is a possible event and its consequence. “Access management” names a topic. “A former engineer can still export customer records after leaving” identifies who, what and why it matters. **Inherent risk** means the exposure before considering safeguards. **Residual risk** is what remains with the safeguards in place. Even after accounts are disabled, a previously downloaded customer file can remain on a laptop. Estimating residual risk requires understanding this boundary.

A **control** is an action that helps achieve an objective. Write down the actor, trigger, action, scope and record. DunaWorks policy L-4 requires the identity team to disable every departing employee's accounts in Payroll, Cloud and CRM (customer relationship management) within 24 elapsed hours of effective departure. A pre-authorized, system-specific extension can change a deadline under this fictional policy. The owner reconciles HR departures to system logs monthly. Disabling accounts limits access. The reconciliation detects omissions. They serve different purposes.

A **preventive control** can stop an unwanted action, such as blocking a payment until a second person approves it. A **detective control** finds a problem after it occurs, such as reconciling yesterday's payments. Either can be manual or automated. **Segregation of duties** means dividing incompatible powers. If one clerk can change a supplier's bank account and release the payment, a second approval screen under that clerk's own login accomplishes little.

**Design effectiveness** asks whether the procedure, performed as written, could achieve its objective. Try walking one event through it. An overnight job that runs only on weekdays cannot reliably meet a 24-hour deadline over a weekend. **Operating effectiveness** asks whether a suitably designed control actually operated as required in the period. A daily job can be well designed and still miss Saturday after its credential expires.

## What counts as evidence?

Imagine four records on an auditor's desk. The policy defines the deadline. A job log records an attempted operation. The destination system's event records an account disablement. A tester's signed worksheet explains how the event was matched and whether it met the deadline. Each answers a different question. An automated system can generate thousands of records of attempts without showing which changes took effect.

| Record | Question the reviewer can answer | Additional check |
| --- | --- | --- |
| Control definition L-4 v3 | What was supposed to happen? | Confirm this version governed October. |
| HR departure export | Which employees should appear? | Reconcile to HR's monthly totals across all three entities. |
| Destination audit event | What happened to this account, and when? | Check stable account ID, time zone, event semantics and export window. |
| Exception approval | Was a different deadline authorized? | Match person, system, dates and approver authority. |
| Test worksheet | How did the evaluator reach the result? | Follow the inputs and independently reproduce one row. |

**Population** means the full set of events covered by a claim. Start from HR, expand each departure to the three required systems, then look up evidence for every expected pair. Starting from system logs silently drops people with no matching event. Ask whether temporary staff, transfers and shared accounts belong in scope. An answer may require a second population and a separate control.

**Provenance** is where a record came from and how it reached the test. Retain the query or export criteria, collection time, period, system owner and access restrictions. A screenshot of a disabled account today cannot establish the date it was disabled. A late-collected event history might still establish that date. The collection date and the event date do different jobs.

## Build a five-row risk-and-control matrix

A **risk-and-control matrix** links a failure scenario to the action intended to address it and the procedure that checks it. One row per control is a useful starting point. Split a row when owners or triggers differ. Use the following worked matrix as a model. The identifiers refer to invented company policies.

| Policy and risk | Control, owner and trigger | Evidence and test | Example finding and response |
| --- | --- | --- | --- |
| P-2. An unauthorized invoice is paid | Finance requires a second authorized approver before each release | Match bank releases to approval IDs, roles and times | One release preceded approval. Finance blocks release and retests the next batch. |
| L-4. A leaver retains access | Identity team disables three accounts within 24 hours of departure | Join HR population to effective disablement events | CRM is late. Identity lead fixes the queue and reruns the test. |
| V-3. An unreviewed distributor trades | Procurement requires clearance before activating each distributor | Compare activation time with signed review and conditions | Activation predates review. Procurement checks open orders and retests the gate. |
| A-1. Unneeded administrator rights persist | System owner reviews all privileged grants quarterly | Reconcile full grant export to review decisions and removals | Emergency admins omitted. Owner expands export and repeats review. |
| E-2. A manager approves personal expenses | Finance routes each claim to a different authorized approver | Compare claimant, approver and delegation records | Self-approval under delegation. Finance changes routing and tests a delegated claim. |

**Try it.** Cover the last two columns and rewrite the test for each row. For the expense row, why might checking that two *usernames* differ be inadequate? One person may hold two accounts. A robust test checks who controlled each identity at approval time. For each finding, name a due date, an owner and a reviewer who can verify the correction.

COSO's internal-control framework places these activities alongside four other components. Management sets expectations and authority (**control environment**), identifies exposure (**risk assessment**), moves usable information to the right people (**information and communication**) and checks whether arrangements still work (**monitoring**). A perfect routing rule can become irrelevant if management routinely pays urgent invoices outside the system. See the COSO and SEC readings.

## Lab: test the October departures

HR confirms these five IDs are the complete October employee departure population for the exercise. All five had an account in each named system. Each departure took effect at **09:00 UTC on 12 October**. Exports cover the relevant days after departure. Cells show elapsed hours from departure to the destination's disable event. An approved extension X7 covers only E04's Cloud account through hour 48. Its approver had authority and signed before departure.

| HR ID | Payroll | Cloud | CRM |
| --- | --- | --- | --- |
| E01 | 1 | 3 | 4 |
| E02 | 2 | 6 | 26 |
| E03 | 1 | No event in extract | 2 |
| E04 | 3 | 36, approval X7 | 3 |
| E05 | 2 | 4 | 3, event tagged E50 |

Use one result per expected person-system pair. Classify as **pass**, **failure**, **approved exception** or **insufficient evidence**. If an identity is ambiguous, keep the expected pair in the worksheet. The clock runs through weekends and the boundary is inclusive. Record the default deadline, any authorized deadline and the evidence reference separately.

1. Build the expected population. What is the denominator, and which join would accidentally shrink it?
2. Reconstruct the ordinary deadline as a timestamp. Write one result for each unusual cell. Identify precisely what would resolve the unknowns.
3. Write a two-sentence report a manager can use. Include the scope and the unresolved cases. Resist converting missing evidence into a success or a proven policy breach.
4. Draft a finding for the observed late case. Suppose the queue is fixed tomorrow. What evidence would let an independent reviewer close it?

**Time box.** Allocate 40 minutes to the matrix, 45 to the test, 20 to the finding and 15 to peer review. Trade worksheets. If someone cannot reproduce the denominator or the late result, identify the missing instruction.

## Answer key: from one late account to verified closure

Five people times three systems gives **15 expected pairs**. An inner join to available events would drop E03's Cloud record. A join on an unverified name could quietly substitute E50 for E05. The ordinary deadline is 13 October at 09:00 UTC. Exactly hour 24 would pass.

| Pair | Result | Reason or next request |
| --- | --- | --- |
| E02 / CRM | Failure | Hour 26 is two hours late. No applicable extension exists. |
| E03 / Cloud | Insufficient evidence | Ask for authoritative account history and extract completeness. Access may have persisted or the export may be incomplete. |
| E04 / Cloud | Approved exception | X7 names the person and system. Hour 36 meets the authorized 48-hour limit. |
| E05 / CRM | Insufficient evidence | Obtain the historical identity mapping or corrected log. E50's event alone proves nothing about E05. |
| Remaining eleven | Pass | All match an in-scope ID and meet the ordinary deadline. |

**Manager's report.** “Of 15 expected October disablements, eleven met the ordinary deadline and one met an authorized extension. CRM was late for E02, and two pairs need additional evidence.” If a dashboard reports a rate, define which statuses are in its numerator and denominator. A result of eleven ordinary passes out of fifteen is reproducible. Calling every other case a failure changes its meaning.

**Finding F-17.** The reviewer records the policy version, matched event and two-hour overrun. The identity lead checks whether E02 used CRM during the exposure and whether others were affected. The reviewer distinguishes possible exposure from demonstrated access. Suppose queue history establishes that a manual retry was required after a timeout. The owner adds retry monitoring, provides the deployment record by 5 November and tests a deliberately delayed job. On 12 November the reviewer rechecks subsequent departures and confirms the alert reached the on-call person. These are example assignments and dates.

Closing the engineering ticket proves a change was delivered. The retest establishes what the change accomplished. If monitoring still overlooks a system, reopen the finding or explicitly record the residual issue and its authorized owner.

## What an assurance report buys the reader

A buyer asks DunaWorks for “the audit.” First find out which claim the buyer needs assessed. Internal control over financial reporting concerns the reliability of financial statements. An access control may support that objective for the accounting system. The same procedure on a public demo environment answers a different question. The SEC guide illustrates financial-reporting controls in a historical US public-company context.

**System and Organization Controls (SOC)** is the AICPA's family of assurance services. SOC 1 addresses controls relevant to user entities' financial reporting. A SOC 2 examination addresses controls relevant to selected trust services criteria for a described system. In a Type 1 report, look for the specified date and the design assessment. In Type 2, also look for the period, the auditor's tests and results, and the opinion on operating effectiveness. Read the boundaries, exceptions and controls the customer is expected to perform.

**ISO/IEC 27001:2022** specifies requirements for an information security management system. Certification concerns the management system within its stated scope. A supplier certificate might cover its Frankfurt hosting operation while your proposed support desk sits in another entity. Read the scope statement, issuer and validity dates. Ask how the actual service fits. A certification and a SOC report provide different evidence to the same purchasing decision.

**Interview and founder exercise.** Ask a control owner to show the last evidence request an auditor returned. What was the stated criterion? Which file did they send? What did the reviewer reject, and what ultimately satisfied them? A pilot could help a security assurance analyst reconcile a monthly HR export to three approved system exports. The analyst resolves identities, the control owner remedies failures and the assurance reviewer accepts the test record. A possible buyer is the head of assurance. Measure minutes per reviewed test and known gaps missed. Data access and willingness to rely on the output are open questions.

## Vocabulary and original readings

| English term | Plain meaning | Magyarul |
| --- | --- | --- |
| Inherent / residual risk | Exposure before safeguards / exposure that remains | eredendő / fennmaradó kockázat |
| Control owner | Person accountable for an operating control | a kontrollért felelős személy |
| Segregation of duties | Split powers that one person could misuse together | összeférhetetlen feladatok szétválasztása |
| Population | Everything the test claims to cover | a vizsgálat teljes alapsokasága |
| Evidence / finding | Record supporting a judgment / documented weakness | bizonyíték / vizsgálati megállapítás |
| Operating effectiveness | Whether the control worked as required in practice | a kontroll működési eredményessége |
| Retest | Check whether the correction works | javítás utáni ismételt ellenőrzés |

**Reading route.** Use 20 minutes for COSO and the SEC, 30 for the AICPA materials and 20 for ISO and your scope notes. The public overviews are sufficient for this exercise.

- **COSO**, Internal Control—Integrated Framework, 2013 update. Read the framework overview and identify the five components in one finance process. [Official overview](https://www.coso.org/guidance-on-ic)
- **US Securities and Exchange Commission**, Sarbanes-Oxley Section 404, A Guide for Small Business, 2007 reporting context. Read “What Constitutes Effective Internal Controls?” for management's role. [Historical guide](https://www.sec.gov/files/info/smallbus/404guide/controls.shtml)
- **American Institute of Certified Public Accountants (AICPA)**, SOC Suite of Services, live overview reviewed 17 November 2026. Compare the objects of SOC 1 and SOC 2. For report dates and periods see the 2022 SOC 2 guide, paragraph 2.05. [SOC overview](https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services) · [Guide excerpt](https://assets.ctfassets.net/rb9cdnjh59cm/2paxzm46AxmwDDSZGkdtFS/c01813c67d26de154898653c121a92ea/AAGSOP22E.pdf)
- **ISO and IEC**, ISO/IEC 27001:2022, third edition. Read the public abstract on the scope of an information security management system. [Standard overview](https://www.iso.org/standard/27001)

**Pass condition.** Hand the worksheet to a second person. Can they reconstruct all 15 results, explain why the two unknowns remain open and describe what would close F-17?
