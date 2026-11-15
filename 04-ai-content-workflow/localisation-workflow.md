# Localisation Workflow

Operational guidance for translating and adapting content for other languages and cultural contexts.

## Contents

- [1. Purpose and relationship to Stage 05](#1-purpose-and-relationship-to-stage-05)
- [2. When localisation applies](#2-when-localisation-applies)
- [3. Writing source content that localises well](#3-writing-source-content-that-localises-well)
- [4. The seven-step localisation process](#4-the-seven-step-localisation-process)
- [5. AI-assisted translation](#5-ai-assisted-translation)
- [6. Briefing a locale reviewer](#6-briefing-a-locale-reviewer)
- [7. Managing multiple locales](#7-managing-multiple-locales)
- [8. Source content changes during localisation](#8-source-content-changes-during-localisation)
- [9. References](#9-references)

---

## 1. Purpose and relationship to Stage 05

This document provides operational guidance for the localisation process. It is a companion to Stage 05 (Localisation and adaptation), which covers localisation within the AI Content Workflow lifecycle — when it applies, what checkpoints govern it, and how it connects to the stages before and after it.

This document focuses on the practical detail: how to prepare for localisation, how to use AI-assisted translation effectively, how to brief a locale reviewer, and how to manage common localisation scenarios. It is intended for practitioners who are running localisation for the first time, managing a complex multilingual task, or who need a reference for specific aspects of the process.

**Where to start**

If you have not read Stage 05, start there. It establishes the conditions under which localisation applies, the required inputs, the Locale approval checkpoint, and the role of localisation within the full content lifecycle. This document assumes that context.

---

## 2. When localisation applies

Localisation applies when content is intended for audiences in more than one language or cultural context. The practitioner confirms which locales are in scope at stage 02 (Ideation and planning), where this affects content structure and format decisions for the source content.

**Criteria for a task requiring localisation:**

- The content will be published, distributed, or implemented in more than one language
- The content will be used by audiences in cultural contexts where direct translation is insufficient — where register, formality, idiom, or cultural reference must be adapted
- Regulatory, accessibility, or compliance requirements differ by locale

**Single-language tasks do not go through Stage 05.** A task that serves one language and cultural context proceeds from stage 04 directly to stage 06.

**Localisation scope should be established early.** Knowing that a task requires localisation affects how source content is written (see Section 3), the resources required, and the overall timeline. Discovering a localisation requirement at stage 04 or later creates avoidable rework.

---

## 3. Writing source content that localises well

Localisation is significantly easier when source content is written with it in mind. Source content that localises well tends to:

**Use plain, direct language**

Idiomatic expressions, colloquialisms, and culture-specific references are difficult to adapt and often have no direct equivalent in other languages. Plain, direct language produces more reliable translations and requires less adaptation.

*Example: "We'll keep you in the loop" requires cultural interpretation in translation. "We will send you updates as they become available" translates more directly.*

**Prefer active voice and clear sentence structure**

Complex nested sentences and passive constructions are harder to translate without changing meaning. Short sentences with clear subject-verb-object structure give translators less room for ambiguity.

**Avoid figurative language and metaphor**

Metaphors and figurative language are often culturally embedded and may not carry across languages directly; they often require cultural adaptation rather than literal translation. Where the source content uses them, assess whether they require adaptation — this requires cultural knowledge and judgement that may not always be available. Use them intentionally, and flag them for the locale reviewer's attention.

**Maintain consistent terminology**

Consistent terminology in the source content is essential for consistent translation. Terminology that varies without reason in the source will produce inconsistent translations that require additional reconciliation. Build the approved glossary before or alongside source content creation.

**Avoid embedded text in images**

Text embedded in images, diagrams, or screenshots cannot be translated without recreating the visual asset. If localisation is in scope, avoid embedding content that must change per locale, or plan for asset recreation as part of the localisation process.

**Note locale-specific decisions for the content brief**

If the source content contains elements that will need locale-specific adaptation — a legal notice, a date format, a culturally specific example — flag these in the content brief. The locale reviewer needs to know what requires adaptation and why.

---

## 4. The seven-step localisation process

The following process applies to each locale version of the content.

### Step 1: Confirm source content readiness

Before localisation begins for any locale, confirm:

- Stage 04 (Review and refinement) is complete and the source content has passed Quality review
- Any changes to the source content after quality review are assessed for impact on locale versions already in progress (see Section 8)
- The source version on which localisation is based is recorded, so locale versions can be traced to a specific source

Do not begin localisation on content that has not completed Quality review. Errors or structural problems in the source content are compounded in translation.

### Step 2: Establish locale requirements

For each target locale, confirm the following before adaptation begins:

- **Target audience:** Who will use this content in this locale? What is their context, knowledge level, and expected relationship with the product or service?
- **Voice and tone:** What are the voice and tone requirements for this language and cultural context? Register and formality conventions differ significantly across languages; a voice that feels appropriate in English may read as too formal, too casual, or inappropriate in another language.
- **Format and typographic conventions:** Does the locale have specific requirements for dates, numbers, currency, punctuation, quotation marks, or spacing? Are there right-to-left (RTL) layout considerations?
- **Compliance and accessibility requirements:** Do applicable legal, regulatory, or accessibility requirements differ for this locale?
- **Locale acceptance criteria:** What must the locale version meet to pass Locale approval? What constitutes a blocking finding, and how will outstanding non-blocking issues be handled?

### Step 3: Prepare grounding materials

Before AI-assisted translation or briefing a human translator, prepare:

- The approved glossary for the target language (see Section 5 for guidance on what to include)
- Voice and tone guidelines for the locale, including any approved reference examples in the target language
- Notes on content elements requiring cultural adaptation, flagged from the source content brief
- Format and typographic conventions for the locale
- The scope and constraints established in step 2

Grounding materials make translation and adaptation more consistent and reduce the volume of corrections needed during locale review. See [`grounding-guide.md`](../03-ai-content-creation/grounding-guide.md) for further guidance on preparing grounding context for AI-assisted activities.

### Step 4: Produce the initial translation draft

The initial translation draft may be produced using AI-assisted translation, a human translator, or the locale reviewer themselves for smaller tasks where they are doing both translation and review.

**AI-assisted translation:** See Section 5 for detailed guidance. Provide AI with the source content, approved glossary, voice and tone requirements, and locale-specific constraints. Review the output before passing it to the locale reviewer. AI translation is a scaffold; it must be evaluated, not accepted.

**Human translator:** Brief the translator using the materials prepared in step 3. The translator should have the approved glossary, voice and tone requirements, and notes on elements requiring cultural adaptation. The translated draft then proceeds to locale review.

**Locale reviewer as translator:** For smaller tasks or tasks where the locale reviewer has the capacity, they may produce the initial translation directly. Where this happens, a separate qualified practitioner must take responsibility for steps 5–7: reviewing and adapting the draft, conducting the substantive locale assessment, and making the Locale approval decision. The person who produced the translation cannot assess their own work at the Locale approval checkpoint. If a separate qualified reviewer is not available, arrange one before localisation begins — not after the draft is complete.

### Step 5: Review and adapt the draft

The locale reviewer reads the initial draft against the source content and locale requirements, and makes the necessary adaptations:

- Correcting translation inaccuracies
- Applying approved terminology from the glossary
- Adapting register, formality, and idiomatic usage for the target cultural context
- Reformulating content elements that do not carry across languages
- Adjusting format or typographic conventions where needed

The goal of this step is a draft that is accurate, appropriate, and consistent with the locale requirements. The locale reviewer should be working from the source content and locale requirements — not from their impression of what the AI-generated draft was trying to say.

### Step 6: Conduct locale review

The locale reviewer performs a structured assessment of the adapted draft against the locale acceptance criteria established in step 2. This is the substantive evaluation that determines whether the locale version meets requirements.

The locale review checks:

- **Accuracy:** Does the content accurately convey the meaning and intent of the source content in the target language?
- **Cultural appropriateness:** Is the register, formality, and idiomatic usage appropriate for the target audience and cultural context?
- **Terminology:** Has the approved glossary been applied consistently throughout?
- **Voice and tone:** Does it reflect the voice and tone requirements for this locale?
- **Format and conventions:** Has the locale followed the applicable format and typographic conventions?
- **Compliance and accessibility:** Does it meet any locale-specific requirements?

The locale reviewer records their findings — what was checked, what was found, and what decisions were made. This documentation supports the Locale approval decision and is part of the handoff to stage 06.

### Step 7: Locale approval decision

The locale reviewer confirms whether the locale version meets the acceptance criteria and approves it to proceed to stage 06, or identifies what must change before it can proceed.

A locale version passes Locale approval when all mandatory acceptance criteria are met. Outstanding non-blocking issues may be documented for consideration at Final approval; they are not accepted as exceptions at the Locale approval checkpoint.

If the locale version does not meet mandatory criteria, it returns to step 5 for further adaptation. The locale reviewer specifies what must change. When the adaptation is complete, the locale reviewer re-assesses the revised version.

---

## 5. AI-assisted translation

AI-assisted translation tools can produce a first draft quickly. Using them effectively requires understanding their limitations and treating their output accordingly.

**What AI translation does well**

- Producing a structurally complete draft in a short time
- Applying terminology consistently when supplied with an approved glossary
- Following phrasing patterns when given reference examples
- Identifying content elements that may not translate directly when prompted to flag them

**What AI translation does not do well**

- Adapting register and formality for a cultural context — it may apply source-language conventions to the target language
- Detecting when a phrase is idiomatic or culturally specific and requires adaptation rather than translation
- Maintaining consistent voice across a long document without explicit guidance
- Independently establishing or guaranteeing factual accuracy in the target language
- Producing natural-sounding content in specialised domains without domain-specific grounding

**How to ground AI translation prompts**

Before generating a translation, supply AI with:

1. The source content to be translated
2. The target language and locale
3. The approved glossary for the target language — term-by-term, with the approved translation for each term
4. The target audience description and context
5. The voice and tone requirements for the target locale, including any approved reference examples
6. Notes on content elements requiring cultural adaptation, so AI can flag them rather than translate them directly
7. Any format or typographic conventions the output should follow

A prompt that supplies these materials will produce a more usable draft than one that simply asks AI to "translate this content into [language]."

**Evaluating an AI-generated translation**

The locale reviewer assesses the AI-generated draft against the source content — not by editing the draft toward acceptable, but by evaluating whether it accurately and appropriately conveys the source content in the target language. Common issues to look for:

- **Source-language structure carried over:** Sentences that follow the word order or grammatical structure of the source language but are unnatural in the target language
- **Inconsistent terminology:** Terms that differ from the approved glossary, or the same term translated differently in different places
- **Register mismatch:** Formality level that is too high or too low for the target audience and cultural context
- **Literal translation of idiomatic content:** Phrases that make grammatical sense but carry unintended meaning in the target language
- **Undetected cultural references:** Source-language cultural references that have been translated literally rather than adapted

A draft with any of these issues should be reworked, not accepted and lightly edited. See [`failure-modes.md`](../03-ai-content-creation/failure-modes.md) for further detail on AI-assisted content failures that apply to translation tasks.

**When to use AI translation and when not to**

The following content categories must not be generated or translated using AI assistance, regardless of subsequent human review. These restrictions are carried forward from the AI Content Creation module and apply equally to translation:

- Legal disclaimers
- Clinical instructions
- Financial product terms
- Safety-critical instructions

Content in these categories must be handled through an appropriate human-led process from the outset.

For all other content, AI-assisted translation is appropriate as a starting point for most content types. It is less appropriate for:

- Other legal or compliance content — where accuracy carries legal weight and errors can have material consequences — consider briefing a human translator
- Content with high cultural specificity, where cultural adaptation is the primary challenge and AI is likely to produce a draft requiring substantial rewriting
- Very short content, where the effort to review and correct an AI draft may exceed the effort of translating it directly

In these cases, consider briefing a human translator from the outset.

---

## 6. Briefing a locale reviewer

The locale reviewer is responsible for the accuracy, cultural appropriateness, and quality of the locale version. Giving them what they need to do that work effectively is the practitioner's responsibility.

**What to include in a locale reviewer brief**

- **Source content:** The quality-reviewed source content, clearly marked as the source version on which the locale version is based
- **Target audience and context:** A description of who will use the content in this locale, in what context, and what they need to understand or do with it
- **Voice and tone requirements:** The applicable voice and tone guidelines for the locale, including any approved reference examples in the target language
- **Approved glossary:** The complete approved glossary for the target language, with clear guidance on how it should be applied
- **Notes on elements requiring cultural adaptation:** Specific passages or elements in the source content that require cultural adaptation rather than direct translation
- **Locale acceptance criteria:** What the locale version must meet to pass Locale approval, what constitutes a blocking finding, and how outstanding non-blocking issues should be documented
- **Format and typographic conventions:** Any locale-specific formatting requirements, including date formats, number formats, currency, RTL layout considerations, and punctuation conventions
- **Reviewer qualifications:** Confirmation that the reviewer has the required language proficiency, domain knowledge, and familiarity with the target cultural context, as established in the locale requirements for this task
- **What to deliver:** The expected format of the locale reviewer's output — a translated and adapted document, a list of tracked changes, review notes, or a completed review record

**What the locale reviewer should return**

- The adapted locale version
- Review notes: what was checked, what required adaptation, what decisions were made
- Notes on any elements that required significant cultural adaptation and the reasoning
- Notes on any outstanding issues for consideration at Final approval
- A confirmation that the locale version meets (or does not meet) the acceptance criteria

**When the locale reviewer is not the translator**

Where the locale reviewer is reviewing a draft produced by AI or a separate human translator, they should approach the draft critically — assessing it against the source content and locale requirements, not simply correcting the existing translation. If the initial draft requires substantial rewriting, the reviewer should rewrite rather than patch. A heavily patched AI translation is often less coherent than one written from scratch.

---

## 7. Managing multiple locales

When content is being localised into more than one language simultaneously, each locale version is managed as an independent content set. Decisions made for one locale do not apply automatically to others.

**Tracking locale-version status**

For tasks involving multiple locales, maintain a clear record of each locale version's status:

- Which source version it is based on
- Current step in the seven-step process
- Whether the initial draft has been reviewed and adapted
- Whether locale review has been completed
- Whether Locale approval has been granted
- Any outstanding issues documented for Final approval

This record prevents locale versions from being overlooked and makes it visible when a source content change requires reassessment.

**Consistency across locales**

Where the same approved terminology applies across multiple locales (product names, feature names, trademarks), confirm that it is applied consistently and in the correct form for each locale. Some terms are translated; others are kept in the source language; others have locale-specific approved forms. The approved glossary for each locale should specify the correct treatment.

**Coordinating locale review**

Where multiple locales are being reviewed simultaneously, the practitioner coordinates reviewer availability and progress without creating cross-locale dependencies. Each reviewer works from the same quality-reviewed source content and their locale-specific requirements. If a source content issue is identified during one locale's review, assess its impact on all other locale versions before concluding that review.

**When locales complete at different times**

Locale versions will often complete review at different times. Each locale version that passes Locale approval may proceed to stage 06 independently. The practitioner confirms that all required locales have passed Locale approval before the full deliverable is considered ready for Final approval.

---

## 8. Source content changes during localisation

If the source content is revised after localisation has begun, the practitioner assesses the impact before allowing in-progress or approved locale versions to continue.

**Step 1: Identify what changed**

Review the change to the source content and identify: what specifically was changed, whether the change affects meaning, intent, or requirements, and which locale versions are likely to be affected.

**Step 2: Assess impact on each locale version**

For each locale version, assess whether the source change affects the translated content. A source change that affects a passage that has not yet been translated requires updating the source materials before translation continues. A source change that affects a passage that has already been translated or adapted requires a corresponding revision to the locale version.

This assessment covers every locale version based on the previous source version, including versions that have already passed Locale approval but have not yet received Final approval.

**Step 3: Revise the source content through the appropriate stages**

Assess the source change against Stage 06's revision-routing table to identify where re-entry is required. The revised source content must return to the earliest affected stage — which may be Stage 01 for new or materially changed research needs, Stage 02 for changes to approach or requirements, Stage 03 for new content creation or substantial restructuring, or Stage 04 for content requiring renewed Quality review. Complete all necessary work at each stage in sequence. Only after the revised source content has passed Quality review at Stage 04 should it be used as the basis for locale work.

**Step 4: Update affected locale versions**

For each affected locale version, make the necessary revision and return it to the locale reviewer for assessment. The locale reviewer confirms whether the revision is accurate and appropriate in the target language. If the locale version had already passed Locale approval, the revised version must complete locale review again before it can proceed.

**Step 5: Record the change**

Document the source change, its impact assessment, and the actions taken for each locale version in the Decision and iteration log. This record supports the Final approval process and future maintenance.

---

## 9. References

| Document | Relationship to this workflow |
|---|---|
| [`stages/05-localisation-and-adaptation.md`](stages/05-localisation-and-adaptation.md) | Workflow context for localisation — required reading before using this guide; covers entry and exit conditions, checkpoints, and integration with the full lifecycle |
| [`human-checkpoints.md`](human-checkpoints.md) | Locale approval checkpoint definition and decision criteria |
| [`master-workflow.md`](master-workflow.md) | Full lifecycle overview, including when localisation applies and how it connects to other stages |
| [`stages/06-delivery-and-maintenance.md`](stages/06-delivery-and-maintenance.md) | What happens after Locale approval: Final approval, delivery, and maintenance of locale versions — including the revision-routing table used in Section 8 |
| [`grounding-guide.md`](../03-ai-content-creation/grounding-guide.md) | How to prepare grounding materials for AI-assisted translation — directly applicable to steps 3 and 4 of the localisation process |
| [`failure-modes.md`](../03-ai-content-creation/failure-modes.md) | AI content failure modes relevant to translation: source-language structural carryover, register mismatch, inconsistent terminology, undetected cultural references |
| [`prompt-templates/`](../03-ai-content-creation/prompt-templates/) | Prompt templates for AI-assisted translation, terminology checks, and localisation issue identification |
| [`templates/`](templates/) | Operational templates for handoffs, decision logs, and content briefs — all applicable to localisation tasks |
