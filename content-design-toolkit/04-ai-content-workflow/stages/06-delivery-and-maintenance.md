# Stage 06 — Delivery and Maintenance

Approve, document, and hand off content; manage updates and future revisions.

## Contents

- [1. Purpose and scope](#1-purpose-and-scope)
- [2. When to use AI](#2-when-to-use-ai)
- [3. Required human inputs](#3-required-human-inputs)
- [4. AI-assisted activities](#4-ai-assisted-activities)
- [5. Human responsibilities](#5-human-responsibilities)
- [6. Inputs and expected outputs](#6-inputs-and-expected-outputs)
- [7. Checkpoints and decision criteria](#7-checkpoints-and-decision-criteria)
- [8. Stage checklist](#8-stage-checklist)
- [9. End of workflow cycle and future revisions](#9-end-of-workflow-cycle-and-future-revisions)
- [10. Phase 4 references](#10-phase-4-references)

---

## 1. Purpose and scope

Stage 06 is the final stage in the AI Content Workflow. It has three purposes: authorising the deliverable for use through Final approval, transferring approved content through delivery, and managing the content's lifecycle after delivery.

**Final approval**

Final approval is the last human checkpoint before content is published, implemented, or handed off for use. It is carried out by the accountable approver — the person or role with authority to authorise the deliverable. Final approval confirms that:

- The content meets all mandatory requirements
- Any outstanding non-blocking issues documented at stage 04 or stage 05 have been reviewed, and a decision has been made to accept them or return the content for further work
- The content is ready to be used as it stands

Final approval is distinct from the Quality checkpoint (stage 04) and Locale approval (stage 05). Those checkpoints evaluated whether the content meets quality standards and locale requirements. Final approval authorises the deliverable for use. The authority for Final approval may rest with the content designer, a subject-matter expert, a product owner, a legal reviewer, or another accountable role, depending on the nature and risk of the content.

**Delivery**

Delivery is the transfer of approved content to the people, systems, or platforms that will publish or implement it. This may be a handoff to a development team, a submission to a content management system, a transfer to a publisher, or a direct publication. The delivery process varies by task; stage 06 ensures it is documented and that the recipients have the information they need.

**Maintenance**

Content delivered at this stage may need to be updated over time — in response to product changes, user feedback, errors, standards updates, or regulatory changes. Stage 06 establishes how the content will be maintained: who is responsible, what triggers a review, and when a change requires the full workflow rather than a minor correction.

---

## 2. When to use AI

**AI assistance is appropriate when:**

- Formatting or converting content for a delivery format — preparing a file for a specific platform, CMS template, or handoff specification
- Running a final consistency check across the deliverable before submission — terminology, labelling, phrasing patterns
- Drafting or structuring delivery documentation: handoff notes, change summaries, version descriptions
- Preparing maintenance documentation: a summary of what the content is, what it covers, what dependencies or related content it has, and what might prompt a review
- Generating a summary of changes for a changelog or version record

**AI assistance is not appropriate when:**

- Making the Final approval decision — this is a human authorisation that cannot be delegated to AI
- Deciding whether outstanding non-blocking issues should be accepted as exceptions — this requires the Final approver's judgement
- Assessing whether content is safe, legally compliant, or accurate — these require the appropriate expertise, not AI assessment
- Making delivery decisions about platform, channel, or audience targeting — these are content and product decisions

---

## 3. Required human inputs

The following must be in place before Final approval and delivery.

**Reviewed content from the preceding stage**

For single-language tasks: quality-reviewed content from stage 04.
For multilingual tasks: quality-reviewed source content and locale-approved locale versions from stage 05.

All required reviews must be complete before Final approval is sought. Final approval should not be used as a shortcut to bypass Quality review or Locale approval.

**Documentation of outstanding non-blocking issues**

Any non-blocking issues documented at stage 04 or stage 05 must be surfaced to the Final approver. The Final approver reviews these explicitly — they cannot be treated as already resolved by virtue of having been documented. The Final approver decides for each outstanding issue: accept it and proceed, or return the content for further work.

**Final approval authority and criteria**

The practitioner must know who has the authority to give Final approval for this content, and what criteria the content must meet to receive it. For some content, Final approval rests with the content designer; for other content, it requires a product owner, compliance reviewer, subject-matter expert, or legal sign-off. If the approval authority has not been established, it must be confirmed before the content proceeds.

**Delivery requirements**

The format, platform, and process for delivery must be established: where the content is going, in what format, to whom, and what documentation should accompany it.

---

## 4. AI-assisted activities

**Final consistency check**

Before submission for Final approval, AI can run a consistency check across the full deliverable — terminology, labelling, phrasing conventions, and any formatting requirements. The practitioner evaluates each finding and resolves genuine inconsistencies. This is a last-pass check, not a substitute for the structured quality review at stage 04.

**Delivery formatting**

AI can help convert or format content for a delivery format: reformatting a document for a CMS template, restructuring a file to meet a handoff specification, or preparing content for a specific platform.

Delivery formatting should normally be completed before Final approval, so the accountable approver can assess the deliverable in its intended delivery format. If formatting takes place after Final approval, the practitioner must verify that it has not changed the approved content. Any substantive content changes introduced during formatting require the relevant review and renewed Final approval before delivery.

*Illustrative example: A practitioner preparing onboarding content for implementation formats the reviewed content into the template required by the development team before seeking Final approval. The practitioner confirms that the formatted output matches the reviewed content and has not introduced errors or unintended changes, then submits it for Final approval in its delivery format.*

**Delivery documentation**

AI can help draft or structure handoff notes, change summaries, and version descriptions. These are for the practitioners and teams who will receive and implement the content. The practitioner confirms that the documentation accurately represents the delivered content and decisions made during the workflow.

**Maintenance documentation**

AI can help draft a maintenance record for the delivered content — what it covers, its dependencies, related content, review triggers, and owner. The practitioner confirms that the record accurately reflects the content and its context.

---

## 5. Human responsibilities

**Carrying out Final approval**

The accountable approver reviews the content and gives Final approval. This is not a rubber-stamp of the work done at previous stages; it is an independent confirmation that the content is ready to be used as it stands. The Final approver:

- Reviews the content against the Final approval criteria
- Reviews any outstanding non-blocking issues documented at stage 04 or stage 05, and explicitly accepts or returns each one
- Confirms that required reviews (Quality, Locale approval where applicable) have been completed
- Authorises the deliverable or identifies what must be resolved before authorisation

**Reviewing and deciding on outstanding issues**

Outstanding non-blocking issues documented at earlier stages have not been resolved — they have been carried forward for the Final approver's consideration. The Final approver reads each documented issue, assesses whether it is acceptable given the content's purpose and risk, and makes an explicit decision: accept and proceed, or return for further work. An issue that the Final approver considers unacceptable at this stage must be resolved before the deliverable is authorised, even if it was treated as non-blocking at an earlier stage.

**Delivering content**

The practitioner ensures the approved content is transferred in the correct format to the correct recipient, with the documentation needed for the recipient to understand and implement it. For content that will be implemented by a development team, this means a handoff that includes not just the content but the context required to implement it correctly — the brief, any implementation-critical decisions, and relevant constraints.

**Establishing the maintenance process**

For content that will remain in use over time, the practitioner establishes how it will be maintained. This includes:

- Who is responsible for the content after delivery
- What events would trigger a review: product changes, user feedback, identified errors, standards updates, regulatory changes
- Whether a future change requires the full workflow or can be managed as a minor correction (see below)
- Where the maintenance record is kept and how it will be updated

**Distinguishing workflow revisions from minor corrections**

Not every update to delivered content requires a full workflow cycle. Minor corrections — such as fixing a typographical error or correcting a clearly established, low-impact error that does not change the content's meaning, intent, requirements, or expected user outcome — may be manageable without returning to stage 01. Substantive or material changes — including changes affecting accuracy, audience, objective, structure, voice, accessibility, or compliance — should re-enter the workflow at the appropriate stage.

The practitioner makes this distinction when a change is requested, and documents the decision. Changes initially assessed as minor must be escalated to a full workflow review if their impact proves greater than expected.

---

## 6. Inputs and expected outputs

**Required inputs**

- Quality-reviewed content from stage 04 (all tasks)
- Locale-approved locale versions from stage 05 (multilingual tasks)
- Documentation of any outstanding non-blocking issues from stage 04 and stage 05
- Final approval authority and criteria
- Delivery format, platform, and recipient

**Expected outputs**

- Final-approved content, authorised for use
- Record of Final approval: who approved, when, against what criteria
- Record of decisions on outstanding non-blocking issues
- Delivered content in the required format, with delivery documentation
- Maintenance record: owner, review triggers, version history

The Final approval record is a governance document. It confirms that the content has met the required standard and been authorised for use by the accountable approver. It is the reference point for future questions about whether the content was approved, by whom, and on what basis.

---

## 7. Checkpoints and decision criteria

### Final approval checkpoint

The Final approval checkpoint is mandatory. It is the last human decision before content is used. The Final approver carries it out; it cannot be delegated to AI or passed without a decision by a qualified human.

**What to confirm:**

- **Completeness of review:** Have all required reviews been completed — Quality review at stage 04, and Locale approval at stage 05 for each required locale?
- **Requirements met:** Does the content meet all mandatory acceptance criteria?
- **Outstanding issues resolved:** Have all outstanding non-blocking issues from stages 04 and 05 been reviewed? Has an explicit decision been made on each?
- **Delivery readiness:** Is the content in the correct format and state for delivery?

**Decision: Is the deliverable authorised for use?**

| Outcome | Action |
|---|---|
| Content meets all criteria; outstanding issues reviewed and accepted | Final approval granted; proceed to delivery |
| Outstanding issues reviewed; one or more not accepted | Return the specific issue to the appropriate earlier stage for resolution; re-seek Final approval after correction |
| Content has an issue not previously identified | Assess the stage at which it should be resolved; return there before re-seeking Final approval |
| Required review not completed | Complete the missing review before Final approval is sought |
| Final approval authority has not been confirmed | Confirm who must approve before proceeding |

**A note on accepted exceptions**

A non-blocking issue explicitly accepted by the Final approver becomes part of the content's approved state. The acceptance and its rationale must be recorded in the Final approval record. If a future revision affects an accepted exception, it must be reviewed again.

---

## 8. Stage checklist

**Before Final approval**
- [ ] Quality review at stage 04 is complete
- [ ] Locale approval at stage 05 is complete for each required locale (multilingual tasks)
- [ ] Outstanding non-blocking issues from stages 04 and 05 are documented and surfaced to the Final approver
- [ ] Final approval authority and criteria are confirmed
- [ ] A final consistency check has been completed

**Final approval decision**
- [ ] Content has been reviewed against Final approval criteria by the accountable approver
- [ ] All outstanding non-blocking issues have been reviewed; explicit decisions have been made on each
- [ ] Final approval has been granted (or specific issues identified for resolution)
- [ ] Final approval record is complete: who approved, when, against what criteria, and decisions on any accepted exceptions

**Delivery**
- [ ] Content is in the correct format for delivery
- [ ] Delivery documentation is complete
- [ ] Content has been transferred to the correct recipient
- [ ] Recipient has the context needed to implement the content correctly

**Maintenance**
- [ ] Maintenance owner is confirmed
- [ ] Review triggers are established
- [ ] Maintenance record is in place

---

## 9. End of workflow cycle and future revisions

Stage 06 marks the end of the workflow cycle for this deliverable. The content has been researched, planned, created, reviewed, localised where applicable, and approved. It is now in use.

**When content needs to be updated**

Delivered content may need to be revised after delivery. The practitioner assesses the nature and scope of the change before deciding how to handle it.

| Nature of change | Approach |
|---|---|
| Minor correction — typographical error or low-impact error that does not change meaning, intent, requirements, or expected user outcome | Assess whether a full workflow cycle is needed; document the correction and the rationale for the approach taken. Escalate to a full workflow review if the impact proves greater than expected. |
| Substantive or material revision — change affecting accuracy, audience, objective, structure, voice, accessibility, or compliance | Re-enter at the earliest stage affected by the change: stage 01 for new or materially changed research questions or discovery needs; stage 02 for changes to approach or requirements; stage 03 for new content creation or substantial restructuring; stage 04 for content requiring renewed Quality review |
| New locale — adding a language that was not in the original scope | Re-enter at stage 05 with the existing quality-reviewed source content |
| Source content change that affects existing locale versions | Assess the impact across all existing locale versions. Revise the source content through the appropriate earlier stages and complete Quality review at stage 04. Then return to stage 05 for each affected locale version. Reassess locale versions that have already passed Locale approval but have not received Final approval. |

When content re-enters the workflow, the existing approval record remains for the content as it was; a new approval record is created for the revised version.

**Maintaining the approval record**

The Final approval record and maintenance documentation are living records. They should be updated when:
- A revision is made and re-approved
- An accepted exception is later resolved
- A review trigger is met and the content is assessed
- Ownership or responsibility changes

---

## 10. Phase 4 references

The following resources from the AI Content Creation module (`03-ai-content-creation/`) are relevant to stage 06.

| Resource | Relevance to this stage |
|---|---|
| [`output-evaluation-rubric.md`](../../03-ai-content-creation/output-evaluation-rubric.md) | Useful when evaluating AI-generated content during the final consistency check. It supports the assessment of AI output but does not replace the task-specific Final approval criteria or the accountable approver's decision. |
| [`ai-content-principles.md`](../../03-ai-content-creation/ai-content-principles.md) | Foundational principles for the full workflow — relevant to the Final approver's assessment of whether the content reflects appropriate human oversight throughout its development |
| [`failure-modes.md`](../../03-ai-content-creation/failure-modes.md) | A reference for the final consistency check — common AI content failure modes that may have persisted through earlier reviews, particularly false completeness and voice drift |
| [`grounding-guide.md`](../../03-ai-content-creation/grounding-guide.md) | Relevant when using AI to assist with delivery formatting or documentation — the same grounding principles apply to these activities as to content generation |
| [`prompt-templates/`](../../03-ai-content-creation/prompt-templates/) | Prompt templates for delivery formatting, documentation drafting, and final consistency checks |
