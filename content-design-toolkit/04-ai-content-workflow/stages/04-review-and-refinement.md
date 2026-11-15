# Stage 04 — Review and Refinement

Evaluate content against requirements, voice guidelines, content standards, and applicable accessibility and compliance requirements.

## Contents

- [1. Purpose and scope](#1-purpose-and-scope)
- [2. When to use AI](#2-when-to-use-ai)
- [3. Required human inputs](#3-required-human-inputs)
- [4. AI-assisted activities](#4-ai-assisted-activities)
- [5. Human responsibilities](#5-human-responsibilities)
- [6. Inputs and expected outputs](#6-inputs-and-expected-outputs)
- [7. Checkpoints and decision criteria](#7-checkpoints-and-decision-criteria)
- [8. Stage checklist](#8-stage-checklist)
- [9. Handoff to next stage](#9-handoff-to-next-stage)
- [10. Phase 4 references](#10-phase-4-references)

---

## 1. Purpose and scope

Stage 04 is the structured quality evaluation for content developed at stage 03. Its purpose is to assess the draft against requirements, voice guidelines, content standards, and applicable accessibility and compliance requirements — and to produce content that meets those criteria before it proceeds to localisation or delivery.

This stage involves two related activities: review (assessing what the content does and does not meet) and refinement (correcting what does not meet requirements). They are not necessarily separate sequential steps; the practitioner moves between them as the review proceeds.

**What this stage determines**

The Quality checkpoint at stage 04 establishes whether content meets the requirements for the work to continue. It is not a comprehensive test of perfection. The exit condition is content that meets the applicable requirements, voice guidelines, and standards — not content that the practitioner would not change anything further in.

Stage 04 is also the point at which the content's suitability for localisation (stage 05) or delivery (stage 06) is confirmed. For single-language tasks, work proceeds directly to stage 06 after a successful quality review. For multilingual tasks, the quality-reviewed source content proceeds to stage 05.

**What this stage is not**

Stage 04 is not final approval. The Quality checkpoint confirms that content meets the required standard; it does not authorise the deliverable for use. Final approval is a separate decision taken at stage 06, after all required reviews are complete.

---

## 2. When to use AI

**AI assistance is appropriate when:**

- Running consistency checks across a document or content set — terminology, labelling, phrasing patterns
- Flagging potential voice or tone misalignments against supplied guidelines
- Identifying candidate accessibility issues: reading level, sentence complexity, label clarity, instruction completeness
- Generating alternative formulations for content elements that do not meet requirements
- Summarising review findings for documentation in the Decision and iteration log
- Checking for internal contradictions or structural inconsistencies within the draft

**AI assistance is not appropriate when:**

- Deciding whether a flagged issue is a genuine problem in context — this requires the practitioner's editorial judgement
- Making editorial decisions about how to resolve a quality finding
- Assessing whether content is factually or technically accurate — accuracy evaluation requires domain knowledge or subject-matter review
- Determining whether the content meets applicable compliance or legal requirements — compliance evaluation requires the appropriate expertise
- Approving or certifying the content as meeting quality standards — no AI-generated assessment constitutes a passed Quality checkpoint

**A note on AI-assisted review findings**

AI quality checks can produce false positives (flagging issues that are not problems in context) and false negatives (not flagging genuine problems that require domain knowledge or editorial judgement to identify). The practitioner evaluates every AI-generated finding independently. A clean AI assessment does not confirm that the content passes quality review; a practitioner review must be completed regardless.

See [`failure-modes.md`](../../03-ai-content-creation/failure-modes.md) for specific failure modes to watch for when using AI-assisted review.

---

## 3. Required human inputs

The following inputs or arrangements must be in place before structured review begins.

**The draft from stage 03**

The practitioner-reviewed draft produced at stage 03, with any documented assumptions or non-blocking questions from creation. Any issue that could prevent reliable evaluation should have been resolved before handoff; if the draft arrives with unresolved blocking issues, those must be addressed before quality review proceeds.

**The confirmed content brief**

The brief from stage 02 is the primary reference for evaluating whether content addresses its stated objective, serves its target audience, and meets its requirements. The review is conducted against the brief; a draft that meets the brief's requirements passes quality review even if the practitioner would have made different choices.

**Voice, tone, and content standards**

The applicable voice and tone guidelines, content standards, and any mandatory rules (Rules) the content must follow. These are the criteria for evaluating voice and tone quality. The practitioner should distinguish between mandatory requirements (Rules) and contextual guidance (Recommendations, Contextual) when evaluating the draft and recording findings.

**Evaluation criteria**

The practitioner should know what the Quality checkpoint requires for this content type: what mandatory criteria must be met, what constitutes a blocking finding, and what minor, non-blocking issues may be accepted and documented. See [`output-evaluation-rubric.md`](../../03-ai-content-creation/output-evaluation-rubric.md) and `human-checkpoints.md` for structured criteria.

**Subject-matter or specialist input, where required**

For content requiring factual, technical, accessibility, legal, or compliance review, the appropriate expertise must be identified and arranged before the quality review begins. The specialist assessment may take place during the review, but it must be completed before the Quality checkpoint can pass. AI cannot substitute for subject-matter or specialist review.

---

## 4. AI-assisted activities

**Consistency scanning**

AI can check for inconsistencies across a draft or content set: terminology that varies without reason, labelling that is inconsistent across related items, phrasing patterns that differ where consistency is expected. The practitioner evaluates each flagged inconsistency to determine whether it is a genuine problem or an intentional variation.

*Illustrative example: A practitioner reviewing a set of related instructional messages supplies them to AI along with the product's approved terminology list and asks for a check against that list. AI flags three terms that differ from the approved list. The practitioner confirms two are genuine inconsistencies to correct, and judges the third to be an acceptable variation given its specific context.*

**Voice and tone checking**

AI can compare draft content against supplied voice and tone guidelines and flag passages that may not align. The practitioner evaluates each flagged item in context, considering audience, register, and purpose. AI cannot assess whether a tone choice is effective for the audience — it can only compare against stated guidelines.

**Accessibility flagging**

AI can identify candidate accessibility issues: sentences above a target reading level, instructions that may be incomplete, labels that do not describe their associated element, or error messages that do not explain what went wrong or what to do. These are candidates for review; the practitioner confirms whether each is a genuine issue before correcting it.

**Alternative generation for failed elements**

Where a content element does not meet requirements and needs to be rewritten, AI can generate alternatives for the practitioner to evaluate. This follows the same process as content creation at stage 03: alternatives are for evaluation, not for acceptance by default.

**Review documentation**

AI can help structure and summarise review findings for recording in the Decision and iteration log. The practitioner confirms that the summary accurately reflects the actual findings and decisions made.

---

## 5. Human responsibilities

**Conducting the quality review**

The practitioner performs a deliberate, structured review of the draft. AI can assist with specific checks, but it does not perform the review. The practitioner reads and assesses the content, applies the evaluation criteria, and determines what meets requirements and what does not.

Reviewing content requires deliberate separation from the generation process. Even when the same person drafted and reviews the content, the review should be conducted as a distinct activity — not as a continuation of drafting. Returning to the content with fresh perspective makes the evaluation more effective.

**Interpreting AI-generated findings**

Every AI-generated finding from a consistency check, voice scan, or accessibility flag is evaluated by the practitioner before it is acted on. The practitioner decides: is this a genuine problem in context? What is the right correction? The finding is an input to the decision, not the decision itself.

**Resolving conflicting recommendations**

Review may surface conflicting guidance, such as a voice recommendation that conflicts with a readability consideration, a terminology requirement that affects natural phrasing, or competing editorial preferences. The practitioner resolves these conflicts according to the status and purpose of the applicable guidance. Mandatory requirements (Rules) must not be overridden by editorial preference. Where mandatory requirements conflict, the issue must be escalated to the appropriate owner or specialist before the Quality checkpoint can pass. Recommendations and contextual guidance are evaluated in relation to the audience, objective, and content context. Significant decisions should be documented.

**Distinguishing mandatory criteria from non-blocking issues**

Not all quality findings have the same significance. Mandatory criteria (Rules) must be met before the content proceeds. Minor, non-blocking issues that cannot be resolved during review may be documented for consideration during Final approval at stage 06. The practitioner does not accept these issues as exceptions at the Quality checkpoint. The practitioner makes this distinction for every finding.

**Deciding when the content is ready to proceed**

The practitioner confirms when the content meets the requirements for this stage. The exit condition is content that meets the applicable criteria, not content free of every possible improvement. If minor non-blocking issues remain, they are documented. If mandatory criteria are not met, the content does not proceed.

---

## 6. Inputs and expected outputs

**Required inputs**

- Practitioner-reviewed draft from stage 03
- Confirmed content brief from stage 02
- Voice, tone, and content standards applicable to the content
- Evaluation criteria, including mandatory requirements and acceptance criteria
- Subject-matter or specialist inputs where required

**Expected outputs**

- Quality-reviewed and refined content that meets the applicable requirements, voice guidelines, and standards
- Documented review findings: what was checked, what was found, what decisions were made
- Change log recording significant changes made during refinement and the reason for each
- Notes on any outstanding non-blocking issues and their rationale, for consideration at Final approval
- Quality-reviewed content ready to proceed to stage 05 (localisation) or stage 06 (delivery)

Mandatory acceptance criteria must be met before content proceeds. Any issue that could prevent reliable evaluation at the next stage must be resolved at stage 04. Minor, non-blocking issues that remain unresolved should be explicitly documented with their rationale for consideration at Final approval; documenting them does not substitute for meeting mandatory requirements.

---

## 7. Checkpoints and decision criteria

### Quality checkpoint

The Quality checkpoint is mandatory at stage 04. It is the final structured evaluation before the content proceeds to localisation or delivery.

**What to check:**

- **Objective:** Does the content address its stated objective and meet the brief?
- **Voice and tone:** Does it reflect the applicable voice and tone requirements? Is the tone appropriate for the audience and context?
- **Content standards:** Does it follow the applicable mandatory requirements (Rules) and relevant recommendations (Recommendations, Contextual guidance)?
- **Accessibility:** Does it meet applicable accessibility requirements, including, where relevant: plain language, reading level, label clarity, instruction completeness, error message quality?
- **Consistency:** Is it internally consistent? Is it consistent with related content?
- **Accuracy:** Is factual or technical content accurate and verifiable? Has subject-matter review been completed where required?

**Decision: Does it meet the acceptance criteria?**

| Outcome | Action |
|---|---|
| Content meets all mandatory criteria | Proceed to stage 05 (multilingual) or stage 06 (single-language) |
| Content has specific, correctable issues | Revise at stage 04; re-check after revision |
| Minor, non-blocking issues remain | Document the issues and rationale for consideration during Final approval at stage 06. Proceed only if all Quality acceptance criteria are met. |
| Content has a fundamental quality problem that cannot be corrected at stage 04 | Return to stage 03 to revise the content |
| Quality review identifies a direction or brief problem | Return to stage 02 to revise the brief or approach |

**What happens if mandatory criteria are not met**

Content does not proceed to stage 05 or stage 06 until mandatory criteria are satisfied. Document the specific finding and the action taken in [`../templates/decision-and-iteration-log.md`](../templates/decision-and-iteration-log.md).

The Quality checkpoint is not the same as final approval. It confirms that content meets the required standard; it does not authorise the deliverable for use. Final approval is a separate decision at stage 06.

---

## 8. Stage checklist

**Before review begins**
- [ ] Draft from stage 03 is complete and any blocking issues from creation have been resolved
- [ ] Confirmed brief is available as the primary evaluation reference
- [ ] Voice, tone, and content standards are identified
- [ ] Evaluation criteria and acceptance criteria are established
- [ ] Subject-matter or specialist input is available where required
- [ ] Review is conducted as a distinct activity, with deliberate separation from drafting

**During review**
- [ ] AI-generated findings have been evaluated by the practitioner before being acted on
- [ ] Mandatory criteria (Rules) have been distinguished from recommendations and contextual guidance
- [ ] Conflicting recommendations have been resolved and significant conflicts documented
- [ ] Factual or technical accuracy has been verified where required

**Quality decision**
- [ ] Content meets all mandatory acceptance criteria
- [ ] Non-blocking issues that remain are documented with rationale for consideration at Final approval
- [ ] All significant review findings and decisions are recorded
- [ ] The practitioner has confirmed the content is ready to proceed

---

## 9. Handoff to next stage

Stage 04 produces quality-reviewed content that proceeds to either stage 05 (Localisation and adaptation) or stage 06 (Delivery and maintenance), depending on whether the task is multilingual.

**What to pass forward**

- Quality-reviewed content
- The confirmed content brief
- Review findings and change log from stage 04
- Notes on any outstanding non-blocking issues and their rationale, for consideration at Final approval
- Confirmation that mandatory criteria have been met
- Subject-matter review records, where applicable
- For multilingual tasks: the quality-reviewed source content is the input to stage 05; locale-specific review and approval happen there

**What to record**

Document in [`../templates/decision-and-iteration-log.md`](../templates/decision-and-iteration-log.md):
- Significant review findings and the decisions made in response
- Changes made during refinement and the reason for each
- Outstanding non-blocking issues and their rationale, for consideration at Final approval
- Returns to earlier stages and why

**Handoff template**

For collaborative tasks — where stage 05 or stage 06 will be carried out by another contributor — use [`../templates/handoff-template.md`](../templates/handoff-template.md) to transfer the reviewed content and context. The handoff should confirm that the Quality checkpoint has been completed and note any outstanding non-blocking issues documented for consideration at Final approval.

---

## 10. Phase 4 references

The following resources from the AI Content Creation module (`03-ai-content-creation/`) are most directly relevant to stage 04.

| Resource | Relevance to this stage |
|---|---|
| [`output-evaluation-rubric.md`](../../03-ai-content-creation/output-evaluation-rubric.md) | The primary structured evaluation tool for quality review — provides criteria for assessing AI-generated and AI-assisted content against requirements, voice guidelines, and standards |
| [`failure-modes.md`](../../03-ai-content-creation/failure-modes.md) | Common AI-assisted content problems relevant to quality review: voice drift, false completeness, accuracy issues, inconsistent terminology — a useful reference for directing the practitioner's attention during review |
| [`ai-content-principles.md`](../../03-ai-content-creation/ai-content-principles.md) | Foundational principles for evaluating AI-assisted content — particularly the distinction between AI-generated findings and human editorial decisions |
| [`prompt-templates/`](../../03-ai-content-creation/prompt-templates/) | Prompt templates for AI-assisted review activities: consistency checks, voice alignment review, accessibility flag scanning |
| [`grounding-guide.md`](../../03-ai-content-creation/grounding-guide.md) | Relevant when using AI to assist with specific review activities — the same grounding principles apply to review prompts as to creation prompts |
