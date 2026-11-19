# FordoX risk and compliance taxonomy

A recruiter can see a suggested rejection. Can she find every eligible application and change the decision in time? The answer depends on the duty being tested, who owes it and what the evidence covers. The examples below use fictional DunaWorks pilot terms. Hungarian equivalents are learning aids.

## From a source to a duty

| Concept | Hungarian | What to record |
| --- | --- | --- |
| Source | forrás | A document or instrument with identifiable versions. Record issuer or contracting parties, authority, jurisdiction where relevant, version and applicable dates. Examples include a law, a signed agreement and an approved internal policy. |
| Provision | rendelkezés | A cited article, paragraph or clause in a specific source version. Keep the passage and a locator a reviewer can open. |
| Obligation | kötelezettség | A duty or prohibition. Record who owes what conduct, to whom where relevant, for which activity and population, under what conditions and by when. |
| Regulatory Subject | szabályozási tárgy | In Lynx this unit can express a duty, right, condition or exemption. Identify which kind the passage expresses before extracting a duty. |
| Compliance Micro Theme (CMT) | megfelelőségi résztéma | FordoX’s name for an operational topic. Assign one primary CMT per Regulatory Subject. Several subjects can share *human oversight*, including duties owed by different parties. |

One provision can establish several obligations. One obligation can draw on several provisions. Label each citation by its purpose, such as **establishes duty**, **defines scope** or **supplies exception**. Record interpretive guidance with its issuer and version as **informs interpretation**. A versioned passage reference or a dedicated Provision record can preserve the same citation. Lynx-style article, paragraph and subparagraph IDs are an implementation option. Secondary CMT links remain an option for future discovery.

## Writing a compliance risk

**Risk** (*kockázat*) is uncertainty that could affect an objective. In a compliance scenario, identify how a named party could miss a specific duty. Then ask who could be affected and how. A risk domain groups related risks, for example failures of human oversight. A sub-risk is a recurring failure type, such as an unavailable intervention. Link each scenario directly to the duty it could miss.

| Question | Worked trace from the fictional pilot agreement |
| --- | --- |
| Where is the duty? | DunaWorks and the employer signed pilot agreement v1. Clause 2(a) establishes DunaWorks’ duty to make eligible applications visible to ordinary recruiters and prevent exclusion until the review step is recorded. Clause 1 defines eligible applications for the pilot vacancy. |
| Who else owes a duty? | Under clause 2(b), the employer must ensure a recruiter actually reviews each eligible application before exclusion. Both subjects have the primary CMT *human oversight*. |
| How could the duty be missed? | A score filter could hide an unscored eligible application, breaching DunaWorks’ visibility duty. A recruiter could record a review without inspecting the file, breaching the employer’s review duty. |
| What could follow? | An applicant could lose an interview. Establishing an actual missed interview requires evidence of the hiring decision. |
| What control and evidence address visibility? | Engineering supplies an independently pageable full queue. The approved procedure supports its design. A matching recruiter-role traversal against a frozen manifest tests implementation in a particular build and configuration. Employer decision samples are needed to assess actual review. |
| What can Compliance conclude? | In the Week 7 Build D exercise, E is eligible and missing. Visibility fails for that vacancy. The broader human-oversight assessment has insufficient information. Engineering owns the fix, QA (quality assurance) supplies the corrected run and Éva verifies it. The release director holds live ranking pending review. |

## Controls and evidence

A **policy requirement** states what must happen. A **control** (*kontroll*) is a safeguard with an objective, owner, trigger and scope. An **execution** records one occasion on which a person or system performed it. A **test** checks specified behavior against a criterion. For example, the product serves a page of the full queue when a recruiter opens it. QA tests the visibility safeguard by traversing every page and comparing the result with eligible submissions. A scheduled reconciliation can itself be a detective control, with a record for each execution.

A duty can have several scenarios. A scenario may need several controls and a control can address several scenarios. For each coverage claim, explain how the safeguard addresses that failure and cite supporting evidence. Record **implementation status** (proposed, implemented, retired) separately from **effectiveness** (what a reviewer established for a named scope and period). A planned control can have design evidence. Compliance needs evidence of operation to credit its effect in practice.

**Assessment evidence** establishes the relevance of a duty or risk, such as a specification showing who uses a recommendation. **Control evidence** supports a particular design, implementation or operating claim. For each claim record what was requested, what arrived, its source and version, population, period, reviewer, verification method, conclusion and limits. An artifact can support several claims with different limits.

## From assessment to decision

**Inherent risk** (*eredendő kockázat*) describes exposure before relevant safeguards. **Residual risk** (*maradványkockázat*) describes exposure after considering the controls supported by evidence. State the population, time horizon, likelihood of the duty failure, possible impacts, rubric and uncertainty. A **test criterion** defines what a run must demonstrate, for example zero missing eligible IDs. **Risk appetite** (*kockázatvállalási hajlandóság*) expresses broad willingness to take risk. **Approved tolerance** (*kockázattűrés*) sets a limit on residual exposure for a particular scope. Record its approving authority, source and version. In the Build D packet the residual rating is unresolved and the approved tolerance is not supplied.

| Decision field | What the record says |
| --- | --- |
| Risk disposition | Treat the risk, for example through remediation, or record authorized acceptance of residual risk (*a maradványkockázat elfogadása*). Acceptance preserves the assessed rating. |
| Escalation | Record referral, recipient, reason, interim restrictions and due date. At DunaWorks, Product Leadership may accept residual risk within delegated authority. The chief executive officer (CEO) is the ultimate escalation authority. Internal delegation cannot waive an applicable duty. |
| Finding status | Open, awaiting retest or verified closed. Name the verifier and the scoped evidence needed for closure. |
| Release decision | The release authority records scope, conditions and expiry. A **hold** pauses release until named evidence or review arrives. A **block** prohibits deployment in the named scope because a mandatory condition or prohibition rules it out. Record what would permit reconsideration. |
| Compliance assessment outcome per requirement | Compliance records whether the requirement is met, unmet or **Insufficient information**. For insufficient information, record what is missing, why it matters, who will supply it and when review resumes. |

For a separate example, a completed assessment rates residual exposure Medium against an approved Low tolerance for that use. Product Leadership commissions further treatment or escalates beyond its mandate. In the Build D case, the missing rating and tolerance leave that comparison open. A reviewer can verify a software fix while a broader requirement or release decision remains open. Reassess when the relevant model, population, workflow, control or source version changes.

Practice the distinctions in [Week 2](chapters/week-02/chapter.md#classify-the-evidence), [Week 6](chapters/week-06/chapter.md#test-the-agents-links) and [Week 7](chapters/week-07/chapter.md#answer-key-and-a-reusable-decision-record).
