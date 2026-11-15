# Stage 05 — Localisation and Adaptation

Translate and adapt content for other languages and cultural contexts; validate each locale version before delivery.

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

Stage 05 adapts quality-reviewed source content for other languages and cultural contexts. Its purpose is to produce locale versions that are accurate, culturally appropriate, and aligned with the requirements of each target audience — and to validate each locale version before it proceeds to delivery.

**This stage is conditional.** It applies only to multilingual tasks. Single-language content proceeds directly from stage 04 (Review and refinement) to stage 06 (Delivery and maintenance). When stage 05 applies, work does not proceed to stage 06 until every required locale version has completed it.

**What this stage produces**

Stage 05 produces locale-approved versions of the source content — one for each target locale. Each locale version is a distinct content set. It has been adapted for its target audience, reviewed by someone with the appropriate language and cultural expertise, and approved against the locale acceptance criteria. These versions are the input to stage 06.

**Localisation as a distinct discipline**

Localisation is not translation alone. Effective localisation adapts content for a cultural context: adjusting register, reformulating idioms, applying locale-specific formatting conventions, and considering what a target audience needs to understand and act on the content in their context. The appropriateness of a locale version is not visible to someone who does not know the target language and culture.

AI-assisted translation can produce a useful starting point. It cannot produce a final locale version. Human review by a qualified locale reviewer is mandatory.

**Locale approval and final approval**

Locale approval is a distinct checkpoint from final approval. Locale approval confirms that a locale version meets the requirements for its target audience and context. It is carried out by the locale reviewer, who has the relevant language and cultural expertise. Final approval, at stage 06, authorises the deliverable for use; it is a separate decision carried out by the responsible approver.

---

## 2. When to use AI

**AI assistance is appropriate when:**

- Producing an initial translation draft as a starting point for human review and adaptation
- Checking terminology consistency across locale versions against an approved glossary
- Identifying content elements that may not localise directly — idioms, culturally specific references, structural patterns that do not carry across languages
- Flagging length or format differences that may affect layout or display in the target locale
- Generating alternative formulations for content elements that do not adapt well in translation
- Checking for internal consistency within a locale version: terminology, labelling, phrasing patterns

**AI assistance is not appropriate when:**

- Making cultural adaptation decisions — these require knowledge of the target culture and audience
- Deciding whether translated content is accurate or appropriate in context — accuracy and appropriateness require appropriate language proficiency, relevant domain knowledge, and familiarity with the target cultural context
- Carrying out or passing the Locale approval checkpoint — no AI assessment constitutes a passed locale review
- Adapting voice and tone for a cultural context without guidance from a locale specialist — register and formality conventions differ significantly across languages and cannot be reliably inferred
- Verifying locale-specific compliance, legal, or accessibility requirements — these require the appropriate expertise for the target locale

**A note on AI translation quality**

AI translation tools have improved substantially, but they produce drafts, not finished content. Common failure modes include: fluent but inaccurate translation; preservation of source-language structure in ways that read unnaturally in the target language; inconsistent terminology; and failure to adapt culturally specific content. See [`failure-modes.md`](../../03-ai-content-creation/failure-modes.md) for further detail on AI-assisted content failures that apply to translation and adaptation tasks.

An AI-generated translation should be treated as a first draft that requires evaluation against the same criteria as any other AI-generated content — not as a near-complete output that needs light editing.

---

## 3. Required human inputs

The following inputs or arrangements must be in place before localisation work begins for each locale.

**Quality-reviewed source content from stage 04**

The source content must have passed the Quality checkpoint at stage 04 before localisation begins. Localising content that has not been quality-reviewed risks producing locale versions that inherit source content problems, compounding them through translation. If the source content changes after localisation has begun, all in-progress locale versions must be reviewed for impact.

**Locale-specific requirements**

For each target locale, the following must be established before adaptation begins:
- Target audience description and context
- Voice and tone requirements for the target language and cultural context
- Format, length, and structural conventions for the locale
- Applicable accessibility, compliance, or legal requirements for the locale
- Locale acceptance criteria: what a locale version must meet to pass Locale approval, what constitutes a blocking finding, and how outstanding minor, non-blocking issues should be documented for consideration at Final approval. The locale reviewer does not accept outstanding issues as exceptions at the Locale approval checkpoint. All mandatory locale acceptance criteria must be met before the locale version can proceed.

**Approved glossary and reference materials**

An approved glossary of key terms in the target language, and any approved reference examples or style guidance for the locale. These are the basis for terminology consistency and adaptation decisions. If no glossary exists, one should be established before localisation begins; ad hoc terminology decisions in translation create inconsistencies that are difficult to correct retrospectively.

**A qualified locale reviewer**

Locale review must be carried out by someone with appropriate proficiency in the target language, relevant domain knowledge, and familiarity with the target cultural context. The locale reviewer is identified and confirmed before localisation work begins. AI cannot substitute for locale review.

---

## 4. AI-assisted activities

**Initial translation draft**

Given the quality-reviewed source content, an approved glossary, and relevant locale context, AI can produce an initial translation as a starting point for human review and adaptation. The practitioner should supply grounding materials specifying the approved terminology, voice and tone requirements, and any locale-specific constraints before generating the draft.

The initial draft is for review, not delivery. The locale reviewer assesses it against the source content, the locale requirements, and the approved glossary, and identifies what needs to be adapted, corrected, or rewritten.

*Illustrative example: A practitioner preparing onboarding content for a new locale supplies AI with the confirmed source content, the approved glossary for the target language, and a summary of the voice and tone requirements. AI generates an initial translation. The locale reviewer reads through it, marks passages that require cultural adaptation or terminology correction, and rewrites them directly — treating the AI-generated draft as a scaffold, not a near-complete output.*

**Terminology and consistency checking**

AI can check a translated draft against an approved glossary — flagging terms that differ from approved usage — and check for consistency within the locale version. The locale reviewer evaluates each flagged item and determines whether it is a genuine inconsistency or an intentional variation given context.

**Localisation issue identification**

AI can flag content elements that may not localise directly: idioms, culturally specific references, structures that are natural in the source language but awkward in the target language, or phrasing patterns that carry different connotations across cultures. These are candidates for adaptation; the locale reviewer determines what adaptation is needed.

**Format and length checking**

AI can identify where translated content differs significantly in length or structure from the source — a relevant consideration when content must fit defined space constraints or layout specifications. The practitioner confirms whether format adjustments are needed.

**Alternative generation**

Where a specific passage does not adapt well in translation, AI can generate alternative formulations for the locale reviewer to evaluate. As with content creation at stage 03, alternatives are for evaluation, not for acceptance by default.

---

## 5. Human responsibilities

**Directing the localisation process**

The practitioner oversees the localisation process for each locale: preparing grounding materials for AI-assisted translation, ensuring locale requirements are established, coordinating locale review, and managing the progression from initial draft to locale-approved version.

**The seven-step localisation process**

Stage 05 is most reliably carried out as a structured sequence:

1. **Confirm the source content is ready.** Verify that stage 04 is complete and the source content has passed Quality review before localisation begins.
2. **Establish locale requirements.** Confirm the target audience, voice and tone requirements, format conventions, applicable compliance or accessibility requirements, and locale acceptance criteria for each locale.
3. **Prepare grounding materials.** Assemble the approved glossary, reference examples, and locale-specific constraints to be used in AI-assisted translation and during review.
4. **Produce the initial translation draft.** Use AI-assisted translation grounded in the established locale requirements and glossary, or brief a human translator using the same materials.
5. **Review and adapt the draft.** The locale reviewer reads the draft against the source content and locale requirements, identifies issues, and makes the necessary adaptations — rewriting, correcting terminology, and adjusting cultural register as needed.
6. **Conduct locale review.** The locale reviewer performs a structured assessment against the locale acceptance criteria. This is the substantive evaluation that determines whether the locale version meets requirements.
7. **Locale approval decision.** The locale reviewer confirms that the locale version meets the acceptance criteria and approves it to proceed to stage 06. If it does not meet the criteria, the version returns to step 5 for further adaptation.

**Evaluating AI-generated translation**

The locale reviewer evaluates every AI-generated translation independently — not by correcting it toward acceptable, but by assessing whether it accurately and appropriately conveys the source content in the target language and cultural context. A translation that requires substantial rewriting is not close enough; it should be used as a structural scaffold only, with the locale reviewer writing the final version.

**Making cultural adaptation decisions**

Cultural adaptation decisions require knowledge of the target audience, cultural context, and language that the practitioner may not have. Where the practitioner is not the locale reviewer, these decisions rest with the locale reviewer. The practitioner ensures the locale reviewer has the information they need: the confirmed brief, the source content, the locale requirements, and the grounding materials.

**Locale approval**

The Locale approval checkpoint is passed when the locale reviewer confirms that the locale version meets the acceptance criteria for the target locale. This is a checkpoint with real authority: a locale version that does not pass Locale approval does not proceed to stage 06, regardless of how close it appears to be.

**Managing multiple locales**

Where content is being localised for more than one locale simultaneously, each locale version is treated as an independent content set. Decisions made for one locale do not automatically apply to others; each has its own requirements, reviewer, and approval. The practitioner tracks the progress of each locale version separately and does not proceed to stage 06 until all required locales have passed Locale approval.

**Source content changes during localisation**

If the source content is revised after localisation has begun, the practitioner assesses the impact on every locale version based on the previous source version, including versions that have already passed Locale approval but have not yet received Final approval. Changes to the source content may require corresponding changes to some or all locale versions. Affected versions must undergo the necessary review again before proceeding to stage 06.

---

## 6. Inputs and expected outputs

**Required inputs**

- Quality-reviewed source content from stage 04
- Locale-specific requirements for each target locale: audience, voice and tone, format conventions, compliance or accessibility requirements, acceptance criteria
- Approved glossary and reference materials for each target language
- Qualified locale reviewer for each locale

**Expected outputs**

- Locale-approved translated and adapted content for each target locale
- Documented review findings and adaptation decisions for each locale version
- Change log recording significant adaptations made and the reason for each
- Notes on any outstanding issues for consideration at Final approval
- Locale-approved content ready to proceed to stage 06

Mandatory locale acceptance criteria must be met for each locale before that locale version proceeds to stage 06. Outstanding non-blocking issues that remain unresolved should be documented with their rationale for consideration at Final approval.

---

## 7. Checkpoints and decision criteria

### Alignment checkpoint

An Alignment checkpoint applies during adaptation, before the locale version is submitted for formal Locale review. At minimum, one Alignment check should be completed on the initial draft for each locale.

**What to check:**

- Does the translated content accurately convey the meaning of the source content?
- Has the approved glossary been applied consistently?
- Has the content been adapted for the target cultural context, not merely translated word for word?
- Are the voice and tone requirements for the target locale reflected?
- Are there format or length issues that need to be resolved before formal review?

### Locale approval checkpoint

The Locale approval checkpoint is mandatory for each locale version. It is carried out by the locale reviewer, who confirms that the locale version meets the acceptance criteria for the target locale.

**What to check:**

- **Accuracy:** Does the content accurately convey the meaning and intent of the source content in the target language?
- **Cultural appropriateness:** Is the content appropriate for the target cultural context — register, formality, idiomatic usage, culturally specific references?
- **Voice and tone:** Does it reflect the voice and tone requirements for the target locale?
- **Terminology:** Is approved terminology applied consistently throughout?
- **Format and conventions:** Does it follow the applicable format and typographic conventions for the target locale?
- **Compliance and accessibility:** Does it meet any locale-specific compliance, legal, or accessibility requirements?

**Decision: Does the locale version meet the acceptance criteria?**

| Outcome | Action |
|---|---|
| Locale version meets all acceptance criteria | Proceed to stage 06 for this locale |
| Locale version has specific, correctable issues | Return to adaptation (step 5); re-review after correction |
| Locale version has fundamental translation or adaptation problems | Return to adaptation (step 5) for substantial revision; locale reviewer to specify what must change |
| Locale version has outstanding non-blocking issues | Document with rationale for consideration at Final approval; proceed only if all mandatory criteria are met |
| Locale review identifies a source content problem | The source content issue must be resolved at stage 04 before the locale version can be completed; other locales in progress must also be assessed for impact |

**What happens if locale acceptance criteria are not met**

A locale version that does not meet mandatory acceptance criteria does not proceed to stage 06. Document the specific finding and the action taken in [`../templates/decision-and-iteration-log.md`](../templates/decision-and-iteration-log.md).

Locale approval is not the same as final approval. It confirms that a locale version meets the requirements for its target audience and context. Final approval, at stage 06, is a separate decision.

---

## 8. Stage checklist

**Before localisation begins (per locale)**
- [ ] Source content has passed Quality review at stage 04
- [ ] Locale-specific requirements are established: audience, voice and tone, format conventions, acceptance criteria
- [ ] Approved glossary and reference materials are available
- [ ] Qualified locale reviewer is identified and confirmed
- [ ] Grounding materials for AI-assisted translation are prepared

**During adaptation (per locale)**
- [ ] Initial translation draft has been reviewed against the source content and locale requirements
- [ ] Approved terminology has been applied and checked
- [ ] Cultural adaptation decisions have been made by the locale reviewer
- [ ] An Alignment check has been completed before formal locale review

**Locale approval decision (per locale)**
- [ ] Locale version has been reviewed against all acceptance criteria by the qualified locale reviewer
- [ ] Mandatory acceptance criteria are met
- [ ] Outstanding non-blocking issues are documented for consideration at Final approval
- [ ] Locale reviewer has confirmed the version is ready to proceed
- [ ] Adaptation decisions and significant findings are recorded

---

## 9. Handoff to next stage

Stage 05 produces locale-approved versions for each target locale. These proceed to stage 06 (Delivery and maintenance), where Final approval is given and the content is handed off for use.

**What to pass forward (per locale)**

- Locale-approved content
- The confirmed content brief and locale-specific requirements
- Review findings and change log from stage 05
- Notes on any outstanding non-blocking issues and their rationale, for consideration at Final approval
- Confirmation that Locale approval has been completed for this locale version
- The source-content version on which the locale version is based, so stage 06 can confirm alignment if the source has been revised

**What to record**

Document in [`../templates/decision-and-iteration-log.md`](../templates/decision-and-iteration-log.md):
- Significant adaptation decisions for each locale and the reason for each
- Changes made in response to locale review findings
- Returns to adaptation and why
- Any source content issues identified during localisation and how they were handled
- Outstanding non-blocking issues and their rationale, for consideration at Final approval

**Handoff template**

For collaborative tasks — where stage 06 will be carried out by a different contributor — use [`../templates/handoff-template.md`](../templates/handoff-template.md) to transfer each locale version and its context. The handoff should confirm that Locale approval has been completed for each locale version and note any outstanding non-blocking issues documented for consideration at Final approval.

---

## 10. Phase 4 references

The following resources from the AI Content Creation module (`03-ai-content-creation/`) are most directly relevant to stage 05.

| Resource | Relevance to this stage |
|---|---|
| [`grounding-guide.md`](../../03-ai-content-creation/grounding-guide.md) | How to prepare grounding materials before AI-assisted translation — specifying the approved glossary, voice and tone requirements, and locale constraints; the same grounding principles apply to translation prompts as to content creation prompts |
| [`failure-modes.md`](../../03-ai-content-creation/failure-modes.md) | AI failure modes relevant to translation and adaptation: fluent but inaccurate translation, source-language structural carryover, inconsistent terminology, failure to adapt culturally specific content |
| [`output-evaluation-rubric.md`](../../03-ai-content-creation/output-evaluation-rubric.md) | Evaluation criteria applicable when assessing AI-generated translation drafts against source content, locale requirements, and approved terminology |
| [`prompt-templates/`](../../03-ai-content-creation/prompt-templates/) | Prompt templates for AI-assisted translation, terminology consistency checks, and localisation issue identification |
| [`ai-content-principles.md`](../../03-ai-content-creation/ai-content-principles.md) | Foundational principles for AI-assisted content work — particularly the distinction between AI-generated output and human editorial decisions, which applies equally to translation and to original content |
