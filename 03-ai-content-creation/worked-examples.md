# Worked examples

This file contains three end-to-end examples demonstrating the toolkit's AI-assisted content workflow. Each example covers grounding setup, a completed prompt, an illustrative AI output, and a walkthrough of the evaluation step.

The AI outputs in these examples are **illustrative** — they show what a realistic output looks like for evaluation purposes, including both correct applications of the grounding and deliberate weaknesses for the evaluation walkthrough to identify. They are not actual model outputs and do not represent what any specific AI system will produce.

**How to use this file.** Read each example alongside the template it uses and the relevant section of the [output evaluation rubric](output-evaluation-rubric.md). The evaluation walkthrough in each example applies the rubric directly — it shows the reasoning, not just the conclusions.

---

## Example 1: Microcopy generation — error messages

**Workflow stage:** Generate  
**Template used:** [Microcopy generation — error messages](prompt-templates/microcopy-prompts.md#1-error-messages)  
**Grounding used:** Reusable instructions + error messages pattern (Module 2)

---

### 1.1 Context

A content designer is working on a file upload component for a project management product. The component allows users to attach files to tasks. The designer needs error messages for two error states: a file type rejection and a file size limit.

The product's voice is Clear, Human, and Helpful — conversational without being casual. The established product terminology for the attachment area is "Files" — an illustrative placeholder used throughout this example. In practice, substitute the product's own established term.

---

### 1.2 Grounding setup

**Reusable instructions (excerpt — full template in [grounding-guide.md](grounding-guide.md#reusable-instructions-template)):**

> Voice attributes: Clear (plain language, direct, no jargon), Human (acknowledge the user's situation, use natural phrasing), Helpful (tell the user what to do next, not just what went wrong).  
> Writing standards: Direct (lead with what matters, avoid throat-clearing), Consistent (use established product terminology).  
> Guidance level framework: Rule (must follow, no exceptions), Recommendation (should follow, exceptions require judgment), Contextual (situation-dependent, designer's judgment).

**Reference context supplied:** Module 2 — Error messages pattern (Rules, Recommendations, anatomy, accessibility requirements).

---

### 1.3 Completed prompt

    Generate error messages for a file upload component. Present 2 options for each
    error state.

    CONTENT TYPE: Error messages — Module 2 error messages pattern

    ERROR STATES:
    1. File type rejected — the user has attempted to upload a file type that is not
       supported (supported types: .pdf, .png, .jpg, .docx)
    2. File too large — the user has attempted to upload a file that exceeds the size
       limit (limit: 25 MB)

    OBJECT: Files (not "attachments" or "uploads" — this is the established product
    term in this example; replace with the product's own term)

    PRODUCT CONTEXT: [Product] is a project management product for small teams. The
    voice is Clear, Human, and Helpful — conversational but not casual. Users
    attaching files are typically mid-task; they did not expect the error and need to
    continue quickly.

    CONSTRAINTS:
    - Maximum 100 characters per message
    - Recovery path for file type: user must re-select a file in a supported format
    - Recovery path for file size: user must compress the file or use a different file;
      there is no product-side compression tool
    - Do not refer users to "support" — there is no in-product support path for this
      error

    For each option, provide an annotation identifying applicable Rules,
    Recommendations, and Contextual decisions, and explaining the trade-off between
    options.

    Label all outputs as options for human evaluation.

---

### 1.4 Illustrative AI output

*The following output is illustrative. It represents a realistic response to the prompt above, including one deliberate weakness for the evaluation walkthrough to identify.*

---

**Error state 1: File type rejected**

**Option 1A** *(option for human evaluation)*

> That file type isn't supported. Try uploading a .pdf, .png, .jpg, or .docx instead.

*Annotation:* Tells the user what went wrong and what to do next [Rule]. Does not blame the user [Rule]. Uses plain language [Rule]. Lists accepted types as the recovery path [Recommendation: be specific about what went wrong]. Uses sentence case [Recommendation]. The Human attribute is light here — the message is functional and clear but does not acknowledge the user's situation. That is a Contextual decision: for a mid-task upload error, a brief functional message may be appropriate.

**Option 1B** *(option for human evaluation)*

> [Product] doesn't support that file type. You can add .pdf, .png, .jpg, or .docx files.

*Annotation:* Same Rule compliance as 1A. Uses the product name rather than "we" — this is a Contextual decision: naming the product can read as distancing; "we" is warmer. "You can add" is slightly softer than 1A's "Try uploading" — the trade-off is between direct recovery instruction (1A) and a more natural phrasing (1B). Uses "files" consistent with product terminology [writing standard: Consistent].

---

**Error state 2: File too large**

**Option 2A** *(option for human evaluation)*

> This file is too large to add. Files must be 25 MB or smaller.

*Annotation:* States what went wrong (file too large) and what the limit is [Recommendation: be specific]. Does not state what to do next — there is no explicit recovery step. This is a Rule gap: the error messages pattern requires a next step. A recovery step for this error state might be: "Compress the file or choose a different one." Rule gap noted for human evaluation.

**Option 2B** *(option for human evaluation)*

> This file exceeds the 25 MB limit. Compress it or choose a different file to continue.

*Annotation:* States what went wrong (exceeds limit), gives the specific limit, and provides a recovery step (compress or choose a different file) [Rule: tell the user what to do next]. Does not blame the user [Rule]. "To continue" acknowledges that the user is mid-task. 86 characters — within the 100-character limit. No invented recovery paths — both options mentioned (compress, choose different file) were supplied in the CONSTRAINTS field.

---

### 1.5 Evaluation walkthrough

**Step 1 — Minimum bar check**

Applying [Section 1 of the output evaluation rubric](output-evaluation-rubric.md#1-minimum-bar-check):

**1a. Invented criteria:** No criteria appear in the annotations that are not in the supplied grounding. The annotations reference the error messages Rules, the voice attributes, and the writing standards — all supplied. ✓

**1b. Guidance-level misclassification:** The Contextual call in 1A's annotation (brief functional message for mid-task context) is correctly identified as Contextual. The Recommendation for specificity is correctly identified as a Recommendation. ✓

**1c. Structural completeness:** Option 2A is flagged in its own annotation as missing a next step (Rule). The annotation correctly identifies this as a Rule gap rather than passing over it. The annotation does not incorrectly label it as a Recommendation. ✓ — the flag is present and correctly typed.

**1d. Internal inconsistency:** No inconsistencies between options or between annotations and options. ✓

Minimum bar: passed for 1A, 1B, and 2B. Option 2A fails the minimum bar on structural completeness — it is missing a Rule-required component. **Decision: re-prompt 2A or use 2B.**

**Step 2 — Universal evaluation (selected dimensions)**

**2a. Grounding fidelity:** The annotations correctly scope the error messages Rules. No widening or narrowing of criteria. ✓

**2b. Guidance-level accuracy:** The Contextual calls are both justified with situational factors (mid-task context; product name vs. "we"). The Recommendation for specificity is correctly scoped. ✓

**2c. Structural completeness:** 2A missing the next-step Rule. Already flagged. 1A and 1B both include what went wrong and what to do next.

**Step 3 — Generation-specific evaluation**

**3a. Factual plausibility:** No invented states, paths, or timeframes. Recovery paths (compress, choose different file) match the CONSTRAINTS field. ✓

**3b. Option diversity:** 1A and 1B differ in structure ("That file type isn't supported" vs. "[Product] doesn't support that file type") and in phrasing of the recovery step. The annotation explains the trade-off. ✓ — not near-identical options.

**3c. Output framing:** Options are labelled "for human evaluation" throughout. ✓

**Step 4 — Decision**

- Options 1A and 1B: **Proceed** — both pass minimum bar and universal dimensions. The designer chooses based on the Contextual call (voice warmth vs. directness of recovery step).
- Option 2A: **Re-prompt** — missing Rule-required next step. Use 2B as the basis for the revised prompt if needed.
- Option 2B: **Proceed** — passes all dimensions.

**Relevant failure mode:** [2.1 Invented product states](failure-modes.md#21-invented-product-states) — none found in this output. The absence of invented states reflects the specific CONSTRAINTS field supplying the recovery paths explicitly.

---

## Example 2: Voice alignment review — button labels

**Workflow stage:** Review  
**Template used:** [Voice alignment review](prompt-templates/review-prompts.md#1-voice-alignment-review)  
**Grounding used:** Reusable instructions + voice principles (Module 1)

---

### 2.1 Context

The same content designer is reviewing button labels for the product's onboarding flow. The labels have been written by a developer and are functionally correct — they describe the action — but the design lead has flagged that they sound generic and do not reflect the product's voice. The designer runs a voice alignment review before deciding which labels to revise.

**Labels under review:**

1. Get started
2. Skip for now
3. Set up your workspace
4. Invite team members
5. Go to dashboard

---

### 2.2 Grounding setup

**Reusable instructions:** Same as Example 1.

**Reference context supplied:** Module 1 — Voice principles (voice attributes and illustrative examples; tone guidance by context).

No Module 2 pattern is supplied for this review — the designer is evaluating voice only, not pattern compliance. If pattern compliance is also needed, that is a separate review using the pattern compliance review template.

---

### 2.3 Completed prompt

    Review the following button labels for alignment with the product's voice attributes.
    Present findings as a structured evaluation for human decision-making.

    CONTENT TO REVIEW:
    1. Get started
    2. Skip for now
    3. Set up your workspace
    4. Invite team members
    5. Go to dashboard

    CONTENT TYPE: Button labels — onboarding flow, project management product

    PRODUCT CONTEXT: [Product] is a project management product for small teams. The
    voice is Clear, Human, and Helpful — conversational but not casual. The onboarding
    flow is a first-use experience; users are setting up for the first time and may be
    unfamiliar with the product. The tone for first-use contexts should be welcoming
    without being excessive.

    For each voice attribute and writing standard (Clear, Human, Helpful, Direct,
    Consistent), state whether findings were identified. Where no issues were found,
    state that explicitly. Present findings as a structured evaluation for human
    decision-making. Do not state whether the content is ready to publish.

    Label all outputs as a structured evaluation for human review.

---

### 2.4 Illustrative AI output

*The following output is illustrative. It represents a realistic voice alignment review, including one deliberate weakness for the evaluation walkthrough to identify.*

---

*Structured evaluation for human review*

**Clear**

Finding — Label 3: "Set up your workspace"

"Set up" is a correct plain-language instruction, but "your workspace" may not be meaningful to a new user who has not yet interacted with the product. If the product uses "workspace" as an established term visible elsewhere in the UI, this label is clear. If not, the term may require prior knowledge the user does not yet have at this onboarding stage.

Guidance level: Contextual — depends on whether "workspace" is established product terminology the user has already encountered in this flow.

**Human**

Finding — Label 1: "Get started"

"Get started" is a generic onboarding phrase that appears across many products. It does not reflect a specific, situated welcome into the product. For a first-use context where tone should be welcoming, the Human attribute suggests acknowledging that the user is beginning something specific, not just beginning.

Guidance level: Contextual — "Get started" is functional and widely understood; the concern is voice alignment, not compliance.

Finding — Label 2: "Skip for now"

"Skip for now" implies the user is deferring something — that is accurate — but the phrasing positions the choice as a temporary workaround rather than a valid option. For a product that values the Human attribute, a label that acknowledges the user's choice more neutrally may be worth considering.

Guidance level: Contextual — the phrasing is not incorrect; this is a voice observation for the designer's judgment.

**Helpful**

No issues identified. Labels 3, 4, and 5 all describe the action the button performs without ambiguity. The user knows what will happen on click.

**Direct**

No issues identified. No throat-clearing or preamble. All labels lead with the action.

**Consistent**

Finding — Labels 1 and 5 against the product context:

"Dashboard" in Label 5 ("Go to dashboard") should be verified against the product's established UI terminology. If the product's navigation uses a different term for this area (e.g., "Home", "Overview"), the label introduces an inconsistency the user will notice when they arrive.

Guidance level: Contextual — if "dashboard" is the product's own term, no issue. If not, this is a Consistent writing standard concern.

**Summary**

Three Contextual observations identified across Clear (1), Human (2), and Consistent (1). No Rule violations or Recommendation observations. The labels are functionally correct. The observations are for the designer's judgment — none requires a change.

---

### 2.5 Evaluation walkthrough

**Step 1 — Minimum bar check**

**1a. Invented criteria:** No external criteria appear. All findings are grounded in the voice attributes and writing standards supplied. ✓

**1b. Guidance-level misclassification:** All four findings are correctly identified as Contextual, with situational factors given for each. No Contextual decisions are presented as Rules or Recommendations. ✓

**1c. Structural completeness:** All five attributes and standards are addressed. "No issues identified" is stated explicitly for Helpful and Direct — the two with no findings. ✓

**1d. Internal inconsistency:** The summary count does not match the findings: it says three Contextual observations, but Clear (1) + Human (2) + Consistent (1) = four. **Minimum bar failure: internal inconsistency in the summary count.**

Minimum bar: failed on 1d. The inconsistency is a summary counting error — the findings themselves are present and consistent. **Decision: correct manually and re-check.** This is a mechanical counting error that the designer can verify directly. Correct the summary from three to four, then repeat the internal-consistency check. Re-prompting is unnecessary if the correction is straightforward and no substantive finding needs to change.

**Manual correction:** Clear 1 + Human 2 + Consistent 1 = 4 Contextual observations. The summary should read "Four Contextual observations identified." The designer can correct this directly without re-prompting.

**Step 2 — Universal evaluation (selected dimensions)**

**2a. Grounding fidelity:** No scope widening. The Consistent observation correctly limits itself to a Contextual question about terminology rather than declaring a violation. ✓

**2b. Guidance-level accuracy:** All Contextual calls include situational factors. ✓

**2c. Structural completeness:** All five attributes covered with explicit "no issues identified" for those without findings. ✓ (pending correction of the summary count).

**Step 3 — Review-specific evaluation**

**3a. Finding traceability:** Each finding quotes the specific label and names the attribute. ✓

**3b. Coverage:** All five labels are addressed — Labels 3, 4, and 5 are covered under their relevant attributes (Clear for 3, Helpful for 3/4/5, Consistent for 5). ✓

**3c. Verdict vs. evaluation:** The output does not state whether the labels are ready to publish. The summary correctly frames findings as "for the designer's judgment." ✓

**Step 4 — Decision**

After manual correction of the summary count: **Proceed with annotation** — the output passes the minimum bar check on all dimensions except the summary count, which the designer has corrected. The Contextual observations are well-evidenced and actionable.

**Relevant evaluation criterion:** [1d Internal inconsistency](output-evaluation-rubric.md#1-minimum-bar-check). No corresponding failure mode is documented in `failure-modes.md`; this example demonstrates a recoverable consistency error caught by the rubric.

---

## Example 3: Compliance rewrite — error message

**Workflow stage:** Rewrite  
**Template used:** [Compliance rewrite](prompt-templates/rewriting-prompts.md#1-compliance-rewrite)  
**Grounding used:** Reusable instructions + error messages pattern (Module 2)

---

### 3.1 Context

Building on Example 1: Option 2A was identified as missing a Rule-required next step. The designer has decided to revise the message rather than use 2B, because the base phrasing of 2A ("This file is too large to add") is preferred by the design lead. A compliance rewrite is used to produce a revised version of 2A that adds the missing next step without changing the base phrasing.

**Original content (Option 2A from Example 1):**

> This file is too large to add. Files must be 25 MB or smaller.

**Issue identified in Example 1 review:**

Missing next step — the error messages Rule requires the user to know what to do next. The original states the problem and the limit but gives no recovery path.

---

### 3.2 Grounding setup

**Reusable instructions:** Same as Examples 1 and 2.

**Reference context supplied:** Module 2 — Error messages pattern. Same grounding used in Example 1 — the revision can only address the criteria that were in the original review's grounding.

---

### 3.3 Completed prompt

    Revise the following content to address the identified issue. Present 2 revised
    versions for human evaluation.

    ORIGINAL CONTENT:
    This file is too large to add. Files must be 25 MB or smaller.

    CONTENT TYPE: Error messages — Module 2 error messages pattern

    IDENTIFIED ISSUES:
    Missing next step. The error messages Rule requires the message to tell the user
    what to do next. The original states what went wrong (file too large) and the limit
    (25 MB) but gives no recovery path. Recovery path: compress the file or choose a
    different one (no product-side compression tool is available).
    Guidance level: Rule.

    REVISION SCOPE: Address the Rule violation — add a recovery step. Do not change
    the base phrasing ("This file is too large to add") unless required to meet the
    Rule.

    PRODUCT CONTEXT: [Product] — project management product, file upload component.
    Users are mid-task. Character limit: 100 characters including spaces.

    Apply the Rules and Recommendations from the supplied grounding context.
    For each change made, identify the applicable Rule, Recommendation, or Contextual
    decision from the supplied grounding. Do not invent criteria or assign guidance
    levels to decisions not covered by the supplied standards.

    OUTPUT FORMAT: Present each revised version as a numbered item. For each revised
    version, include:
    - The revised content (complete)
    - A change log: for each change, quote the original text, state the revised text,
      name the criterion addressed, confirm whether the change is required (Rule) or
      for consideration (Recommendation or Contextual), and indicate whether the change
      directly addresses the identified issue or is a supporting edit.

    Label all outputs as revised versions for human evaluation.

---

### 3.4 Illustrative AI output

*The following output is illustrative. It represents a realistic compliance rewrite output.*

---

**Revised version 1** *(revised version for human evaluation)*

> This file is too large to add. Compress it or choose a different file to continue.

*Change log:*

| Original | Revised | Criterion | Guidance level | Change type |
|---|---|---|---|---|
| "Files must be 25 MB or smaller." | "Compress it or choose a different file to continue." | Error messages Rule: tell the user what to do next | Rule | Directly addresses identified issue |

Note: "Files must be 25 MB or smaller" has been replaced by the recovery step. The size limit is no longer stated explicitly — the revised version prioritises the next step over restating the limit. If stating the limit is considered important for the user's understanding, Revised version 2 preserves both.

Character count: 82 characters. ✓

**Revised version 2** *(revised version for human evaluation)*

> This file is too large. Files must be 25 MB or smaller. Compress it or choose another file.

*Change log:*

| Original | Revised | Criterion | Guidance level | Change type |
|---|---|---|---|---|
| "This file is too large to add." | "This file is too large." | No criterion requires "to add" — removed to shorten the base clause | Contextual | Supporting edit (improves flow; no Rule or Recommendation requires the phrase) |
| "Files must be 25 MB or smaller." | "Files must be 25 MB or smaller. Compress it or choose another file." | Error messages Rule: tell the user what to do next; Recommendation: be specific about what went wrong | Rule + Recommendation | Directly addresses identified issue (recovery step added); supporting edit (limit retained as supplied in CONSTRAINTS) |

Character count: 91 characters. ✓ (within 100-character limit)

---

### 3.5 Evaluation walkthrough

**Step 1 — Minimum bar check**

**1a. Invented criteria:** No invented criteria. Version 1's change log references the recovery-step Rule. Version 2 references both that Rule and the specificity Recommendation. Both classifications are supported by the supplied grounding. ✓

**1b. Guidance-level misclassification:** Version 1's change log correctly labels the recovery step addition as a Rule. Version 2 correctly labels the Rule component and the Recommendation component separately. ✓

**1c. Structural completeness:** Both revised versions include: what went wrong (stated in the original base phrasing, preserved), and what to do next (added by the revision). ✓

**1d. Internal inconsistency:** No inconsistencies between the revised content and the change logs. Version 1's note (size limit removed) accurately describes what changed. ✓

Minimum bar: passed.

**Step 2 — Universal evaluation (selected dimensions)**

**2a. Grounding fidelity:** The change logs scope changes to the identified issue and one supporting edit. No criteria invented. ✓

**2b. Guidance-level accuracy:** Correctly distinguishes Rule (recovery step) from Recommendation (specificity/limit retention). ✓

**2c. Structural completeness (rewriting):** Both change logs distinguish direct-issue changes from supporting edits, as the template requires. ✓

**Step 3 — Rewriting-specific evaluation**

**3a. Scope discipline:** Revised version 1 makes one change (replace limit statement with recovery step). Revised version 2 makes one change (integrate recovery step while retaining the limit). Both stay within the REVISION SCOPE. ✓

**3b. Change log completeness:** Each change is quoted (original text), stated (revised text), attributed to a criterion, labelled by guidance level, and typed as direct or supporting. ✓

**3c. Rules compliance check on revised versions:** Both revised versions include what went wrong (file too large — in the base phrasing), what to do next (recovery step), and do not blame the user. Both are within the character limit. ✓

**Step 4 — Decision**

Both revised versions: **Proceed** — both pass all evaluation dimensions.

**Designer's decision:** The choice between versions 1 and 2 is a content decision, not a compliance issue. Version 1 is shorter and prioritises the recovery step; Version 2 retains the size limit for users who want to know why the file was rejected. The designer's judgment applies — the rubric does not prescribe a preference between compliant versions.

**Relevant failure modes:**
- [4.1 Scope creep](failure-modes.md#41-scope-creep) — not present. Neither version changes the base phrasing beyond what the identified issue requires.
- [4.2 Rules regression](failure-modes.md#42-rules-regression-after-rewriting) — not present. The Rules check confirms both versions preserve what went wrong and add the missing next step.

---

## Related documents

- [AI content principles](ai-content-principles.md) — Pre-prompt checklist referenced before each example
- [Grounding guide](grounding-guide.md) — Reusable instructions template used in all three examples
- [Prompt templates — README](prompt-templates/README.md)
- [Microcopy generation prompts](prompt-templates/microcopy-prompts.md) — Template used in Example 1
- [Review prompts](prompt-templates/review-prompts.md) — Template used in Example 2
- [Rewriting prompts](prompt-templates/rewriting-prompts.md) — Template used in Example 3
- [Output evaluation rubric](output-evaluation-rubric.md) — Applied in all three evaluation walkthroughs
- [Failure modes](failure-modes.md) — Cross-referenced at the end of each walkthrough
- [Module 1 — Voice principles](../01-foundations/voice-principles.md)
- [Module 2 — UX writing standards](../02-ux-writing-standards/)
