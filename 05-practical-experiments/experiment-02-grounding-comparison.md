# Experiment 02 — Grounding Comparison

How outputs differ between equivalent tasks with different levels of grounding specification.

## Contents

- [1. Research question](#1-research-question)
- [2. Hypothesis](#2-hypothesis)
- [3. Test scenario](#3-test-scenario)
- [4. Materials](#4-materials)
- [5. Procedure](#5-procedure)
- [6. Observations](#6-observations)
- [7. Evaluation](#7-evaluation)
- [8. Limitations](#8-limitations)
- [9. Recommendations](#9-recommendations)

---

## 1. Research question

How do outputs differ between equivalent tasks with different levels of grounding specification?

---

## 2. Hypothesis

AI outputs generated from underspecified prompts will be generic, non-actionable, and misaligned with product and audience context — requiring human practitioners to supply the specificity the prompt did not provide. Outputs generated from grounded prompts will be more specific and actionable but will introduce verifiable claims that require human fact-checking, including claims that go beyond the grounding materials provided.

The nature and scope of human oversight will differ between the two conditions: underspecified output requires revision to add missing specificity; grounded output requires verification of the specificity that was produced. Neither condition eliminates the need for a human output evaluation pass — grounding shifts where human effort is required, not whether it is required.

---

## 3. Test scenario

**Task:** Write an error message for a file upload failure caused by an oversized file.

**Screen context:** A file upload interface within a generic document management application. The message appears inline, below the upload control, when the user attempts to upload a file that exceeds the size limit.

**Two conditions:** The same task is given to AI under two different levels of grounding specification — Condition A (underspecified) and Condition B (grounded). The task type, screen context, and content goal are identical in both conditions; only the grounding specification differs.

**Relationship to Experiment 01:** Experiment 01 tested voice consistency across a multi-piece content set produced under similar grounding conditions. This experiment tests what happens when grounding quality varies for a single content task — a more fundamental question about input quality and its effect on output specificity.

---

## 4. Materials

| Document | Role |
|---|---|
| `03-ai-content-creation/grounding-guide.md` | Establishes grounding principles, grounding specification framework, and common grounding failures |
| `03-ai-content-creation/prompt-templates/microcopy-prompts.md` | Provides prompt structures for microcopy tasks including error messages |
| `03-ai-content-creation/output-evaluation-rubric.md` | Provides the evaluation dimensions applied to both outputs |

**Evaluation dimensions:** This experiment applies the Phase 4 output evaluation rubric to both outputs. The rubric assesses accuracy, voice alignment, audience fit, task completion, and concision. Because the two conditions use different grounding levels, some rubric dimensions will produce different types of findings — Condition A findings are primarily about absence of specificity; Condition B findings are primarily about the accuracy of specificity that was produced.

---

## 5. Procedure

How the illustrative case is constructed, examined, and evaluated, step by step:

1. **Construct the underspecified prompt (Condition A)** — a minimal prompt that describes the task and content type without product context, audience context, voice reference, or specific parameters.
2. **Construct the grounded prompt (Condition B)** — a prompt for the same task, supplemented with product-specific parameters, audience context, available alternative actions, and a voice reference.
3. **Construct illustrative outputs for both conditions** — representing possible characteristics of content produced under each prompt condition, labelled as illustrative.
4. **Identify any additions in the Condition B output that were not present in the grounding materials** — this tests whether the grounded output stays within what was provided or introduces ungrounded specificity.
5. **Evaluate both outputs against the Phase 4 rubric** — applying each dimension and documenting findings.
6. **Identify human intervention required for each condition** — what a practitioner would need to do with each output before it could be used.
7. **Compare the nature and scope of intervention** — documenting where human effort moves, not only whether it is reduced.

---

## 6. Observations

What the application of the method identifies, including deliberate weaknesses, evaluation findings, and human intervention points.

### 6.1 Condition A — Underspecified prompt

**Prompt:**

> Write an error message for when a user tries to upload a file that is too large.

*Illustrative output — constructed to demonstrate the characteristics of AI-generated content produced without grounding specification.*

**Output A:**

> File upload failed. The file you have selected exceeds the maximum file size limit. Please reduce the file size and try again.

**Characteristics noted before evaluation:**
- States that upload failed but does not state what the limit is
- "exceeds the maximum file size limit" contains a redundancy ("maximum" and "limit" are synonymous)
- "Please reduce the file size" describes the goal without describing any available action
- "try again" gives the user no information about what to try differently
- Register is formal and unspecified; does not reflect a specific product voice

---

### 6.2 Condition B — Grounded prompt

**Grounding specification provided:**

| Element | Content provided |
|---|---|
| File size limit | 50 MB |
| Audience | Small business owners; not technical; may be uploading for the first time |
| Alternative actions available | Compressing the file before uploading; uploading a link to the document instead of the file itself |
| Voice reference | "Plain language. Tell people what to do, not what they cannot do. Keep it short." |
| Approximate word target | Approximately 30 words |

**Prompt:**

> Write an error message for when a user tries to upload a file that exceeds the size limit. Use the grounding specification above.

*Illustrative output — constructed to demonstrate the characteristics of AI-generated content produced with explicit grounding specification. A deliberate weakness has been introduced as noted.*

**Output B:**

> This file is too large to upload. Files must be 50 MB or smaller. Try compressing it, split it into smaller sections, or upload a link to the document instead.

**Deliberate weakness introduced:** "Split it into smaller sections" was not included in the grounding specification. This is a plausible alternative action that the AI introduced beyond the provided grounding materials. It may or may not reflect an action the product supports or recommends. This failure mode — where a grounded output introduces additional specificity that was not supplied — is noted here and examined in Section 6.4.

---

### 6.3 Evaluation against the Phase 4 output evaluation rubric

| Dimension | Output A assessment | Output B assessment |
|---|---|---|
| **Accuracy** | Accurate but incomplete — the statement that the file "exceeds the maximum file size limit" is true but omits the limit itself, making the message accurate in a way that provides no useful information | Partially accurate — the 50 MB limit and two of the three alternatives are grounded; "split it into smaller sections" is unverified and may be inaccurate for this product |
| **Voice alignment** | Does not meet — formal and passive; does not reflect any specific product voice; "you have selected" and "please reduce" are not consistent with any grounding-established register | Partially meets — "this file is too large" and the imperative alternatives are plain and direct; overall register is consistent with the voice reference |
| **Audience fit** | Does not meet — does not address a non-technical audience; no concrete action; assumes the user knows how to "reduce the file size" | Meets — alternatives are concrete and accessible; no technical terminology; suited to a user uploading for the first time |
| **Task completion** | Does not meet — user is told upload failed and that the file is too large; no actionable path to completing the task | Partially meets — alternatives are concrete and accessible, but one alternative was not present in the grounding materials and requires product verification before the message can be treated as fully actionable |
| **Concision** | Approximately 20 words; appropriate length, but the words carry limited information | Approximately 30 words; meets the approximate word target; each word carries a specific piece of information |

---

### 6.4 Addition beyond grounding materials

Output B included "split it into smaller sections" — an alternative action not present in the grounding specification.

This is the most important evaluation finding from Condition B. The grounded prompt produced clear improvement in three rubric dimensions (voice alignment, audience fit, and task completion — with caveats on the last). Accuracy shows a mixed result: Output B includes verified specificity the ungrounded output lacked, but also an unverified claim. Concision shows no clear difference between conditions; both outputs are reasonably concise relative to their respective requirements. And Output B produced a specific claim that cannot be verified against the grounding materials provided.

The finding creates two implications for human oversight:

1. **The practitioner must check the output not only against the grounding materials, but against the product itself.** Matching output to grounding materials is a necessary but not sufficient step. If the grounding materials are incomplete, or if the AI adds beyond them, the output may contain inaccurate specificity.

2. **A grounded output that looks more authoritative requires more careful fact-checking, not less.** Output A's vagueness ("reduce the file size") is immediately recognisable as incomplete and will be revised. Output B's specificity ("split it into smaller sections") looks like a helpful, complete answer — and is therefore more likely to pass a cursory review without the unverified claim being caught.

Before Output B can be used, the practitioner must confirm: (a) that the product actually supports splitting files into smaller sections as a workaround, and (b) whether recommending it is consistent with the product's own guidance. If neither is true, that alternative must be removed.

---

### 6.5 Human intervention required

| | Output A | Output B |
|---|---|---|
| **Nature of intervention** | Supplying all missing specificity — the limit, the available alternatives, and a consistent register | Fact-checking specific claims — particularly the unverified alternative; confirming the limit and stated alternatives are accurate |
| **Scope of intervention** | Substantial — the output requires a full revision pass to add the context the prompt did not supply | Targeted — the output is largely usable; intervention includes confirming the file size limit and both grounded alternatives against the product, in addition to resolving the unverified addition |
| **Primary risk if used without review** | Omission and non-actionability — the message provides no concrete path forward; this gap is immediately visible and would likely be caught before publication | Introducing an unsupported instruction that appears authoritative — specific claims look credible and may pass a surface review without the unverified content being caught |
| **Checkpoint most relevant** | Quality review: the reviewer must add specificity the output lacks | Quality review: the reviewer must verify claims the output introduced |

**Key observation:** Grounding does not reduce the need for a human output evaluation pass. It changes what that pass needs to do. Where Output A requires the reviewer to add, Output B requires the reviewer to verify — and the verification is less visible because the specific claims look credible.

---

## 7. Evaluation

### What the experiment demonstrates

The comparison illustrates the core value of grounding: a grounded prompt produced an output that was more specific, more actionable, and more appropriate for the target audience than an equivalent underspecified prompt. Three rubric dimensions showed clear improvement between conditions (voice alignment, audience fit, and task completion — with caveats). Accuracy showed a mixed result, and concision showed no clear difference.

### What grounding does not eliminate

The experiment also illustrates a limitation of grounding that is easy to overlook: a grounded prompt does not constrain the AI to producing only what was provided. Output B introduced a specific alternative action not present in the grounding materials. This introduced a factual claim requiring verification that the ungrounded Output A did not introduce — because Output A was too vague to make any specific claim that could be wrong.

This is not an argument against grounding. It is an argument for understanding what grounding does: it moves the output from generic to specific. Specific outputs are more useful but also more accountable. The practitioner's responsibility at the output evaluation stage changes accordingly.

### The locus of human work

The comparison makes visible a consistent pattern: human effort is required at the output evaluation stage regardless of grounding level, but the nature of that effort differs. For underspecified output, the reviewer is an author — supplying what is missing. For grounded output, the reviewer is a fact-checker — verifying what was produced. Both are human responsibilities that cannot be delegated to AI assessment alone.

This has a practical implication for how output evaluation is scoped. When working with grounded prompts, the evaluation checklist should include an explicit step: confirm that all specific claims in the output are present in the grounding materials, and check any that are not against the product itself.

### Rubric dimension most affected by grounding level

The evaluation dimension that most visibly differentiates the two constructed outputs was **task completion** — specifically, whether the output gave the user an actionable path to completing their task. This is the dimension that most directly reflects the absence or presence of product-specific context. Generic outputs can describe a goal ("reduce the file size") without providing a path; grounded outputs can specify the path ("try compressing it") — but the path must be verified.

---

## 8. Limitations

**Illustrative outputs**

Both outputs were constructed to demonstrate specific characteristics. This experiment cannot establish what AI systems would produce under equivalent conditions with these prompts, or how consistently grounded prompts outperform underspecified ones. The comparison is an illustration of two output types and the evaluation method applied to them.

**Grounding specification as a practitioner judgment**

The grounding specification in Condition B was deliberately well-formed — it included all the elements Phase 4's grounding guide identifies as important. Real-world grounding documents may be less complete, partially accurate, or inconsistently applied. The gap between Condition A and Condition B in this experiment represents an idealised improvement; partial grounding would produce partial improvement.

**Single content type**

Error messages are a specific content type with particular characteristics: they carry factual product claims (a file size limit, available actions), have an identifiable audience context (the user has just experienced a failure), and have a clear goal (help the user proceed). The grounding-to-specificity relationship demonstrated here may play out differently for content types where grounding matters less (structural copy, navigational labels) or differently (campaign content, where voice and audience matter more than factual specificity).

**Two-condition design**

This experiment compares one underspecified and one grounded condition. It does not examine partial grounding (some context provided but not all), grounding with inaccurate information, or the effect of grounding specification quality on output quality over multiple tasks.

**Grounding materials treated as authoritative**

The grounding specification in Condition B — including the 50 MB file size limit and the two available alternative actions — is treated as accurate within this constructed scenario. Their factual accuracy against an actual product is not independently tested. Traceability to grounding materials and factual accuracy in the real product are related but not identical: an output can be fully grounded and still require product verification if the grounding materials themselves are incomplete or incorrect.

---

## 9. Recommendations

### 1. Treat grounding specification as Stage 02 work

Grounding materials — the product context, audience definition, voice reference, and task parameters that will anchor AI-assisted generation — should be identified and documented during Stage 02 (brief completion), not assembled at Stage 03 (content creation). Grounding that is put together at the point of generation is more likely to be incomplete or inconsistent across a content set.

*Toolkit implication:* The content brief template already includes an audience section, requirements section, and glossary. A short "grounding materials" field under Stage 02 preparation — listing the specific documents, examples, and parameters to include in AI prompts for this task — would make grounding specification a standard brief activity rather than an ad hoc one.

### 2. Add a grounding adequacy check before the output evaluation pass

Before applying the output evaluation rubric, confirm that the prompt was adequately grounded. If the grounding was incomplete, the output evaluation pass will find gaps that reflect the prompt rather than the AI output. When this happens, the practitioner should first identify whether the gap comes from missing grounding. Depending on the issue and the workflow, the response may be to supplement the grounding and regenerate, or to revise the output directly. Identifying grounding gaps before evaluation makes this decision clearer.

*Toolkit implication:* The output evaluation rubric could include a pre-evaluation step: confirm the grounding materials used, and assess whether they were sufficient for the content type before evaluating the output itself.

### 3. Check grounded outputs for additions beyond the grounding materials

The standard verification step for grounded output should include confirming that specific claims in the output are traceable to the grounding materials provided — and that any additions are checked against the product before use. This step is easy to overlook because specific claims look authoritative; that is precisely when they most need checking.

*Toolkit implication:* The worked examples in `03-ai-content-creation/worked-examples.md` demonstrate individual output evaluation steps. This experiment suggests adding an explicit note in the output evaluation section on checking for ungrounded additions — a risk specific to grounded prompting that underspecified prompting does not introduce in the same way.

### 4. Document grounding materials as reusable assets

For recurring content types — error messages, confirmation toasts, empty states — the grounding specification developed for one task should be documented and reused. This reduces the effort of grounding specification for subsequent tasks and ensures consistency in what is provided to AI across a content type.

*Toolkit implication:* This is consistent with the content brief's glossary and reference sections. For teams with recurring content types, one possible approach is to document grounding materials as a shared resource — approved product context, voice examples, and parameter specifications by content type — which would reduce the per-task setup cost of grounded generation. This is a team practice to consider where the content volume and recurring types make the upfront investment worthwhile, not a requirement for all teams.
