# Stage 03 — Content Creation

Develop content based on the confirmed brief and requirements.

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

Stage 03 produces draft content from the confirmed brief. Its purpose is to develop content that addresses the stated objectives, serves the target audience, and meets the applicable requirements — in a form ready for structured review and refinement at stage 04.

This is the stage where AI-assisted generation is most directly applied. The practitioner uses the confirmed brief to ground AI activities, evaluates the outputs produced, and builds toward a draft that is ready for review. The output of this stage is not a finished product; it is a practitioner-reviewed draft that meets the brief well enough to benefit from the structured quality review at stage 04.

**The brief as the governing document**

The content brief confirmed at stage 02 is the controlling reference for all creation activities. Generation prompts are grounded in it; outputs are evaluated against it; decisions are traceable to it. If creation activities reveal that the brief is incomplete or needs revision, the work returns to stage 02 before creation continues. Stage 03 must not resolve brief ambiguities through editorial or content choices. The ambiguity should be documented and referred back to stage 02 for resolution.

**Scope of AI assistance**

Stage 03 involves AI-assisted drafting, restructuring, adaptation, and alternative generation. The practitioner directs these activities by supplying context, reviewing outputs, making editorial decisions, and guiding further generation based on those decisions. AI assists the creation process; it does not drive it.

---

## 2. When to use AI

**AI assistance is appropriate when:**

- Generating a first draft from a confirmed brief, structure, and relevant context
- Producing alternative formulations of specific content elements — labels, headings, calls to action, error messages, instructions — for the practitioner to evaluate
- Restructuring existing content for a different format, length, or audience
- Adapting a draft to better align with voice and tone guidelines after initial generation
- Generating placeholder or scaffold content for sections not yet drafted
- Identifying inconsistencies in structure, labelling, or terminology within a draft

**AI assistance is not appropriate when:**

- Beginning content generation before the brief is confirmed and grounded context is prepared
- Using AI to resolve ambiguities in the brief through content choices, rather than returning to stage 02
- Accepting a first-pass draft as complete without evaluating it against the brief and requirements
- Treating AI-generated phrasing as the practitioner's editorial voice without review and adaptation

**A note on prompt grounding and generation quality**

The quality of AI-generated content is directly affected by the quality of the context and instructions provided. A prompt that supplies the confirmed brief, target audience, voice and tone requirements, and applicable standards will produce more usable output than one that does not. Undirected generation — asking AI to "write content about X" without grounding — produces drafts that require extensive reworking and often do not reflect the brief.

Prepare grounding materials before generating. See [`grounding-guide.md`](../../03-ai-content-creation/grounding-guide.md) for guidance on what to include and how to structure it.

---

## 3. Required human inputs

The following must be in place before AI-assisted generation begins.

**Confirmed content brief**

The content brief confirmed at stage 02 is the foundation for all creation activities. It must be complete, confirmed by the responsible practitioner, and available to inform generation prompts. If the brief has documented assumptions or outstanding questions, these should be resolved or explicitly managed before creation begins.

**Content structure or outline**

The content structure confirmed at stage 02 provides the scaffold for creation. Each section or element of the structure should have a clear purpose traceable to the brief. If the structure is incomplete, creation will produce fragments rather than a coherent draft.

**Voice, tone, and content standards**

The practitioner must know which voice and tone guidelines, content standards, and applicable rules apply to this content. These are the basis for evaluating AI-generated outputs and deciding which to keep, adapt, or discard. Mandatory requirements must be met; recommendations and contextual guidance inform editorial decisions.

**Grounding materials**

Before AI-assisted generation begins, the practitioner prepares the relevant context for use in generation prompts. This may include selected information from the confirmed brief and content structure, applicable voice and tone guidance, approved reference examples, terminology, source material, and task-specific constraints. The brief remains the governing document; grounding materials are the task-specific information assembled to help AI work within its requirements. They should not introduce requirements or assumptions that conflict with the brief.

**Criteria for a draft ready to proceed**

The practitioner should know what "ready for stage 04" looks like for this task: what level of completeness is needed, what quality issues are expected to be resolved at stage 04, and what would make the draft unsuitable for review. This prevents both premature handoff (sending work to review before it is substantively complete) and over-investment (attempting to fully polish content at a stage designed to produce a draft).

---

## 4. AI-assisted activities

**Generating a first draft**

Given a confirmed brief, structure, and grounding materials, AI can produce an initial draft. The practitioner reviews this draft against the brief and requirements, identifies what works and what needs revision, and uses that assessment to guide further generation or direct editing.

*Illustrative example: A practitioner preparing a set of short instructional messages supplies AI with the confirmed brief, the purpose and context of each message, the applicable voice guidelines, and approved reference examples. AI generates an initial set. The practitioner reviews each message for accuracy, voice alignment, and length, then revises unsuitable content or provides more specific instructions for another generation attempt.*

**Generating alternatives**

For specific content elements where multiple approaches could work — a label, an error message, a section heading — AI can generate a set of alternatives for the practitioner to evaluate. This is particularly useful when no single first-pass option is satisfactory, or when the practitioner wants to compare formulations before deciding.

Alternatives are for evaluation, not for selection by default. The practitioner assesses each option against the brief and requirements, selects one, and documents the decision where relevant.

**Restructuring and adaptation**

AI can restructure existing content for a different format or length, adapt tone for a different audience segment, or reframe content that is not meeting its stated objective. The practitioner supplies the source content, the target requirements, and the specific transformation needed. The adapted output is reviewed against the same criteria as new-generation work.

**Consistency checking within a draft**

AI can flag inconsistencies in terminology, labelling, structure, or voice within a developing draft. The practitioner evaluates whether the flagged inconsistency is genuine and decides how to address it. This activity is distinct from the structured quality review at stage 04; it supports the creation process, not the approval process.

---

## 5. Human responsibilities

**Directing generation**

The practitioner directs every AI-assisted generation activity: supplying the brief, the structure, and the grounding context; specifying what is needed; and guiding revision based on output assessment. AI does not independently decide what to generate or how.

**Evaluating every output against the brief**

Every AI-generated draft, section, alternative, or adaptation is evaluated by the practitioner before it is incorporated into the working draft. The evaluation is against the brief and applicable requirements — not against whether the output sounds well-written. Fluent AI output that does not meet the brief is not usable. See [`output-evaluation-rubric.md`](../../03-ai-content-creation/output-evaluation-rubric.md) for structured evaluation criteria.

**Making editorial decisions**

The practitioner decides which AI-generated content to keep, adapt, or discard. These are editorial decisions: they require judgement about whether the content serves its purpose, addresses the audience, reflects the product's voice, and meets applicable standards. AI cannot make these decisions.

Where AI produces content that is partly usable, the practitioner adapts it rather than accepting or rejecting it wholesale. The working draft may be a mix of AI-generated content, practitioner-edited content, and practitioner-written content — this is normal. What matters is that every element in the stage 03 draft has been reviewed and confirmed by the practitioner before it is handed over for structured review.

**Identifying when creation has stalled**

If repeated generation attempts are not producing content that meets the brief, the practitioner investigates the cause before continuing. Common causes include insufficient grounding context, an unclear or incomplete brief, or a mismatch between the stated objective and the content structure. These require resolution at the appropriate level: improve the grounding context where the brief remains valid; return to stage 02 when the brief, content structure, or selected approach needs revision; or reconsider the generation instructions when the task is sufficiently defined but the outputs remain unsuitable. Generating more content without addressing the cause is unlikely to resolve the problem.

**Deciding when the draft is ready for stage 04**

The practitioner confirms when the draft is complete enough for structured review. This is a judgement call, not a perfect-completion threshold. The draft should address the full brief, be internally coherent, and reflect the voice and tone requirements well enough for review to be productive. A draft sent to stage 04 with significant unresolved structural or content issues wastes review effort; a draft withheld from stage 04 until it is fully polished delays the feedback cycle unnecessarily.

---

## 6. Inputs and expected outputs

**Required inputs**

- Confirmed content brief from stage 02
- Confirmed content structure or outline from stage 02
- Voice, tone, and content standards applicable to the content
- Grounding materials prepared for AI-assisted generation
- Criteria for a draft ready to proceed to stage 04

**Expected outputs**

- Draft content that addresses the full brief
- Notes on significant editorial decisions or trade-offs, particularly where multiple options were considered
- Documented assumptions and non-blocking questions relevant to the review, with any unresolved issues that could affect the content clearly identified
- A practitioner-reviewed draft ready for structured quality review

Any issue that prevents reliable evaluation or materially affects the content must be resolved before handoff to stage 04; only non-blocking questions may be carried forward.

---

## 7. Checkpoints and decision criteria

### Direction checkpoint

Before generation begins, the practitioner confirms that the task, objectives, audience, context, and constraints are sufficiently defined in the confirmed brief and supporting materials. If these are incomplete or have changed, the work returns to stage 02 before generation proceeds.

### Alignment checkpoint

The Alignment checkpoint applies at stage 03. At minimum, one Alignment checkpoint must be completed before the draft proceeds to stage 04. Additional Alignment checks are appropriate for longer or more complex drafts, after each major content section is generated, or when generation is not producing content that meets the brief.

**What to check at each Alignment checkpoint:**

- Does the draft content address the stated objective in the brief?
- Is it consistent with the confirmed content structure?
- Does it reflect the applicable voice and tone requirements?
- Has AI introduced assumptions, generalisations, or content not grounded in the brief or supplied context?
- Is the draft free from significant content gaps that would make stage 04 review unproductive?

**Decision: Continue, redirect, or revise?**

| Outcome | Action |
|---|---|
| Draft meets requirements at this stage | Proceed — continue creation or proceed to stage 04 |
| Draft has recoverable issues in specific sections | Revise at stage 03 — re-prompt with more specific grounding, or edit directly |
| Draft has a consistent pattern of not meeting voice or brief requirements | Investigate grounding and prompt quality; adjust before continuing |
| Brief is insufficient to evaluate the draft against | Return to stage 02 — the brief must be resolved before creation can proceed |
| Confirmed structure or approach does not support the brief | Return to stage 02 — revise the structure or approach before continuing |

Alignment checks during creation do not replace the structured Quality checkpoint at stage 04. Stage 03 confirms that the developing draft remains aligned with the brief; stage 04 evaluates its quality against the applicable requirements.

**When to apply multiple Alignment checks**

A single Alignment check at the end of a short, single-element creation task is sufficient. For longer tasks — a multi-section guide, a set of related UI strings, a document with distinct sections — an Alignment check after each major section prevents compounding misalignment. If the first section is not meeting the brief, it is better to resolve this before generating the remaining sections.

---

## 8. Stage checklist

**Before generation begins**
- [ ] Direction checkpoint completed: task, objectives, audience, context, and constraints are sufficiently defined
- [ ] Confirmed brief is available and complete
- [ ] Content structure or outline is confirmed
- [ ] Voice, tone, and content standards are identified
- [ ] Grounding materials are prepared
- [ ] Criteria for a draft ready for stage 04 are established

**During creation**
- [ ] Generation prompts are grounded in the confirmed brief and context
- [ ] At least one Alignment checkpoint has been conducted
- [ ] AI-generated outputs have been evaluated against the brief and requirements before incorporation
- [ ] Editorial decisions have been made by the practitioner, not accepted by default from AI output

**Draft readiness**
- [ ] The draft addresses the full brief
- [ ] The draft is internally consistent in structure, terminology, and voice
- [ ] Significant editorial decisions and trade-offs are noted
- [ ] Documented assumptions or questions for stage 04 are recorded
- [ ] The practitioner has confirmed the draft is ready for structured review

---

## 9. Handoff to next stage

Before moving to stage 04 (Review and refinement), confirm the following are in place and documented.

**What to pass forward**

- The practitioner-reviewed draft
- The confirmed content brief from stage 02 (stage 04 evaluates the draft against this)
- The confirmed content structure or outline
- Notes on significant editorial decisions or trade-offs
- Documented assumptions and non-blocking questions relevant to the review, with any unresolved issues that could affect the content clearly identified
- The applicable voice, tone, and content standards the draft should be evaluated against
- Relevant source and reference materials used during creation, where needed to evaluate the draft

**What to record**

For tasks where AI-assisted generation required significant iteration or produced content that was substantially revised, note in `../templates/decision-and-iteration-log.md`:
- What was generated and what was kept, adapted, or discarded
- Significant decisions about voice, structure, or approach made during creation
- Recurring generation issues and how they were resolved

**Handoff template**

For collaborative tasks — where stage 04 will be carried out by a different reviewer — use `../templates/handoff-template.md` to transfer the draft and relevant context. The handoff should give the reviewer enough information to evaluate the draft effectively: the brief, the applicable standards, any decisions made during creation that affect what is or is not in the draft, and any known areas that may require particular attention at review.

---

## 10. Phase 4 references

The following resources from the AI Content Creation module (`03-ai-content-creation/`) are most heavily used at stage 03.

| Resource | Relevance to this stage |
|---|---|
| [`grounding-guide.md`](../../03-ai-content-creation/grounding-guide.md) | How to prepare grounding context before AI-assisted generation — directly applicable to every generation activity at this stage |
| [`prompt-templates/`](../../03-ai-content-creation/prompt-templates/) | Reusable prompt templates for common content creation tasks: drafting, reformulation, adaptation, and alternative generation |
| [`output-evaluation-rubric.md`](../../03-ai-content-creation/output-evaluation-rubric.md) | Structured evaluation criteria for assessing AI-generated drafts against the brief, voice guidelines, and content standards — applicable to Alignment checkpoint evaluation during creation |
| [`failure-modes.md`](../../03-ai-content-creation/failure-modes.md) | AI failure modes most relevant to content creation: voice drift, content that sounds complete but misses the brief, terminology inconsistency, overconfident assertions presented as facts |
| [`worked-examples.md`](../../03-ai-content-creation/worked-examples.md) | End-to-end examples of content creation with AI assistance, including evaluation and revision decisions |
