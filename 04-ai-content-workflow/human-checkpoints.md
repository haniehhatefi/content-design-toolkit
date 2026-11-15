# Human Oversight Checkpoints

Five checkpoints for human direction, review, and approval in AI-assisted content work.

## Contents

- [Purpose and scope](#purpose-and-scope)
- [Overview of the five checkpoints](#overview-of-the-five-checkpoints)
- [Mandatory and conditional checkpoints](#mandatory-and-conditional-checkpoints)
- [Checkpoint definitions](#checkpoint-definitions)
  - [Direction](#direction)
  - [Alignment](#alignment)
  - [Quality](#quality)
  - [Localisation](#localisation)
  - [Final approval](#final-approval)
- [Responsibility matrix](#responsibility-matrix)
- [AI assessments and human decisions](#ai-assessments-and-human-decisions)
- [Supporting resources](#supporting-resources)

---

## Purpose and scope

This document defines the five human oversight checkpoints in the AI Content Workflow. It establishes when each checkpoint applies, what the practitioner or team is responsible for checking, how to reach a decision, and what to do when a checkpoint is not passed.

The checkpoints are not procedural formalities. They are the points in the workflow where human judgement is required and cannot be delegated to AI. Without them, the connection between human accountability and AI-assisted output is lost.

This document should be read alongside `master-workflow.md`, which explains how the checkpoints fit into the six lifecycle stages.

---

## Overview of the five checkpoints

| Checkpoint | Purpose | Decision question | When it applies |
|---|---|---|---|
| Direction | Establish the task before AI-assisted work begins | Is the brief ready? | Mandatory — every task |
| Alignment | Verify that AI output follows the intended direction | Continue, redirect, or revise? | Mandatory — at least one check; scales with complexity |
| Quality | Evaluate content against requirements and standards | Does it meet the acceptance criteria? | Mandatory — every deliverable |
| Localisation | Validate language, terminology, meaning, and cultural suitability | Is this locale-ready? | Conditional — multilingual tasks only |
| Final approval | Review and approve the complete deliverable | Is this approved for use? | Mandatory — every deliverable |

---

## Mandatory and conditional checkpoints

**Mandatory checkpoints** apply to every AI-assisted content task.

- **Direction** must be established before any AI-assisted activity begins.
- **Quality** review must be completed before a deliverable is considered ready.
- **Final approval** must be given by an accountable person before any deliverable is treated as complete.

There are no exceptions to these three requirements. No AI-generated assessment substitutes for them.

**Alignment** is required whenever AI contributes to a task's intermediate content, analysis, or recommendations. At minimum, one alignment check must take place before AI-assisted work advances to the next stage. Additional checks are appropriate when the brief is complex, the content is high-risk, or the task involves multiple contributors.

**Localisation** applies whenever content is being prepared for a language or cultural context other than the source. It is applied once per locale, not once per task. A task producing content in four languages requires four localisation checkpoints.

---

## Checkpoint definitions

### Direction

**Purpose**

Establish the task objectives, audience, context, and constraints before AI-assisted work begins.

**When it applies**

Before any AI-assisted activity in a task. For multi-stage tasks, Direction is confirmed at the start and revisited if requirements change significantly during the work.

**What to check**

- Are the task objectives defined and agreed?
- Is the target audience identified?
- Is the content context understood — what it is for, where it will appear, who will use it?
- Are the constraints clear: scope, format, length, language, compliance requirements?
- Are the relevant voice, tone, and content standards identified?

The Direction checkpoint is established through the content brief. AI may assist with organising information or structuring a draft brief, but the practitioner or content lead remains responsible for defining, validating, and approving the task direction. AI-assisted activities must work within that human-defined direction.

**Decision: Is the brief ready?**

| Outcome | Action |
|---|---|
| Brief is complete | Proceed to AI-assisted activities |
| Brief has gaps | Complete the missing elements before proceeding |

**What happens if the checkpoint is not passed**

Work does not proceed until the brief is established. Beginning AI-assisted activities without a defined direction produces outputs that cannot be reliably evaluated — they may appear to meet requirements that have not yet been defined.

---

### Alignment

**Purpose**

Confirm that AI output is following the intended direction before the work advances.

**When it applies**

After AI-assisted activities that produce intermediate outputs — including generation, analysis, synthesis, ideation, or review — before those outputs move to the next stage or activity. At minimum, one alignment check per task. Additional checks are added for complex tasks, high-risk content, or multi-stage deliverables.

**What to check**

- Does the output address the stated objective?
- Is it consistent with the established content brief and requirements?
- Does it follow the relevant voice, tone, and content standards?
- Are there signs that the AI has introduced assumptions, generalisations, or content not grounded in the supplied context?

**Decision: Continue, redirect, or revise?**

| Outcome | Action |
|---|---|
| Output meets requirements | Proceed to the next stage or activity |
| Output has recoverable issues | Revise at the current stage — re-prompt or edit |
| Output reflects a direction problem | Return to an earlier stage — revise the brief, the approach, or the supporting information |

**What happens if the checkpoint is not passed**

Work does not advance until the alignment issue is resolved. If the problem is a wording or quality issue, it can be corrected at the current stage. If the problem reflects a misalignment with the brief or a gap in the direction, it must be resolved by revising the brief before continuing. Document significant misalignments in the Decision and iteration log.

---

### Quality

**Purpose**

Evaluate content against requirements, voice guidelines, content standards, and applicable accessibility and compliance requirements.

**When it applies**

Before a deliverable proceeds to stage 05 (Localisation and adaptation) or stage 06 (Delivery and maintenance). The Quality checkpoint is the final structured evaluation before localisation or delivery.

**What to check**

The specific checks depend on the content type, but a quality review covers:

- **Requirements:** Does the content address its stated objective and meet the brief?
- **Voice and tone:** Does it reflect the product or brand voice? Is the tone appropriate for the audience and context?
- **Content standards:** Does it follow the applicable Rules, Recommendations, and Contextual guidance in the AI Content Creation module?
- **Accessibility:** Does it meet applicable accessibility requirements — plain language, reading level, label clarity, error message completeness?
- **Consistency:** Is it internally consistent? Is it consistent with related content?
- **Accuracy:** Is factual or technical content accurate and verifiable?

AI can assist with specific quality checks — voice alignment, consistency scans, accessibility flag review — but the practitioner evaluates the findings and makes the editorial decisions. See [AI assessments and human decisions](#ai-assessments-and-human-decisions).

**Decision: Does it meet the acceptance criteria?**

| Outcome | Action |
|---|---|
| Content meets all criteria | Proceed to stage 05 (if multilingual) or stage 06 |
| Content has specific, correctable issues | Revise at stage 04; re-check after revision |
| Content has a fundamental quality problem | Return to stage 03 or earlier — revise the content or the brief |

**What happens if the checkpoint is not passed**

Content does not proceed to stage 05 or stage 06 until quality criteria are met. Document the specific finding and the action taken in the Decision and iteration log.

Mandatory acceptance criteria must be met before content proceeds. Minor, non-blocking issues may be considered for an explicitly documented exception during Final approval; this does not waive any mandatory requirement.

---

### Localisation

**Purpose**

Validate language accuracy, terminology, meaning, and cultural suitability before approving content for a specific locale.

**When it applies**

For every locale in a multilingual task, after AI-assisted translation or adaptation and before the locale version is approved for delivery. This checkpoint does not apply to single-language tasks.

**What to check**

- **Language accuracy:** Is the translation accurate? Does it preserve the meaning of the source content?
- **Terminology:** Does it use the approved terminology for the locale?
- **Cultural suitability:** Is the content appropriate for the cultural context of the target audience?
- **Locale requirements:** Does it meet any locale-specific content requirements — date formats, units, legal conventions, reading conventions?
- **Consistency with source:** Does it maintain the intent, tone, and structure of the quality-reviewed source content?

This checkpoint requires a qualified reviewer: someone with the linguistic competence and cultural knowledge to evaluate the content for the specific locale. AI translation output must not be treated as approved without this review.

**Decision: Is this locale-ready?**

| Outcome | Action |
|---|---|
| Locale version meets all criteria | Approve the locale; document in the locale review record |
| Locale version has correctable issues | Revise the locale version; re-check before approving |
| Locale issues reflect a source content problem | Return to stage 04 to correct the source before continuing with localisation |

**What happens if the checkpoint is not passed**

The locale version does not proceed to stage 06 until localisation criteria are met. If the finding is a source content problem rather than a translation problem, work returns to stage 04 before localisation continues. Document locale-specific findings and decisions in the Decision and iteration log.

---

### Final approval

**Purpose**

Review and approve the complete deliverable before it is considered ready for use.

**When it applies**

Before any deliverable is treated as complete. This checkpoint is mandatory for every deliverable — there are no exceptions.

**What to check**

Final approval is a holistic review, not a re-run of earlier checks. The approver confirms that:

- All required quality checks have been completed and documented.
- All required locale approvals are in place for multilingual deliverables.
- Any outstanding issues have been resolved or recorded with an accepted rationale.
- The content meets its stated objectives.
- The Final approval checklist has been completed.

**Decision: Is this approved for use?**

| Outcome | Action |
|---|---|
| Deliverable meets all criteria | Approve; complete the Final approval checklist; proceed to handoff |
| Deliverable has outstanding issues | Document specific issues; return to the appropriate stage for revision |
| Deliverable is approved with recorded exceptions | Approve with documented rationale; note any accepted exceptions explicitly |

Approval with recorded exceptions is appropriate only for minor, non-blocking issues that the accountable approver has explicitly assessed and accepted. It must not be used to bypass unmet mandatory requirements, unresolved material accuracy problems, or applicable accessibility, legal, safety, or compliance requirements. Each exception must include its rationale and, where relevant, an owner and follow-up action.

**What happens if the checkpoint is not passed**

The deliverable is not handed off or published. The specific issues preventing approval must be documented, addressed, and re-reviewed before the checkpoint can be completed. Passing earlier checkpoints does not constitute final approval.

---

## Responsibility matrix

This matrix identifies who performs each checkpoint in individual and team workflows. In team workflows, the "performs" column indicates who carries out the review activity; the "decides" column indicates who is accountable for the outcome.

| Checkpoint | Individual workflow | Team workflow — performs | Team workflow — decides |
|---|---|---|---|
| Direction | Practitioner | Content lead | Content lead |
| Alignment | Practitioner | Content lead or reviewer | Content lead |
| Quality | Practitioner | Reviewer | Content lead |
| Localisation | Practitioner, if qualified for the target locale; otherwise, a qualified reviewer | Localisation reviewer | Localisation reviewer |
| Final approval | Practitioner | Designated approver | Designated approver |

**Notes on the matrix**

In individual work, the practitioner holds all responsibilities. The Direction, Alignment, and Quality checkpoints remain meaningful even when one person performs them all. Deliberately separate content generation from evaluation; returning to the output with fresh perspective makes the review more effective.

In team workflows, roles may be combined when team size requires it. The minimum requirement is that an identifiable person is responsible for each checkpoint decision. Accountability must remain clear even when responsibilities are shared.

For the Localisation checkpoint, linguistic and cultural competence in the specific locale is required, regardless of team size. The practitioner may serve as the qualified reviewer if they have that competence; an external reviewer is not automatically required. If a qualified reviewer is not available within the team, one must be sourced before the locale version is approved. The checkpoint is applied once per locale, but review and revision may repeat within that locale until it passes.

For the Final approval checkpoint, the approver must conduct a deliberate review against the approval criteria. Where practical, the approver should not be the same person who generated the content being approved. If roles must be combined, the review must be conducted as a distinct, considered activity — not as a confirmation that earlier stages are complete. Higher-risk content may require an independent specialist or additional reviewer.

---

## AI assessments and human decisions

AI can support several checkpoint activities: generating consistency checks, flagging potential voice misalignments, running accessibility scans, checking terminology, or summarising review findings. These outputs are inputs to the human's decision — not decisions in themselves.

The distinction applies at every checkpoint.

| AI can contribute | Human must decide |
|---|---|
| Flag potential quality issues | Whether the flagged issue is a genuine problem |
| Check for consistency against supplied guidelines | Whether the inconsistency is substantive or acceptable |
| Identify potential terminology mismatches in translation | Whether the terminology choice is correct for the locale |
| Summarise changes between versions | Whether the changes reflect the intended revision |
| Generate a draft approval summary | Whether the deliverable actually meets the criteria |

**When AI flags an issue**

Evaluate whether the flagged item is a genuine problem in context. Do not assume that identifying some issues means identifying all of them. Scan for problems the AI may have missed. Record substantive findings and decisions in the Decision and iteration log.

**When AI identifies no issues**

Conduct your own review. AI may miss context-dependent problems, subtle voice mismatches, or issues that require domain knowledge or editorial judgement. A clean AI assessment supports, but does not replace, the practitioner's review.

**The underlying principle**

No AI-generated assessment constitutes a passed checkpoint. Responsibility for content quality and accuracy remains with the practitioner or team. This does not change when AI is used in the review process.

---

## Supporting resources

| Resource | Purpose |
|---|---|
| `master-workflow.md` | The complete lifecycle, stage transitions, and operating modes |
| `localisation-workflow.md` | Detailed operational process for the Localisation checkpoint |
| `templates/content-brief-template.md` | Establish the Direction checkpoint |
| `templates/decision-and-iteration-log.md` | Document alignment findings, quality decisions, and returns |
| `templates/final-approval-checklist.md` | Complete the Final approval checkpoint |
| `03-ai-content-creation/output-evaluation-rubric.md` | Evaluation criteria for the Quality checkpoint |
| `03-ai-content-creation/failure-modes.md` | Common AI-assisted content problems relevant to Quality and Alignment checkpoints |
