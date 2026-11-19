# FordoX risk and compliance taxonomy

A recruiter clicks **Reject** after reading a model recommendation. To assess that interaction, DunaWorks needs to know what the system promises, what could harm the applicant, which safeguards operated and who may decide whether the remaining exposure is acceptable. The English terms below follow the FordoX taxonomy. Hungarian equivalents are learning aids. All DunaWorks rules, IDs and ratings used here are fictional.

| Concept | Hungarian | Question to answer in the recruitment case |
| --- | --- | --- |
| Source / obligation | forrás / kötelezettség | Which passage creates an expectation for this entity and use? Identify its authority, version and applicable dates. An internal pilot rule can also create an obligation. |
| Compliance Micro Theme (CMT) | megfelelőségi résztéma | What operational topic connects this obligation to the product? Meaningful human oversight covers how recruiters understand, challenge and change a recommendation. |
| Risk domain / sub-risk | kockázati terület / alkockázat | Under human oversight, record the concrete event and harm. A recruiter follows an erroneous rejection and an eligible applicant loses an interview opportunity. |
| Inherent risk | eredendő kockázat | How likely and how serious is that outcome before controls? Record population, assumptions, rationale, uncertainty and approved scoring rubric. |
| Control | kontroll, kockázatkezelő intézkedés | What action changes exposure? Requiring review before rejection is preventive. Sampling decisions to detect rubber-stamping is detective. Reopening affected applications is corrective. |
| Assessment evidence | az alkalmazandóságot vagy a kockázatot alátámasztó bizonyíték | What establishes the relevance of the theme or risk? A versioned specification shows that a score influences rejection. |
| Control evidence | a kontrollt alátámasztó bizonyíték | What supports a claim about design, implementation or operation? A procedure describes the design. A role-matched test demonstrates the override in one build. Sampled decisions show how people actually reviewed cases. |
| Control effectiveness | a kontroll eredményessége | Did the safeguard achieve its objective in the assessed setting? Record scope, verification method, reviewer and limitations. |
| Residual risk | maradványkockázat | What exposure remains after considering verified controls? A planned appeal route earns no reduction. Record an unresolved rating when the evidence cannot support one. |
| Risk appetite / tolerance | kockázatvállalási hajlandóság / kockázattűrés | Appetite expresses management’s broad willingness to take risk. Tolerance sets the approved limit for this scenario and scope. Record its owner and version. |
| Risk decision | kockázatkezelési döntés | Who has authority, what outcome follows, and what evidence or change would reopen the decision? Acceptance records a judgment. It leaves the assessed score intact. |

## Writing a compliance risk

FordoX uses *risk* broadly enough to include harm to people. For a compliance review, first identify the obligation, who owes it and how that party could fail to meet it. Record the possible consequences for people in the impact assessment. A finding requires evidence of what happened within a defined scope.

| Question | DunaWorks example |
| --- | --- |
| What is the topic (CMT)? | Human oversight (*emberi felügyelet*). |
| What is the obligation (*megfelelési kötelezettség*)? | A fictional pilot agreement requires DunaWorks to let ordinary recruiters override a suggested rejection before it takes effect. |
| What is the compliance risk (*megfelelőségi kockázat*)? | A permissions change could reserve the override for administrators, leaving DunaWorks unable to provide the promised recruiter override. |
| What is the possible impact (*lehetséges következmény*)? | An erroneous rejection could cost an applicant an interview. The employer might also suspend the pilot. |
| What would count as a finding (*megállapítás*)? | In a hypothetical test, an ordinary recruiter is denied the override on the pilot configuration. Record the build, role, configuration and observed result. An administrator-only test would leave recruiter access unknown. |

Suppose the recruiter catches the error and phones the applicant. The applicant gets the interview. DunaWorks still needs to correct the permissions and verify that recruiters can exercise the override it promised.

## From assessment to decision

Suppose a separate, completed assessment of discriminatory recommendations finds high inherent risk under DunaWorks’ approved rubric. A reviewer verifies subgroup tests, human-review records and the handling of candidate challenges. The risk owner rates the remaining exposure Medium and explains the limits of the evidence. The approved tolerance for this use is Low. There is enough evidence to assign a rating, yet the rating exceeds the limit.

| Outcome | Hungarian | When to use it |
| --- | --- | --- |
| Accept | elfogadás | Verified residual exposure is within the applicable limit, mandatory conditions are met and the authorized owner signs for a defined scope. |
| Remediate | helyesbítő intézkedés elrendelése | Safeguards or evidence need work. For the example above, assign an owner to investigate remaining disparities, test the change and reassess. |
| Escalate | döntés magasabb szintre emelése | The decision exceeds delegated authority or needs an authorized exception review. Record the receiving authority and interim restrictions. |
| Block / Do not deploy | bevezetés megtiltása | A prohibition, unmet mandatory prerequisite or unacceptable safety or rights exposure prevents deployment. Internal approval cannot waive an applicable legal requirement. |

The reasoning runs from obligation through theme, risk, safeguards and evidence to a decision against tolerance. Store the relationships as many-to-many. One oversight theme may expose both undue reliance and exclusion from review. One full-queue review control may address both risks. Each risk can also need another control. Give records stable IDs and versions. For each link, record why the relationship holds and who verified it.

A control-library entry identifies the objective, type, owner, linked obligations and risks, implementation state, testing frequency and expected evidence. Each evidence item records the claim, source, date, version, owner, reviewer, coverage period and verification status. Preserve the difference between evidence requested and evidence received. Reassess when a model, dataset, workflow, supplier, market or governing requirement changes.

The exercises in [Week 2](chapters/week-02/chapter.md#classify-the-evidence), [Week 6](chapters/week-06/chapter.md#test-the-agents-links) and [Week 7](chapters/week-07/chapter.md#answer-key-and-a-reusable-decision-record) use these distinctions.
