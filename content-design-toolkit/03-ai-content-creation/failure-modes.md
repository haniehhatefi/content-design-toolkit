# Failure modes

This document describes 15 AI failure patterns that arise specifically when using the toolkit's prompt templates. Each failure mode is documented with how to recognise it in an output and what to do about it.

This document is not a list of general AI limitations — it describes failures that are specific to the toolkit's grounding approach, its three-tier guidance level framework, and the content types its templates cover. General AI limitations (hallucination, verbosity, inconsistency) are real, but they are not specific enough to act on. The failure modes here are specific to the toolkit's workflow and can be recognised and acted on.

**How to use this document.** Use it at two points in the workflow. Before prompting: scan Section 1 (Grounding failures) to prepare grounding that reduces the most common failure patterns. After receiving output: use the [output evaluation rubric](output-evaluation-rubric.md) to evaluate the output systematically, then consult the relevant section here when a specific problem is detected.

---

## 1. Grounding failures

Grounding failures occur when the AI does not apply the supplied grounding accurately — either by substituting its own trained defaults, misinterpreting the guidance level of a criterion, or selectively attending to some grounding over others.

Grounding failures are partly preventable. Well-structured grounding that follows the [grounding guide](grounding-guide.md) reduces their frequency. Some will occur regardless of grounding quality and require post-hoc detection.

---

### 1.1 Guidance-level inflation

**What it is:** The AI promotes a Recommendation to a Rule. The output treats a guideline labeled Recommendation in the supplied grounding — one that content designers can exercise judgment on — as a non-negotiable requirement.

**How to recognise it:**
- Sentence case described as "required" or as a Rule — it is a Recommendation in both the error messages and buttons and CTAs patterns
- Voice attribute directions (Clear, Human, Helpful) described as Rules — they are directional attributes, not binary requirements
- The output uses language like "must", "required", or "violates the standard" for guidance that the toolkit marks as Recommendation

**Common trigger:** This failure is most likely when the grounding does not explicitly label guidance levels, or when the reusable instructions include general guidance without linking it to the three-tier framework.

**What to do:** Verify any "must" or "required" framing against the source file. If the criterion is a Recommendation, the AI's framing has overstated it. The output is still usable if the underlying observation is correct — reclassify the guidance level and evaluate the finding accordingly. For recurring instances, add an explicit note to the reusable instructions that names specific criteria the AI is likely to inflate: "Sentence case is a Recommendation [Rec], not a Rule."

---

### 1.2 Grounding recency bias

**What it is:** A potential failure in multi-layer grounding: the AI may give more attention to material supplied later and apply earlier material less consistently. In this toolkit, this could mean that criteria from the reusable instructions are under-represented when reference context and task-specific instructions follow them.

**How to recognise it:**
- Voice attributes (Clear, Human, Helpful) are absent from annotations even when they are relevant — these are typically in the reusable instructions, supplied first
- Writing standards (Direct, Consistent) are not referenced even when the content clearly raises them
- Module 2 pattern criteria (supplied later as reference context) are well-represented; Module 1 criteria (voice) are not
- Generation annotations focus only on pattern-level Rules and Recommendations without any voice dimension

**Potential contributing conditions:** Long grounding inputs, generic reusable instructions, or a dense block of reference context immediately preceding the task-specific request.

**What to do:** Add an explicit instruction at the start of the task-specific request: "Apply both the voice attributes in the reusable instructions and the [content type] pattern Rules in the reference context." This anchors both grounding layers at the point where the task is introduced. If voice is consistently under-represented, consider including the voice attributes as a brief reminder at the top of the task-specific request.

---

### 1.3 Contextual decision reclassification

**What it is:** The AI promotes a Contextual decision (situation-dependent, requires the content designer's judgment) to a Recommendation or Rule, based on the AI's own assessment of what is usually better. The output presents a Contextual choice as if the toolkit has a preference.

**How to recognise it:**
- First vs. third person ("We couldn't send your message" vs. "Your message couldn't be sent") presented as a Recommendation rather than a Contextual choice
- Tone matching for error severity framed as a Recommendation rather than a designer judgment
- Empty state illustrations described as "best practice" despite the toolkit labeling them Contextual
- The output explains why one Contextual choice is "better" rather than explaining the situational factors

**Common trigger:** AI tools have strong priors about UX writing conventions from training data. When a Contextual decision aligns with what the AI considers standard practice, it tends to present it as normative rather than situational.

**What to do:** When an annotation or finding includes the word "best practice" or cites a preference without situational factors, check whether the criterion is Contextual in the source file. If it is, the finding should identify it as Contextual and list the situational factors rather than recommend one option. Use the finding as a prompt to make your own situational judgment; do not accept the AI's framing as a standard.

---

### 1.4 Generic defaults override product context

**What it is:** The AI produces output that reflects generic UX writing conventions from its training data rather than the product-specific context and vocabulary supplied in the prompt. The output is plausible but does not reflect the product.

**How to recognise it:**
- Generated button labels use generic verbs ("Get started", "Continue", "Submit") despite a specific product action being named in the prompt
- Empty state copy does not use the product's established terminology for its primary object ("item" or "document" instead of the product's own term)
- Error message recovery steps reference generic support channels rather than the product's specific recovery path
- Review annotations evaluate copy against a generic "clear and simple" standard rather than the product's voice attributes

**Common trigger:** This failure is most likely when the PRODUCT CONTEXT field is brief or absent, when the product's own terminology is not supplied in the prompt, or when the task-specific request does not anchor the product's voice explicitly.

**What to do:** Extend the PRODUCT CONTEXT field with the product's own terminology, the audience's characteristics, and one or two examples of copy the product already uses that reflects its voice. For generation specifically, supply the OBJECT field with the exact product term. For recurring instances, build a terminology list as part of the reference context.

---

## 2. Generation failures

Generation failures arise specifically when using the [microcopy generation prompts](prompt-templates/microcopy-prompts.md). They concern the content of generated options and the structure of the output.

---

### 2.1 Invented product states

**What it is:** A generated option includes specific product states, feature names, flow paths, timeframes, or recovery links that the AI invented. The invented content is plausible and may not be identifiable without product knowledge.

**How to recognise it:**
- Recovery steps name specific paths that may not exist in the product ("Go to Settings > Account > Security")
- Timeframes are stated with false precision ("try again in 30 minutes", "your session will expire in 10 minutes") without being supplied in the prompt
- Feature or plan names appear that the product uses generally ("upgrade to Pro") but have not been verified as the exact current name
- An error message links to a support page that may not exist

**What to do:** Treat any option that includes specific paths, timeframes, feature names, or recovery links as a template requiring verification before use. Verify each specific element against the actual product before selecting the option. For generation prompts that require recovery steps, supply the specific recovery path in the CONSTRAINTS field rather than relying on the AI to infer it. See [AI content principles — Factual and product-specific claims](ai-content-principles.md#factual-and-product-specific-claims).

---

### 2.2 Structural component omission

**What it is:** A generated option omits a Rule-required structural component, producing copy that is incomplete according to the Module 2 pattern's anatomy. The omission may not be obvious if the option sounds coherent without the missing part.

**How to recognise it:**
- An error message does not include "what to do next" — the message describes the problem but gives no path forward [Rule]
- A notification states that something happened but does not name what happened specifically [Rule]
- The annotation does not reference the anatomy at all, suggesting the AI was not checking against it

**Common trigger:** Most likely when the error message or empty state is short — the AI may treat brevity as inherently compliant. Longer, more complex scenarios tend to include all components because the AI has more context to work with.

**What to do:** Apply the Module 2 Review Checklist for the content type to every option before selecting one. For error messages specifically, verify: (1) states what went wrong, (2) includes what to do next. For empty states: (1) explanation, (2) next step (CTA matching the product's primary action for first-use states). Do not select an option that is missing a Rule-required component, regardless of how well it handles the Recommendations.

---

### 2.3 Near-identical options

**What it is:** A generation output produces multiple options that differ only in minor word-level variation rather than representing meaningfully different approaches to the writing problem. The output technically provides N options but does not give the content designer genuine alternatives to evaluate.

**How to recognise it:**
- All options use the same opening word or phrase
- All options have the same structure (what went wrong → what to do) without exploring alternatives (what to do → what went wrong)
- The annotations describe all options as "clear and direct" or "compliant with all Rules" without distinguishing them
- The options differ mainly in wording rather than in structure, emphasis, specificity, or approach

**Common trigger:** This failure is most likely with highly constrained prompts (short character limits, restrictive requirements) or when the content type is simple (a toast notification, a one-line inline validation error).

**What to do:** Explicitly push for structural contrast in the CONSTRAINTS field: "One option that opens with the problem; one that opens with the resolution. One shorter option; one longer option that provides more context." If the character limit is genuinely very tight and options will necessarily be near-identical, reduce the number of options to two and ask for a specific annotation explaining the trade-off between them.

---

## 3. Review failures

Review failures arise specifically when using the [review prompts](prompt-templates/review-prompts.md). They concern the structure, coverage, and framing of review outputs.

---

### 3.1 Review framed as verdict

**What it is:** The AI frames the review output as a pass/fail verdict on the content, rather than a structured evaluation for the content designer to act on. The output pre-empts the designer's judgment about what to change.

**How to recognise it:**
- The output concludes with "this content is not ready to publish" or "this copy passes the review"
- The summary section gives an overall quality judgment rather than a count of Rule violations and Recommendation observations
- Recommendation observations are framed as blockers ("you need to fix this") rather than considerations ("this is worth reviewing")
- The output does not carry the label "structured evaluation for human review"

**What to do:** Disregard the verdict framing and work from the findings directly. Rule violations require a change regardless of how the AI frames them; Recommendation observations are for your judgment regardless of how strongly the AI presents them. If the AI is consistently framing outputs as verdicts, add an explicit instruction to the task-specific request: "Present findings as a structured evaluation for human decision-making. Do not state whether the content is ready to publish."

---

### 3.2 Coverage drop

**What it is:** When a review is supplied with multiple items (a set of error messages, a series of notifications, all button labels for a component), the AI reviews the first few items thoroughly and gives reduced attention to later items — or omits them entirely.

**How to recognise it:**
- A review of five error messages where only three are referenced by name in the findings
- A voice alignment review that quotes specific text from early items but gives only general observations about later ones
- The findings count in the summary is lower than the number of items supplied would warrant
- Later items in a set receive "No issues identified" without engagement, while earlier items receive detailed findings

**Common trigger:** This failure is most likely with longer sets (five or more items) and with more complex content types (error messages, empty states) that require more output per item. It is less common with simpler content types (button labels, toast notifications).

**What to do:** For sets of more than three items, either review items in smaller batches (two to three at a time) or explicitly number and list the items in the CONTENT TO REVIEW field and add an instruction: "Review each numbered item separately. Identify findings for each item by its number." After receiving the output, verify that every item is addressed by name or number.

---

### 3.3 Finding consolidation

**What it is:** The AI merges multiple distinct issues into a single finding, losing the specificity needed for the content designer to make a targeted decision about each one. A single consolidated finding may describe two or three separate problems that require different changes.

**How to recognise it:**
- A finding that says "this error message does not follow the error message anatomy" without specifying which component is missing and what the Rule requirement is for that component
- A finding that describes an overall voice concern rather than naming which specific attribute is affected and what the text does that works against it
- A finding count in the summary that is lower than the number of distinct issues visible in the content

**What to do:** Break consolidated findings apart yourself before using the output. For each consolidated finding, identify the distinct issues it contains, the specific text each concerns, and the guidance level for each. If this requires returning to the Module 2 source file to separate the issues, do so — the finding is a prompt for your own analysis, not a complete evaluation.

---

### 3.4 Implicit "no issues identified" in voice review

**What it is:** The voice alignment review template requires an explicit "No issues identified" statement for each attribute where nothing was found. When the AI omits this statement for one or more attributes, the content designer cannot tell whether no issues were found or whether the AI simply did not address that attribute.

**How to recognise it:**
- The voice alignment review output covers three or four evaluation dimensions but not all five (three voice attributes: Clear, Human, Helpful; and two cross-cutting writing standards: Direct, Consistent)
- The summary count is lower than the number of evaluation dimensions assessed
- One or more attributes appear in the output format but have no content under them

**What to do:** Treat any missing attribute as potentially unreviewed rather than as "no issues found." If an attribute is absent from the output, assess that attribute yourself, or run a second prompt specifically for the missing attribute. This failure is in the structural completeness dimension of the [output evaluation rubric](output-evaluation-rubric.md) — it should be caught during the rubric check before the type-specific evaluation.

---

## 4. Rewriting failures

Rewriting failures arise specifically when using the [rewriting prompts](prompt-templates/rewriting-prompts.md). They concern the scope, traceability, and compliance of rewriting outputs.

---

### 4.1 Scope creep

**What it is:** The AI makes changes beyond the stated scope — fixing things the prompt did not identify as issues, changing established product terminology, or restructuring copy in ways that go beyond what the identified issues require.

**How to recognise it:**
- The revised version differs from the original in more places than the IDENTIFIED ISSUES field accounts for
- The change log has fewer entries than visible differences between the original and the revised version
- Established product terminology has been replaced with the AI's own phrasing
- For voice rewrites: the meaning or structure of the content has changed, not only the expression

**Common trigger:** Scope creep is most likely when the original content has multiple issues the AI can detect — even if only one was identified in the prompt, the AI may address others. It is also more likely with voice rewrites, where the boundary between expression and meaning is less clear.

**What to do:** Compare the revised version to the original word by word if the change log does not appear to account for all differences. Any change not in the change log is an unreported edit — evaluate it on its own merits before accepting or rejecting it. For compliance rewrites, the IDENTIFIED ISSUES field constrains what should change; treat any edit outside that scope as requiring separate review.

---

### 4.2 Rules regression after rewriting

**What it is:** Fixing one Rule violation introduces a violation of another. The revised version is compliant on the identified issue but non-compliant on a Rule that the original met.

**How to recognise it:**
- An error message rewritten to remove blame (Rule) no longer includes "what to do next" (Rule)
- A button label rewritten to be more specific (Rule) has been given end punctuation (Rule violation)
- An empty state rewritten for first-use (Rule: match to primary action) now implies the user is at fault for the absence of content (Rule: do not imply fault)
- The change log does not confirm that all Rules requirements are still met in the revised version

**Common trigger:** Rules regression is most likely in compliance rewrites where multiple Rules interact with the same sentence or structural element. Restructuring to address one Rule creates a new gap.

**What to do:** After evaluating the change log, apply the Module 2 Review Checklist for the content type to the revised version. The checklist is a faster check than re-running the rubric from scratch. Do not use a revised version until you have verified it against the full checklist, not only against the identified issues the rewrite was supposed to fix.

---

### 4.3 Voice stripping in length rewrites

**What it is:** A length rewrite meets the character limit but removes the elements that made the original comply with the Human attribute — acknowledgement of the user's situation, natural phrasing, or contextual reassurance. The result is shorter but sounds like a system log entry rather than a helpful product message.

**How to recognise it:**
- The revised version removes a "your draft has been kept" clause to meet a character limit, leaving only the error statement
- The revised version changes from active ("We couldn't save your changes") to passive ("Changes could not be saved") to save characters
- The cut log justifies cuts on length grounds without noting whether voice attributes are still present in the revised version
- The revised version meets the target but the Human attribute is absent from the cut log's confirmation

**What to do:** After evaluating the cut log, assess the revised version against the voice attributes separately from Rules compliance. A version that meets the character limit and all Rules may still fail the Human attribute — both are relevant to whether the version is usable. The length rewrite template instructs the AI to preserve voice attributes; if the cut log does not confirm this, it has not done so. If voice is stripped, return to the original and make the cuts yourself, treating the AI's version as a floor (minimum length possible) rather than a final draft.

---

## 5. Comparison failures

Comparison failures arise specifically when using the comparative review template in [review prompts](prompt-templates/review-prompts.md#3-comparative-review). They concern how the AI evaluates versions relative to each other.

---

### 5.1 Version A anchoring bias

**What it is:** When multiple versions are presented for comparison, the order of presentation may influence how the AI evaluates them. Version A may establish an implicit reference point, causing later versions to be assessed relative to it rather than independently against the supplied grounding. This can make the comparison uneven.

**How to recognise it:**
- The evaluation of Version A is more detailed and covers more dimensions than B or C
- Findings for Version B include comparisons to Version A ("less clear than A's approach") rather than assessments against the grounding
- The recommended starting point is Version A by default, without clear grounds for preferring it over B
- The relative strengths section for each version tends to frame later versions in terms of what they do better or worse than A

**Potential source of bias:** A potential source of bias in ordered comparisons is that the first version may establish an implicit reference point. Later versions may then be assessed relative to it rather than independently against the supplied grounding. Reordering can help reveal whether this has affected the comparison. A finding that changes or disappears when the order changes may indicate that the original assessment was influenced by presentation order.

**What to do:** If you notice the comparison is uneven, re-run it with the versions in a different order and compare the two outputs. If a finding persists across orderings, it may reflect a substantive weakness; if it changes or disappears, the original assessment may have been influenced by presentation order. Treat reordering as a diagnostic check, not proof of anchoring. For high-stakes comparisons, running both orderings may be worth the additional prompt.

---

## Failure modes not covered here

Two failure modes are documented elsewhere in this module:

**Invented accessibility criteria:** When an AI output cites WCAG success criteria not present in the Module 2 pattern's accessibility section, the appropriate response is documented in the [output evaluation rubric](output-evaluation-rubric.md#1-minimum-bar-check) (Section 1a) and the [pattern compliance review usage notes](prompt-templates/review-prompts.md#2-pattern-compliance-review). The core principle: external accessibility criteria are outside the scope of a toolkit-grounded review and must not be presented as toolkit violations.

**General AI limitations** (verbosity, inconsistency, hallucination) are not documented here because they are not specific enough to act on within this workflow. The output evaluation rubric addresses the toolkit-specific consequences of these limitations — invented criteria, structural incompleteness, internal inconsistency — which are actionable. General limitations are addressed by using the rubric and working through the minimum bar check before detailed evaluation.

---

## Related documents

- [AI content principles](ai-content-principles.md) — Pre-prompt checklist and responsible-use requirements; grounding principles that prevent some failure modes
- [Grounding guide](grounding-guide.md) — How to structure grounding context to reduce grounding failures specifically
- [Output evaluation rubric](output-evaluation-rubric.md) — Structured criteria for detecting failure modes in an output
- [Prompt templates — README](prompt-templates/README.md) — Default constraints included in every template to prevent common failures
- [Microcopy generation prompts](prompt-templates/microcopy-prompts.md)
- [Review prompts](prompt-templates/review-prompts.md)
- [Rewriting prompts](prompt-templates/rewriting-prompts.md)
- [Module 2 — UX writing standards](../02-ux-writing-standards/) — Source for grounding and verification
