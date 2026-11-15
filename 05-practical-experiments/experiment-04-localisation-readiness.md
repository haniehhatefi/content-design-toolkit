# Experiment 04: Localisation Readiness

**Phase 6: Practical Experiments**

---

## 1. Research question

How do two constructed content outputs compare when one is developed with explicit localisation guidance and the other without it, and what does assessing their readiness for a specific target locale require from a human reviewer?

---

## 2. Hypothesis

The experiment constructs two illustrative outputs that differ only in whether explicit localisation guidance was applied. Where that guidance is present, the constructed output is intended to demonstrate translation readiness characteristics — neutral register, explicit variable marking, simple, clearly structured sentences with variables in identifiable grammatical contexts, and an absence of idiomatic language. Where it is absent, the constructed output demonstrates characteristics that would require additional preparation before localisation: idiomatic phrasing, informal register, and embedded variables in sentence structures that may not accommodate word-order variation in target languages. Confirming whether either output is ready for localisation into a specific target locale requires the reviewer to evaluate it against the requirements of that locale — a judgment that extends beyond the structural properties visible in the source content.

---

## 3. Test scenario

The scenario is a short notification content set for a generic subscription-based platform in which an automatic subscription renewal has processed and the account holder is being notified.

The content set consists of four pieces:

| Piece | Type | Purpose |
|---|---|---|
| P1 | Email subject line | Identifies the notification topic |
| P2 | Salutation | Addresses the account holder |
| P3 | Notification body | Confirms renewal and states the next renewal date and amount |
| P4 | Action label | Labels the primary action available after the notification |

The following task context is shared by both conditions.

| Element | Context established |
|---|---|
| Notification trigger | An automatic subscription renewal has processed |
| Account holder name | User-specific variable (available as [name]) |
| Renewal amount | User-specific variable (available as [amount]) |
| Next renewal date | User-specific variable (available as [renewal_date]) |
| Primary action available | View or manage subscription settings |
| Action destination | A subscription settings page within the platform |

The audience is the platform's existing subscribers, who may be located in different countries and whose first language may not be English. The notification is intended to be translated and adapted for use in multiple locales.

The initial content set is a constructed illustrative example representing content that might result from AI-assisted drafting without explicit localisation requirements.

---

## 4. Materials

This experiment draws on the following toolkit materials:

- `03-ai-content-creation/grounding-guide.md`
- `03-ai-content-creation/output-evaluation-rubric.md`
- `04-ai-content-workflow/localisation-workflow.md`

---

## 5. Procedure

### Step overview

1. Define the content task, the audience, and the notification context.
2. Construct an illustrative output for Condition A, representing possible characteristics of content produced from a prompt with no localisation specification.
3. Define the localisation guidance for Condition B.
4. Construct an illustrative output for Condition B, representing possible characteristics of content produced from a prompt that includes the localisation guidance.
5. Evaluate both outputs against the Phase 4 output evaluation rubric.
6. Assess each output against the localisation guidance criteria specified in Condition B.
7. Compare the intervention each output would require from a human reviewer before it could enter a localisation workflow.

---

## 6. Observations

### 6.1 Condition A: content without localisation guidance

**Prompt (Condition A):** The shared task context from Section 3 (notification trigger, variable names, available action, audience description) was included. The content instruction was:

> Write a subscription renewal notification for an account holder confirming that their subscription has been automatically renewed.

**Output A (illustrative):**

> **Great news — your subscription has been renewed! 🎉**
>
> Hi [name],
>
> Great news! We've just renewed your subscription, and you're all set.
>
> Heads up — your next renewal is due on [renewal_date] for [amount].
>
> **Manage my subscription**

**Characteristics of Output A:**

- Idiomatic phrases: "Great news", "you're all set", "Heads up" — informal and culturally-bound; may not translate cleanly or may carry unintended tone in other languages
- Informal contractions: "We've", "you're" — may require restructuring in some target languages
- Emoji in the subject line: requires review against target-locale expectations, audience, channel, and platform conventions; not automatically unsuitable for localisation
- Subject line and notification body both open with "Great news" — an idiomatic phrase that is repeated across pieces
- Variables [renewal_date] and [amount] are embedded within a single sentence connected by "for" — a structure that may require restructuring in languages where word order or case marking places these elements differently
- Register: informal and conversational; assumes familiarity between platform and user that may not be appropriate in formal-register locales
- Action label: "Manage my subscription" uses first-person possessive, which may not translate appropriately into languages that handle possession differently in imperative constructions

---

### 6.2 Localisation guidance

The following specification was used to anchor Condition B.

| Element | Guidance provided |
|---|---|
| Register | Formal and neutral; suitable for adaptation without tone recalibration |
| Idioms and culturally-specific phrases | Avoid; replace with direct, neutral phrasing |
| Contractions | Avoid; use full forms throughout |
| Emoji and decorative punctuation | Avoid by default where they add no functional meaning; assess suitability against target-locale expectations, audience, channel, and platform conventions |
| Variable marking | Mark all user-specific values as named variables: [name], [amount], [renewal_date] |
| Variable placement | Place variables in clearly identifiable positions and avoid embedding them in complex sentence structures; their final placement should be determined during target-language adaptation |
| Sentence structure | Use simple, clearly structured sentences; avoid unnecessarily complex or deeply embedded clauses, particularly where they contain variables; keep each variable in a clearly identifiable grammatical context |
| Action labels | Use neutral constructions without first-person possessive; prefer imperative form |

---

### 6.3 Condition B: content with localisation guidance

**Prompt (Condition B):** The same shared task context and content task instruction as Condition A, with the localisation guidance from Section 6.2 added. The localisation guidance is the only substantive difference between the two prompts.

**Output B (illustrative):**

> **Your subscription has been renewed**
>
> Dear [name],
>
> Your subscription has been renewed. Your next renewal is scheduled for [renewal_date]. The renewal amount is [amount].
>
> To view or update your subscription settings, select the link below.
>
> **Manage subscription**

**Characteristics of Output B:**

- Subject line: direct and informational; no idiomatic phrases or decorative punctuation
- Variables [name], [renewal_date], and [amount] are explicitly marked; the date and amount appear in separate, clearly structured sentences
- Action label: "Manage subscription" uses neutral imperative form without first-person possessive
- Sentence structure: simple and clearly structured throughout; one idea per sentence; variables in clearly identifiable grammatical positions; no multi-clause constructions containing variables
- Register: formal and neutral throughout; no contractions, no idioms, no decorative punctuation

---

### 6.4 Locale-specific convention not addressed by the guidance

Output B improved the structural properties relevant to translation readiness. However, the salutation "Dear [name]" follows standard English formal correspondence convention but does not account for locale-specific salutation requirements.

The issue is not that every locale requires a different salutation. Some locales may use a form similar to "Dear [name]"; others may adapt or omit the salutation entirely. The more precise finding is threefold: [name] is explicitly marked as a variable; the data format represented by [name] is unspecified — it may contain a first name, a full name, or a locale-formatted name; and the appropriate salutation convention for a specific locale cannot be confirmed without target-locale requirements. The localisation guidance addresses variable marking but does not supply these requirements.

This is a compound finding. The localisation guidance reduced structural barriers in Output B: variables are explicitly marked and placed, idioms are absent, contractions are removed, and sentences are structured for clean extraction by translation tooling. But Output B still retains a salutation form whose locale appropriateness cannot be established from the source content alone. The guidance addresses how content is structured for processing; it does not address whether the content's conventions — including the salutation form and the nature of the [name] variable — are appropriate for a specific target locale.

This distinction — between **translation readiness** (structural properties that allow content to be processed and translated with less rework) and **locale appropriateness** (whether the content, once translated and adapted, is contextually correct and culturally appropriate for a specific locale) — maps to the stages of the localisation workflow:

1. **Source preparation** — variables, strings, structure, and terminology are identified and prepared.
2. **Translation readiness** — the source can enter localisation without avoidable structural ambiguity.
3. **Locale approval** — the translated or adapted content is reviewed for linguistic and contextual appropriateness in the target locale.

Translation readiness, as demonstrated by Output B, does not mean that the content is ready for every target language without further structural adaptation. It means that avoidable source-level barriers have been reduced. A human reviewer assessing Output B must evaluate both dimensions: does the content meet structural readiness criteria, and are its conventions appropriate for the target locale?

---

### 6.5 Evaluation against the Phase 4 output evaluation rubric

| Dimension | Output A assessment | Output B assessment |
|---|---|---|
| **Accuracy** | Meets — the variables are correctly used as placeholders; no specific claims about subscription duration, account status, or benefits beyond confirming the renewal are made; the structure is consistent with the shared task context | Meets — variables are correctly marked and placed; the salutation convention is a locale-specific matter, not a factual inaccuracy in the source content |
| **Voice alignment** | Does not meet — informal register, idiomatic phrases, and contractions are not consistent with the requirements of a neutral formal notification; the register would require recalibration before entering a localisation workflow | Meets — neutral, formal register is consistent with the requirements specified in the localisation guidance; the communication style is applied consistently across all four pieces |
| **Audience fit** | Does not meet — informal tone and idiomatic language create barriers for readers whose first language is not English; the register is likely to be inappropriate when adapted to locales where formal register is standard | Partially meets — neutral register and clear variable marking suit a broad multilingual audience; the salutation form and [name] variable format are not confirmed as locale-appropriate for all target locales |
| **Task completion** | Meets — the renewal confirmation, next renewal date, and renewal amount are communicated via the shared variables; the available action is provided; idiomatic framing adds register noise but does not prevent the information from being communicated | Meets — the renewal confirmation, next renewal date, and renewal amount are each stated directly in separate sentences; the action is clearly labelled; the information is unambiguously structured |
| **Concision** | Approximately 34 words across four pieces (subject line, salutation, body, and action label; variables counted as one word each; emoji not counted); some words carry register rather than information ("Great news" appears twice; "you're all set" and "Heads up" are tonal rather than informational) | Approximately 37 words across four pieces (same counting convention); slightly longer in absolute word count, but each word carries a specific piece of information |

---

### 6.6 Human intervention required

| | Output A | Output B |
|---|---|---|
| **Nature of intervention** | Restructuring content for translation readiness — removing idioms, removing contractions, neutralising register, correcting variable placement and sentence structure, replacing action label | Reviewing structural compliance with localisation guidance; assessing locale-specific conventions, including the salutation form and what the [name] variable should represent in the target locale |
| **Scope of intervention** | Substantial — the output requires a full revision pass before it is structurally ready for localisation; the revision covers register, phrasing, and sentence structure throughout | Targeted — the output is structurally ready for a localisation workflow; intervention focuses on locale-appropriateness assessment and confirming conventions against target-locale requirements |
| **Primary risk if used without review** | Content that enters localisation without translation readiness preparation creates rework at the translation stage; idioms may be translated literally or require significant adaptation; informal register may produce inappropriate output in formal-register locales | The salutation form may be inappropriate for the target locale; this risk is less visible than Output A's structural issues because the content otherwise meets the localisation guidance criteria |
| **Expertise required for review** | Knowledge of localisation guidance criteria to identify and revise structural issues; knowledge of the target locale to confirm that the revised register is appropriate | Knowledge of the localisation guidance criteria to confirm structural compliance; knowledge of the target locale to assess salutation conventions, name variable format requirements, and register appropriateness in the adapted output |

**Key observation:** Localisation guidance changes the nature of reviewer intervention. With Output A, the reviewer must identify and revise structural properties before the content can enter a localisation workflow. With Output B, the reviewer can focus on locale-appropriateness assessment rather than structural preparation. In both cases, the reviewer must hold knowledge of the target locale — not only of the localisation guidance criteria — because translation readiness can be assessed against the guidance, but locale appropriateness requires knowledge external to the source content.

---

## 7. Evaluation

### What the experiment demonstrates

The comparison illustrates how two constructed outputs can differ when one incorporates explicit localisation guidance and the other does not: Output B uses a neutral register, marks variables explicitly, avoids idioms and contractions, and structures sentences for clean extraction. Voice alignment showed clear improvement — specifically, alignment with the neutral and formal requirements specified in the localisation guidance. Audience fit showed partial improvement: the structural barriers to multilingual readability were reduced, but the salutation convention remains locale-specific and cannot be confirmed as appropriate without target-locale knowledge. Task completion is consistent between conditions: both outputs communicate the renewal confirmation, the next renewal date, the renewal amount, and the available action; Output B communicates this information more directly, with each piece stated in a dedicated sentence. Accuracy is consistent between conditions: both outputs use the available variables as placeholders without introducing unsupported claims. Concision shows no clear advantage to either condition: Output A is slightly shorter in absolute word count (approximately 34 words) but includes words that carry register rather than information; Output B is slightly longer (approximately 37 words) with each word carrying informational content.

### What localisation guidance does not cover

The experiment illustrates a boundary of localisation guidance: it addresses the structural properties that allow content to be translated with less rework, but it does not establish whether the content's conventions are appropriate for a specific target locale. Output B follows all the structural guidance but retains a salutation form — "Dear [name]" — whose appropriateness depends on the target locale, the name data available in that locale, and the platform's established conventions for that market. These are questions that cannot be answered from the source content or the localisation guidance alone.

This boundary has an implication for how localisation review is scoped. Structural review — checking that guidance criteria are met — is a different task from locale-appropriateness review, which requires knowledge of the target locale that is external to both the content and the guidance. Where content will be adapted for multiple locales, both reviews may be needed, and they may require different reviewers or different review stages.

### The nature of localisation review

The comparison makes visible that localisation review requires the reviewer to hold knowledge beyond the guidance itself. Identifying that Output A uses idiomatic phrases and informal contractions requires knowledge of the localisation guidance criteria. Confirming that Output B's sentence structures and variable placements are appropriate for a target language requires knowledge of that language. Assessing whether "Dear [name]" is an appropriate salutation for a specific locale requires knowledge of that locale's correspondence conventions and of what name data is available.

This has a practical implication for how output evaluation is scoped. When working with localisation guidance, the evaluation checklist should include an explicit step: confirm structural compliance against the guidance, and separately confirm locale-appropriateness with input from someone with knowledge of the target locale. These are not the same review, and they should not be scoped as one.

### Rubric dimension most visibly differentiating the two constructed outputs

The rubric dimension that most visibly differentiates the two constructed outputs in this experiment is **voice alignment** — specifically, whether the content uses a neutral, formal register consistent with localisation requirements. This is the dimension where the difference between the two constructed outputs is most immediately apparent, because it manifests across every piece: the subject line, the salutation, the notification body, and the action label.

---

## 8. Limitations

**Illustrative outputs**

Both outputs were constructed to demonstrate specific characteristics. This experiment cannot establish what AI systems would produce under equivalent conditions with these prompts, or how consistently localisation guidance improves output readiness. The comparison is an illustration of two output types and the evaluation method applied to them.

**Source-language scope**

This experiment evaluates outputs in the source language (English). It does not examine the quality or appropriateness of translated or adapted output in any specific target language. Localisation readiness, as assessed here, concerns structural properties of the source content; the adequacy of the localised output in a specific target language is not examined.

**Language-pair specificity**

Localisation requirements vary significantly between language pairs. Variable placement, sentence structure, and register appropriateness in translation depend on the characteristics of the specific target language. This experiment does not examine any target language and cannot establish which structural properties of Output B would or would not create challenges for a specific translation.

**Single content type**

This experiment uses a subscription renewal notification. The relationship between localisation guidance and translation readiness may play out differently for other content types — particularly those with longer strings, more complex variable structures, or less standardised conventions, such as help documentation, legal notices, or marketing copy.

**Specification without locale-specific requirements**

The localisation guidance in Condition B addresses structural properties of the source content without specifying target-locale requirements: particular languages, expected formality levels for specific markets, or platform conventions for specific locales. Where localisation is planned for specific target locales, guidance that includes locale-specific requirements would address a wider range of readiness questions than the structural guidance used here.

---

## 9. Recommendations

### 1. Include a localisation specification in content briefs for content intended for multiple locales

Where content will be translated or adapted for use in more than one locale, the content brief should include a localisation specification: register guidance, variable marking conventions, instructions for avoiding idioms and culturally-specific references, and sentence structure guidance. This makes localisation readiness criteria an input to the AI-assisted drafting step, rather than a requirement applied only in a later restructuring pass.

*Toolkit implication:* The content brief template already includes an audience section and a requirements field. Adding a localisation field — activated for content that will be translated — would make localisation specification a standard brief activity for applicable content types. The localisation criteria developed for a content type could be documented alongside the brief as a reusable specification for that type.

### 2. Distinguish structural review from locale-appropriateness review in the evaluation pass

Reviewing content for translation readiness — checking that guidance criteria are met — is a different task from reviewing content for locale appropriateness, which requires knowledge of the target locale. These should be scoped separately in the output evaluation pass, and where the team's current capabilities do not cover a required target locale, specialist input should be arranged for the locale-appropriateness review.

*Toolkit implication:* The five human oversight checkpoints include a Quality checkpoint and a Localisation checkpoint. Locale approval takes place within the localisation workflow, as a step in the Localisation checkpoint stage. For content with localisation requirements, the Quality checkpoint should note the distinction between structural review (checkable against the guidance) and locale-appropriateness review (requiring target-locale knowledge), so the reviewer knows which review they are conducting; the Localisation checkpoint is where locale approval occurs.

### 3. Specify the nature of name and date variables where locale requirements are known

Where content uses variables for user data such as names and dates, the brief should specify what format those variables will contain — a first name, a formatted full name, or a locale-specific form — and whether the format varies by locale. This reduces ambiguity at the translation and adaptation stage and allows locale reviewers to flag format requirements before the content is released.

*Toolkit implication:* Variable specification is an element of content grounding. The grounding guide in `03-ai-content-creation/grounding-guide.md` could include a section on variable format specification for content types that use user-specific data, noting where the format is locale-dependent and what information the brief should supply.

### 4. Document locale-specific conventions as reference material for recurring localisation tasks

Where content will be regularly localised into the same target locales, the conventions for those locales — salutation forms, date format requirements, register expectations — should be documented as reference material and made available to the team. This reduces the dependency on locale-specific knowledge being held by one reviewer and supports consistency across localised versions.

*Toolkit implication:* This is a possible future enhancement to the localisation guide rather than a change to any currently completed phase. Where a team has established target locales, a locale conventions reference — covering salutation forms, name formatting, and register norms for each locale — would make locale-appropriateness review more consistent and reduce per-task setup time.
