# Output evaluation rubric

This rubric provides structured criteria for evaluating the outputs produced by the toolkit's prompt templates — generation outputs, review outputs, and rewriting outputs. Use it after receiving an AI output and before deciding how to act on it.

This rubric evaluates the AI's output, not the content itself. Its purpose is to tell you whether the output is usable as a basis for a content decision, not whether the content the AI produced is ready to publish. For evaluating final content against the toolkit's standards, use the Review Checklists in Module 2.

**What this rubric does not replace.** The rubric provides a framework for evaluation; it does not make the evaluation for you. The dimensions below name what to look for — the content designer applies them to the specific output, in the specific context of the prompt, the grounding supplied, and the content type being worked on.

---

## How to use this rubric

Work through it in four steps:

1. **Minimum bar check** (Section 1) — Four conditions that make an output not usable as written. Check these first. If the output fails any of them, re-prompt before continuing.
2. **Universal evaluation dimensions** (Section 2) — Five dimensions that apply to all output types. Work through each.
3. **Output-type-specific criteria** (Sections 3–5) — Additional criteria for generation, review, or rewriting outputs. Apply the section that matches the template you used.
4. **Decision** (Section 6) — Use the evaluation to decide: use the output, use it with annotation, or re-prompt.

The rubric is designed for the full workflow. For a quick check on a familiar output type, the minimum bar check and the type-specific criteria are the most essential.

---

## 1. Minimum bar check

Before detailed evaluation, check for four conditions that make an output not usable. If any of these apply, the output should not be acted on without re-prompting or significant correction.

**1a. Invented criteria.** The output cites requirements, Rules, or Recommendations that are not in the supplied grounding. Signs: a criterion appears that you cannot find in the Module 2 pattern or the reusable instructions; a WCAG success criterion is presented as a requirement of the supplied pattern, or as a toolkit violation, even though it does not appear in the pattern's accessibility section — an external accessibility observation may be relevant, but it must be clearly distinguished from toolkit requirements and independently verified against the applicable accessibility standard before acting on it; the output refers to a "standard" or "best practice" without tracing it to the toolkit.

> This is the highest-priority check. The do-not-invent-criteria instruction in every template is designed to prevent this. When it fails, the output may contain plausible-sounding but ungrounded requirements that lead the content designer to make changes that the toolkit does not require.

**1b. Guidance-level misclassification — a Rule or Recommendation is assigned the wrong level, or a Contextual decision is incorrectly presented as a Rule or Recommendation.** Signs: the output calls something "recommended" when it is a Rule in the supplied pattern (for example, "it is recommended to tell the user what to do next" for an error message, when this is a Rule); or calls something "required" when it is a Recommendation. This is a higher-priority concern than other annotation gaps — a misclassified Rule may prevent publication of copy that is otherwise acceptable, or lead to publishing copy that fails a required standard.

**1c. Structural incompleteness — the output is missing required sections or components.** Signs: a generation output is missing annotations for some options; a review output is missing a section or component required by its specific template — for example, a pattern compliance review is missing one of its four sections, or a voice alignment review omits an attribute without explicitly stating that no issue was identified; a rewriting output has no change log; the output does not include the required label ("options for evaluation" / "structured evaluation for human review"). An output that is structurally incomplete cannot be evaluated against the rubric's other dimensions without first noting what is missing.

**1d. Internal inconsistency — the output contradicts itself.** Signs: the summary section of a review does not match the findings; a generation output's annotation for one option contradicts the annotation for another on the same criterion; a rewriting change log cites a criterion that was not in the IDENTIFIED ISSUES field and was not flagged as a supporting edit. Internal inconsistency suggests the AI is applying criteria inconsistently and the output cannot be used without resolving the contradiction.

**What to do if the minimum bar check fails:** Note which condition applies. For invented criteria, check whether the criterion is real but was not in the grounding — if so, consider whether to add it and re-prompt, or handle it separately. For the other three, re-prompt with the same template, supplying clearer or more complete grounding.

---

## 2. Universal evaluation dimensions

These five dimensions apply to all output types — generation, review, and rewriting. After the minimum bar check, work through each.

### 2a. Grounding fidelity

**What to evaluate:** Whether the output interprets the supplied grounding accurately. Having passed the minimum bar check, the output should now be assessed for whether it preserves the scope, meaning, and intended application of each criterion — not only whether criteria are present, but whether they are applied as the grounding intends.

**What to look for:**
- Each finding, annotation, or change is linked to a specific Rule, Recommendation, or Contextual decision in the grounding
- The output does not paraphrase criteria in ways that change their scope or meaning (for example, widening a Recommendation's scope to apply it in contexts the pattern does not cover)
- Contextual decisions are identified as Contextual and not reclassified as Rules or Recommendations

**Signs of partial grounding fidelity:** The output cites real criteria but applies them broadly or narrowly compared to their actual scope in the pattern. For example, an error message annotation that cites "use plain language" [Rule] as grounds for removing a technical term — when the Rule specifically refers to avoiding technical codes and stack trace language, not all technical terminology — has extended the Rule beyond its documented scope.

**What to do:** For each criterion cited, verify it against the source file. If the AI has extended or narrowed a criterion's scope, note it in your evaluation and apply the criterion as written.

### 2b. Guidance-level accuracy

**What to evaluate:** Each criterion cited in the output carries a guidance level (Rule, Recommendation, or Contextual). Verify that the guidance levels assigned match the source.

**What to look for:**
- Rules are labeled as Rules and treated as required
- Recommendations are labeled as Recommendations and presented as strong defaults, not requirements
- Contextual decisions are labeled as Contextual and explained with their situational factors — not reclassified as Recommendations
- The output does not omit guidance levels where the template required them

**Common guidance-level errors:**
- Sentence case labeled as Rule rather than Recommendation (see [Module 2 — Buttons and CTAs](../02-ux-writing-standards/microcopy-patterns/buttons-and-ctas.md) and [Module 2 — Error messages](../02-ux-writing-standards/microcopy-patterns/error-messages.md))
- The readability target Grade 6–7 for error messages labeled as Recommendation rather than Rule
- "Tell the user what to do next" (error messages) labeled as Recommendation rather than Rule

**What to do:** For any guidance level that seems wrong, verify it in the Module 2 source file before acting on the output's classification. Do not adjust copy or accept a revision on the basis of a guidance-level label you have not verified.

### 2c. Structural completeness

**What to evaluate:** The output includes all components and sections the template requested.

**What to look for — by output type:**

| Template type | Required components |
|---|---|
| Generation | Numbered options; annotation for each option identifying applicable Rules, Recommendations, or Contextual decisions, and explaining the trade-off |
| Voice alignment review | Findings per attribute (Clear, Human, Helpful, Direct, Consistent); "No issues identified" where none; closing summary |
| Pattern compliance review | Section 1 (Rule violations); Section 2 (Recommendation observations); Section 3 (accessibility issues); Section 4 (summary with status flags) |
| Comparative review | Structured assessment per version; comparison summary; recommended starting point |
| Compliance rewrite | Revised version(s); change log per revision |
| Voice rewrite | Revised version(s); voice decision log per revision |
| Length rewrite | Revised version(s) with counts; cut log per revision |

**Signs of incomplete structure:** Sections present but empty without explanation; a summary that lists fewer issues than the findings sections; a change log with fewer entries than visible differences between original and revised versions.

**What to do:** Note missing components. If a section is absent, determine whether it is absent because the output legitimately found nothing (acceptable, if explicitly stated) or because the AI did not follow the output format (not acceptable — re-prompt).

### 2d. Actionability

**What to evaluate:** A usable output gives the content designer a specific basis for a decision. Vague annotations, non-specific findings, or generic observations require additional work before the output can be used.

**What to look for:**
- Annotations and findings quote the specific text they concern, not the content generally
- Findings name the criterion and guidance level, not just describe a problem
- For reviews: observations explain what specifically the content does that the criterion does not permit or recommends against, not just that "it could be clearer"
- For generation: trade-off annotations identify the actual choice made (for example, "prioritises brevity over specificity — omits the specific file format"), not just that "a trade-off exists"
- Recommended next steps (where present) name specific actions, not general directions

**Signs of low actionability:** Annotations that say "this is clearer" without explaining what made the original unclear; findings that say "violates the Rule" without quoting the specific text; a recommended starting point in a comparative review that says "Version B is better overall" without specifying what to change.

**What to do:** For vague findings or annotations, return to the source material (the Module 2 pattern, the voice principles) and apply the criterion yourself. If most of the output is vague, re-prompt with more specific grounding or a more detailed task-specific request.

### 2e. Internal consistency

**What to evaluate:** The output applies the same standards throughout and does not contradict itself.

**What to look for:**
- For generation: the same criterion is applied (or explicitly noted as not applicable) across all options
- For reviews: the summary section reflects the findings — if three Rule violations were identified, the summary counts three Rule violations
- For comparative reviews: the same dimensions are assessed for each version
- For rewriting: the change log accounts for all visible differences between original and revised versions
- Status flags and summary counts match the body of the output

**What to do:** If the summary and findings do not match, trust the findings — summaries are more susceptible to AI averaging and over-simplification. Note the discrepancy and use the findings as your working document.

---

## 3. Generation output evaluation

Apply this section after the universal dimensions, when evaluating output from [microcopy generation prompts](prompt-templates/microcopy-prompts.md).

### 3a. Factual plausibility

Generation outputs may include specific product states, feature names, flow paths, timeframes, or recovery links that the AI invented. These will appear plausible and may be difficult to identify without product knowledge.

**What to look for:**
- Recovery steps that name specific links, paths, or flows ("click Settings > Billing > Manage Plan") — verify that this path exists
- Timeframes ("try again in a few minutes", "your session will expire in 10 minutes") — verify that the product can communicate this accurately
- Feature or plan names ("upgrade to Pro", "export as PDF") — verify that these names match current product terminology
- Quantities or thresholds ("files up to 25 MB", "passwords must be at least 8 characters") — verify against the actual product constraints

**What to do:** Treat any option that includes specific product states, paths, or names as a template requiring verification before use. See [AI content principles — Factual and product-specific claims](ai-content-principles.md#factual-and-product-specific-claims).

### 3b. Option diversity

A generation output with three to five options that are near-identical variations is not useful. Options should represent meaningfully different approaches to the same writing problem.

**What to look for:**
- Do the options differ in structure, not only in word choice? (For error messages: does one lead with what went wrong while another leads with the next step?)
- Do the options explore a range of specificity, length, or tone?
- Does the annotation explain what makes each option different from the others?

**Signs of low diversity:** Options that differ by one or two words; annotations that describe all options as "clear and direct" without differentiating them; options where every version uses the same opening word or phrase.

**What to do:** If diversity is low, narrow the generation to two options and use the CONSTRAINTS field to push for a specific contrast ("one option that leads with what went wrong; one that leads with what to do next").

### 3c. Output framing

**What to look for:** The output is labeled as options for evaluation, not as final or recommended copy. If the output recommends a specific option without being asked to, treat the recommendation as one data point, not a verdict — apply the rubric's other dimensions to all options before deciding.

---

## 4. Review output evaluation

Apply this section after the universal dimensions, when evaluating output from [review prompts](prompt-templates/review-prompts.md).

### 4a. Finding traceability

**What to evaluate:** Each finding should be traceable to a specific criterion in the supplied grounding. This is more specific than grounding fidelity (dimension 2a) — it focuses on whether the finding cites the criterion precisely enough to verify.

**What to look for:**
- Each finding quotes the specific text it concerns
- Each finding names the criterion (or quotes it) rather than describing the problem in general terms
- For pattern compliance review: Section 3 (accessibility) findings should be linked to the accessibility requirements in the Module 2 pattern. External accessibility observations must be identified as outside the scope of the toolkit-grounded review, not presented as toolkit violations, and verified separately if relevant.

**What to do:** For any finding you cannot trace to a specific criterion in the grounding, verify it yourself before acting on it. A finding that cannot be traced is a candidate for the invented-criteria condition in the minimum bar check.

### 4b. Coverage

**What to evaluate:** The review should address all items in the content you supplied and all dimensions in the REVIEW SCOPE field.

**What to look for:**
- For sets of items (multiple error messages): does the review address each item, or did the AI address only the first few?
- For full reviews (Rules, Recommendations, and accessibility): are all three dimensions present in the output?
- For voice alignment review: does the review address all five dimensions (Clear, Human, Helpful, Direct, Consistent), or did it skip some?

**Signs of incomplete coverage:** A review of five error messages where only three are mentioned by name; a "full review" output where Section 3 (accessibility) is absent rather than explicitly empty; a voice alignment review where "No issues identified" appears for every attribute without engagement.

**What to do:** If coverage is incomplete, run a second pass on the missed items or dimensions, or re-prompt with explicit scope.

### 4c. Verdict vs. evaluation framing

**What to evaluate:** A review output is a structured evaluation for human decision-making, not a verdict. The content designer decides what to change, not the AI.

**What to look for:**
- The output presents findings and guidance levels, not a "pass/fail" assessment that pre-empts the designer's decision
- The output is labeled as a structured evaluation for human review
- For pattern compliance review: the status flags (Rule status and accessibility verification flag) are present, but the output does not add its own editorial verdict beyond what the flags communicate

**What to do:** If the output reads as a verdict, use the findings and guidance levels directly and disregard any summary framing that overstates the AI's role. The status flags are the appropriate summary — not "this content is not ready to publish."

---

## 5. Rewriting output evaluation

Apply this section after the universal dimensions, when evaluating output from [rewriting prompts](prompt-templates/rewriting-prompts.md).

### 5a. Scope discipline

**What to evaluate:** A rewriting output should address only the issues identified in the prompt (or the voice concern, or the length target). Changes beyond the stated scope indicate the AI has made additional content decisions without being asked.

**What to look for:**
- For compliance rewrites: the change log accounts for all differences between the original and the revised version — if there are differences not in the change log, the AI has made unreported changes
- For voice rewrites: the revised version preserves the functional content of the original — the meaning and structure should be intact, with only expression changed
- For length rewrites: the cut log accounts for every element removed or shortened — if the revised version is shorter than expected, verify what was removed

**What to do:** Compare the revised version to the original word by word if the change log does not account for all differences. Any change not in the change log is an unreported edit — evaluate it yourself before accepting it.

### 5b. Change log completeness

**What to evaluate:** The change log should account for every difference between the original and the revised version. It is the primary tool for evaluating a rewriting output — if it is incomplete, the revision cannot be properly evaluated.

**What to look for:**
- Every visible difference between original and revised versions appears in the change log
- For compliance rewrites: each change identifies whether it directly addresses an identified issue or is a supporting edit for coherence or restructuring
- For voice rewrites: each change names the voice attribute or writing standard it addresses
- For length rewrites: each change states what was removed or shortened, the guidance level governing that content, and any Contextual decision and situational factors

**What to do:** If the change log is incomplete, do not accept the revision. The missing changes may include alterations to meaning, Rule requirements, or established product terminology. Re-prompt and ask for a complete change log, or rebuild the change log yourself before deciding.

### 5c. Rules compliance of the revised version

**What to evaluate:** Verify that the revised version meets all the Rules for the content type — not only the Rules that were identified as issues in the original, but all of them.

**What to look for:**
- For compliance rewrites: the fix for one Rule does not introduce a violation of another (for example, restructuring to remove blame sometimes removes the "what to do next" element)
- For voice rewrites: improving Human attribute does not reduce clarity to the point of failing the readability target
- For length rewrites: the cut log's confirmation that "all Rules requirements are still preserved" should be verified, not assumed

**What to do:** After evaluating the change log, apply the Module 2 pattern's Review Checklist to the revised version before using it. The change log evaluation and the Review Checklist are complementary — the change log tells you what changed and why; the checklist confirms the result meets the bar.

---

## 6. When to re-prompt

Use this section to decide what to do after completing the evaluation.

### Re-prompt: the output is not usable

Re-prompt when the output fails the minimum bar check (Section 1). Before re-prompting, identify the root cause:

- **Invented criteria:** Was the criterion missing from the grounding? If so, add it and re-prompt. If the criterion is not in the toolkit, do not add it — address it outside this workflow.
- **Guidance-level misclassification:** Verify the correct level in the source file, then add an explicit note in the grounding about that criterion's level before re-prompting.
- **Structural incompleteness:** Add an explicit instruction about the missing section or component to the OUTPUT FORMAT field.
- **Internal inconsistency:** If the output contradicts itself, the grounding may be ambiguous. Clarify the specific point before re-prompting.

### Re-prompt with refinement: the output is usable but limited

Consider re-prompting when:
- Generation options are not diverse enough (dimension 3b) — narrow the prompt and push for a specific contrast
- Coverage is incomplete (dimension 4b) — add a second pass for the missed items
- The change log is incomplete (dimension 5b) — ask explicitly for a complete change log before deciding

A re-prompt for refinement is worth it when the gap is specific and fixable with a clear instruction. If the gap is broad (most of the output is vague or ungrounded), a full re-prompt with improved grounding is more reliable than targeted corrections.

### Proceed with annotation: the output is usable with caveats

Proceed when the output passes the minimum bar check and the universal dimensions, and any type-specific gaps have been resolved or documented sufficiently to support the content decision. When you proceed with annotation:

- Record any criteria you verified against the source file
- Note any findings or annotations you judged to be vague and resolved yourself
- Keep the annotation alongside the output if it will be shared with another content designer or reviewed later

### Proceed: the output is usable

Proceed when the output passes the minimum bar check, the universal dimensions, and the type-specific criteria. Document your evaluation decision as part of your content review record — the output was evaluated against the rubric before the content decision was made.

---

## Related documents

- [AI content principles](ai-content-principles.md) — Pre-prompt checklist and responsible-use requirements
- [Grounding guide](grounding-guide.md) — How to structure grounding context to improve output quality
- [Prompt templates — README](prompt-templates/README.md) — Template anatomy and default constraints
- [Microcopy generation prompts](prompt-templates/microcopy-prompts.md)
- [Review prompts](prompt-templates/review-prompts.md)
- [Rewriting prompts](prompt-templates/rewriting-prompts.md)
- [Failure modes](failure-modes.md) — Specific AI failure patterns to watch for in this toolkit's outputs
- [Module 2 — UX writing standards](../02-ux-writing-standards/) — Source for grounding and verification
