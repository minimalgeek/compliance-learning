# Week 6 · Which compliance workflow is worth building?

An AI compliance reviewer at DunaWorks reads the same product specification twice. The first version promises that recruiters can review unscored applicants. The revision says “hide applications without a score.” Engineering sees a small wording change. The reviewer sees a decision that may need reopening. Who notices today, how much work follows, and who would pay to improve it?

DunaWorks is a fictional developer of AI recruitment software. This chapter turns a plausible incident into a testable product hypothesis. All customer statements, volumes, scores, prices and evaluation results in the examples are invented. Replace them with evidence from interviews and an authorized pilot.

> Magyarul: A „jó ötlet” és a fizetős próba között az a kérdés, hogy ki milyen döntést hoz ma, mi kerül neki időbe, és milyen mérhető eredményért fizetne.

**Your five hours.** Spend 60 minutes mapping existing products, 90 on three short interviews, 30 comparing opportunities, and 120 building and testing a thin prototype. Read the relevant section as part of each block. Finish with a one-page opportunity memo that a buyer and reviewer could challenge.

### Chapter map

- [Look at the tools already in the room](#look-at-the-tools-already-in-the-room)
- [Interview for a recent decision](#interview-for-a-recent-decision)
- [Choose one decision and expose the assumptions](#choose-one-decision-and-expose-the-assumptions)
- [Build a prototype a reviewer can reject](#build-a-prototype-a-reviewer-can-reject)
- [Evaluate misses, reviewer work and uncertain cases](#evaluate-misses-reviewer-work-and-uncertain-cases)
- [Write the one-page opportunity memo](#write-the-one-page-opportunity-memo)
- [Vocabulary and product readings](#vocabulary-and-product-readings)

## Look at the tools already in the room

DunaWorks may already pay for a governance, risk and compliance (GRC) platform, a ticketing system and a cloud document suite. The analyst may still keep a spreadsheet because it records why a particular change was closed. Examine the spreadsheet and handoffs as seriously as the software contract. Replacing ten minutes of copying achieves little if the reviewer then waits four days for an engineer.

The following are workflow examples to investigate using the vendors' public descriptions. Specific buyers, inputs and deployment choices need confirmation at each customer. The comparison gives you a starting script for the one-hour landscape exercise.

| Product and advertised area | Representative trigger, user and inputs | Decision, output and question for discovery |
| --- | --- | --- |
| Vanta / security assurance | An assurance analyst prepares a control review using connected evidence and policy records | Analyst resolves gaps and prepares evidence. What did the last auditor send back? |
| OneTrust / third-party management | Procurement opens a supplier intake with a questionnaire and supporting documents | Risk reviewer conditions or escalates the review. Which answers still require email follow-up? |
| NAVEX / whistleblowing and incident management | A report enters a restricted case system. Authorized staff receive details and case history. | Investigator follows the allegation and records disposition. Where do access limits affect handoffs? |
| ServiceNow / GRC | A risk or control issue enters an enterprise workflow with owners and linked records | Owner remediates; reviewer assesses closure. Which decisions still happen in meetings? |

Use 15 minutes per vendor. Record trigger, user, inputs, systems or integrations, decision, output and advertised automation. Add a column called “customer evidence needed.” A vendor page can establish that a capability is marketed. A user's last completed file can show whether the existing deployment solves the specific problem. Product sources appear at the end.

## Interview for a recent decision

A **user** operates the workflow. A **reviewer** must trust or approve the output. A **buyer** controls budget or can sponsor the purchase. A **gatekeeper** can permit or block access, deployment or procurement. One person may hold several roles. At DunaWorks the AI compliance analyst might want a document-change assistant while the AI compliance lead owns decisions, security grants integration access and the general counsel's office controls the budget.

Run three 30-minute sessions. Use the first five minutes to choose one recent case, fifteen to reconstruct events, five on costs and five to summarize what would change the participant's decision. Across the whole course aim for roughly eight conversations, including three users of the same workflow, a budget owner, an assurance reviewer and adjacent operators. A conversation may cover two roles. An unfilled role remains an open question.

1. **With an operator:** “Show me the last revised specification you reviewed, with sensitive details removed. How did you hear about the change? Which versions did you compare? Where did you save the result?” Ask for active minutes, waiting time, frequency and a case that did not follow the usual path.
2. **With a reviewer:** “Take the last recommendation you sent back. Which fact was missing? What source would have changed your mind? What happens when evidence is unavailable?” Learn who decides materiality, accepts exceptions and verifies closure.
3. **With a buyer or gatekeeper:** “Who paid for the current process? Who approved the document permissions? What would a paid four-week test require, and what result would justify continuing?” Distinguish budget authority from enthusiasm.

**How to take notes.** Label each entry *observed*, *reported*, *inferred* or *unknown*. Seeing three separate spreadsheets in a walkthrough establishes that three files were used in that case. “We do this weekly” is a reported frequency. “They would buy a connector” is an inference. Ask for a dated example, an anonymized count or a procurement contact that could test it. Obtain permission before retaining any real file. A redacted walkthrough can suffice.

## Choose one decision and expose the assumptions

Compare four opportunities from the course: checking evidence completeness, preparing supplier follow-ups, routing changes to an interpretation owner and verifying remediation. Define a unit of work for each. “One changed specification assessed by the AI compliance reviewer” gives a denominator. “Continuous compliance” leaves almost everything open.

Score from 1 to 5 with higher always more favorable. For frequency, time spent today, budget access, permitted data access, reviewer acceptance, measurable benefit and differentiation, 5 means stronger. For integration, 5 means easier. Keep the supporting observation next to each score. Below are hypothetical ratings solely to demonstrate the calculation.

| Candidate | Frequency / effort / budget / data | Integration ease / acceptance / measurable benefit / differentiation | Sum out of 40 |
| --- | --- | --- | --- |
| Check completeness of one evidence request | 4 / 4 / 3 / 4 | 4 / 4 / 5 / 2 | 30 |
| Draft missing supplier questions | 4 / 3 / 3 / 3 | 3 / 3 / 4 / 2 | 25 |
| Route policy-relevant document changes | 4 / 4 / 3 / 4 | 4 / 3 / 5 / 4 | 31 |
| Verify closure evidence in tickets | 3 / 3 / 3 / 4 | 4 / 4 / 4 / 2 | 27 |

The 31-point candidate leads by one point. Lower its data-access score from 4 to 2 because approved historical versions are hard to obtain and the ranking reverses. In 30 minutes, spend ten defining criteria, ten assigning scores with evidence labels, and ten challenging the top assumptions. Some conditions make a pilot infeasible regardless of rank. If no one can authorize the necessary documents, test with synthetic pairs and leave real-world acceptance unknown.

**Decision for this exercise.** Use a document-change assistant because it permits a small, reviewable test. An alternative customer might have better access to audit-request evidence. Compare the best existing workaround, including the document editor's version comparison and an email to the AI compliance team, against the proposed feature.

## Build a prototype a reviewer can reject

Take one approved folder of product specifications and one reviewed internal policy. A new document version triggers comparison with the last reviewed version. The **bounded decision** is whether an identified change should be routed to the AI compliance reviewer under that policy. The reviewer decides what the change means and whether a formal assessment needs reopening.

**Fictional policy P-7.** Route changes to candidate visibility, scoring inputs, human approval or ranking purpose. An authorized, unexpired exception covers only its named change and scope. A missing previous version or inaccessible referenced annex produces “insufficient evidence.” A spelling-only change can close as routine once both versions are available. These are operational states for this prototype.

| Input pair | Expected output | Explanation the reviewer can check |
| --- | --- | --- |
| A. “Show unscored applicants” becomes “hide unscored applicants” | Route | Cite both queue rules and their version IDs. |
| B. “Reciept” becomes “Receipt” | Routine | Cite the changed word. No policy category changed. |
| C. New version says “see Annex B”; annex unavailable | Insufficient evidence | Ask for the exact annex and version. |
| D. Live ranking uses interview transcripts. An exception covers use in an offline evaluation | Route | Cite scoring input and environment. Exception scope differs. |
| E. A synthetic demo hides unscored records. A signed exception names this demo, period and revision | Approved exception | Attach authorization, match fields and expiry. Keep it visible to reviewer. |
| F. Document deleted; event contains only a title | Insufficient evidence | Mark unavailable source and request prior authorized snapshot; avoid inventing its content. |

**Two-hour build.** Use 20 minutes to assemble pairs and policy, 25 to label them with a reviewer or provisional answer key, 35 to build a manual or scripted version comparison, 25 to run it blind and 15 to inspect errors. A spreadsheet can hold source versions, quoted spans, applicable rule, proposed disposition, reviewer decision and reason. Label any unreviewed ground truth provisional. You can validate the decision without a live connector.

For a future Drive, Notion or GitHub integration, ask which tenant, folders or repositories can be read, which version identifiers are stable, whether the reviewer can open the cited version and what happens after access is revoked. Use a selected approved source in the first trial. A GitHub pull request can establish that code changed. A policy document can establish intended behavior. Neither alone establishes what happened in production.

### Test the agent’s links

Use this synthetic fixture within the prototype block. Every ID below is at version 1. Each link in the expected answer has to cite a passage or a test result. Keep earlier versions when a model or policy changes.

| Record | Supplied fact |
| --- | --- |
| O1, pilot policy §2 | A recruiter must review each application before exclusion. |
| T1, CMT | Meaningful human oversight of recommendations. |
| R1 and R2, risks | An unscored applicant disappears from review. A recruiter accepts an erroneous rejection without inspection. |
| C1 and C2, controls | C1 requires full-queue review before exclusion. C2 reconciles eligible IDs against the recruiter-visible queue. |
| E1, E2 and E3, evidence | E1 is the approved procedure for C1. E2 is a build-matched recruiter test demonstrating C1’s review screen. E3 is an engineering proposal to implement C2. |

**Expected links.** O1 → T1. T1 → R1 and R2. C1 addresses R1 by requiring full-queue coverage and R2 by requiring inspection. C2 addresses R1 by detecting omissions. C1 needs evidence of both implementation and actual review. E1 supports design and E2 supports implementation for the tested build. Request sampled decisions before marking C1 verified effective. E3 supports the **suggested** state for C2. Record the missing reconciliation run as an outstanding evidence requirement.

**Score the agent.** Count supported expected links recovered, unsupported links proposed and correct control states. Report denominators separately. Treat promotion to verified effective on this packet as a material error even if every link is correct. Repeat with E2 tied to a superseded build. The agent should retain the historical result and request evidence for the candidate build. [FordoX taxonomy](../../taxonomy.md)

## Evaluate misses, reviewer work and uncertain cases

A **baseline** is the current process measured on comparable work. Time the analyst using the existing version viewer and policy, including follow-ups. Then time assisted review with the same decision rules. Avoid letting a reviewer memorize the answer first. For a small pilot, split matched cases between conditions, counterbalance order across reviewers and reserve unseen cases. Record case difficulty and access failures. Count setup, review and rework separately.

Suppose an independent reviewer labels 20 synthetic pairs: 8 should route, 7 are routine, 3 have insufficient evidence and 2 have authorized exceptions. The prototype routes 9, of which 7 truly need routing and 2 are routine. It misses one material visibility change. It correctly handles the three insufficient-evidence cases and the two exceptions. The other five routine pairs close correctly.

| Question | Calculation | Meaning |
| --- | --- | --- |
| How many material changes were found? | 7 of 8 = 87.5% recall | One required review was missed. Inspect it before rollout. |
| How much alert noise reached the reviewer? | 2 of 9 routed alerts were false; precision is 7 of 9, about 78% | Nine alerts cost review time; two did not need escalation. |
| How often did the four-way disposition match? | (7 + 5 + 3 + 2) / 20 = 85% | Good aggregate agreement can coexist with a consequential miss. |
| Did time improve? | Baseline median 12 min; assisted median 8 min | A four-minute difference in these synthetic summaries. Check real workloads and tail cases. |

**Question.** A team proposes improving the dashboard by hiding “insufficient evidence” cases. What happens to recall? In the example, hiding the three unknowns need not change the seven-of-eight material-change count, because none of the reference labels for those three was “route.” It would remove three necessary follow-ups and understate work. Track abstentions and their resolution separately. A hidden missing annex can be a serious failure even if a binary routing metric looks unchanged.

**Evaluate trust.** Ask whether every cited passage exists in the authorized version, whether both normal and exceptional cases have enough context and whether overrides are recorded. Categorize misses by cause, such as unavailable source, bad version match, incomplete policy or erroneous interpretation. Each points to a different product change. Re-evaluate on held-out cases after adjusting the prototype.

## Write the one-page opportunity memo

Use one sentence each for customer, buyer, trigger, current process, pain, current alternative, proposed output, human decision, required data, baseline, success criteria and commercial next step. Label what interviews established, what the prototype demonstrated and what still needs testing.

| Memo field | Worked example for DunaWorks, entirely hypothetical |
| --- | --- |
| Customer, user, reviewer, buyer | B2B software teams with a AI product release review queue. Product engineers edit specs; AI compliance operations triages; AI compliance lead decides materiality; general counsel sponsors a trial. |
| Current workflow and pain | Editors send voluntary messages. Analysts compare versions manually and chase missing annexes. Frequency, waiting time and missed changes need customer evidence. |
| Output and authority | Draft review card with old and new citations, policy trigger, missing input or applicable exception. Human reviewer accepts, dismisses or requests evidence. |
| Pilot access | One approved folder, version history, internal policy and redacted past dispositions. Tenant administrator grants bounded access; security reviews retention and deletion. |
| Baseline and target | Measure current minutes per reviewed change and known material misses. Example target: reduce median active time by 25% with zero missed critical reference cases and all missing-source cases visible. |
| Commercial terms | Illustrative offer: EUR 2,000 fixed for four weeks, one team and up to 40 changes. Sponsor names reviewer and spending authority. Price and purchasing route are untested. |
| Decision after trial | Continue only if data access works, reviewers accept provenance, and targets hold on agreed cases. Otherwise revise the scope or stop. |

**Worked judgment.** The 20-case synthetic evaluation demonstrates that the prototype can surface a visibility change and preserve some unknowns. It also missed a material change. If the buyer rates that miss critical, the proposed quality threshold fails even though median time improved. Ask the reviewer to classify severity before seeing the prototype's result. No interview or purchase occurred in this example.

**Your finish line.** Replace at least three hypothetical fields with evidence from your conversations. If a buyer is still unknown, write “unknown” and name the question that would identify one. A defensible decision to abandon an opportunity is a valid course outcome.

## Vocabulary and product readings

| English term | Plain meaning | Magyarul |
| --- | --- | --- |
| Discovery interview | Reconstructing work and testing assumptions with a participant | problémafeltáró interjú |
| Buyer / gatekeeper | Controls spending / authorizes access or deployment | költségkeret gazdája / hozzáférés jóváhagyója |
| Baseline | Measured performance of today's process | összehasonlítási alapérték |
| Ground truth | Agreed reference answer for evaluation, with its limits | ellenőrzött referenciaeredmény |
| Precision / recall | Correct alerts among alerts / detected positives among actual positives | pozitív találatok pontossága / felismerési arány |
| Abstention | Explicitly withholding a conclusion when evidence is insufficient | döntéstől való tartózkodás |
| Paid pilot | Time-limited paid trial with a buyer and agreed acceptance criteria | fizetett próbaüzem |

These live pages were reviewed on 17 November 2026. They establish vendor positioning and documented workflows. Use the landscape exercise to discover what actually runs at a customer.

- **Vanta**, platform overview. Inspect evidence collection, monitoring and trust workflows. [Vendor overview](https://www.vanta.com/)
- **OneTrust**, Third-Party Management. Inspect assessment, lifecycle monitoring and workflow triggers. [Product page](https://www.onetrust.com/solutions/third-party-management/)
- **NAVEX**, About NAVEX One Whistleblowing & Incident Management. Read the case database and role-based access description. [Product help](https://help.navexglobal.com/epim/content/overview/overview.htm)
- **ServiceNow**, Governance, Risk, and Compliance. Inspect integrated risk, assurance and third-party workflows. [Product overview](https://www.servicenow.com/products/governance-risk-and-compliance.html)

**Pass condition.** A practitioner should be able to identify the exact decision your prototype supports, show how to detect a harmful miss, name who approves the result and state what evidence would justify paying for a pilot.
