# Rewriting prompts

This file contains three prompt templates for rewriting existing content: a compliance rewrite to address identified issues, a voice rewrite to align copy with the product's established voice, and a length rewrite to meet a specific brevity or character constraint. Each template produces one or two revised versions for human evaluation — not final, ready-to-publish copy.

Before using any template, work through the [pre-prompt constraint checklist](../ai-content-principles.md#pre-prompt-constraint-checklist) and ensure your grounding context is in place. See [grounding-guide.md](../grounding-guide.md) for how to structure reusable instructions and reference context.

**What rewriting prompts do not replace.** A rewriting prompt can produce a revised version that addresses specific identified issues. It cannot decide which changes to make, what to prioritise, or whether the original was actually wrong. The content designer makes those determinations — the template helps execute them once the decision is made.

---

## 1. Compliance rewrite

**Purpose:** Revise existing copy to address issues identified in a pattern compliance review. Use when a review has produced a list of Rule violations and Recommendation observations, and you want one or two revised versions that bring the copy into compliance for human evaluation.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes (Clear, Human, Helpful), writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | The Module 2 pattern for the content type being revised: its Rules, Recommendations, anatomy, and accessibility requirements | The relevant file in [Module 2 — UX writing standards](../../02-ux-writing-standards/) |

Supply the same reference context used in the preceding review. The revision can only address the criteria that are in the grounding.

---

**Template:**

    Revise the following content to address the identified issues. Present [1 / 2]
    revised version(s) for human evaluation.

    ORIGINAL CONTENT:
    [Paste the original content here. If revising multiple items (for example,
    a set of error messages), include all items. Label each item clearly.]

    CONTENT TYPE: [Name the content type and Module 2 pattern being applied.
    For example: "Error messages — Module 2 error messages pattern"]

    IDENTIFIED ISSUES:
    [Paste or summarise the issues from the preceding review. For each issue,
    include the criterion from the grounding, its guidance level (Rule,
    Recommendation, or Contextual decision), and the specific text it concerns.
    Partial review output is acceptable — the revision will address only what is
    listed here.]

    REVISION SCOPE: [Specify what this revision covers. For example:
    "Address Rule violations only" / "Address all findings: Rules and Recommendations"
    / "Address the Rule violations; note which Recommendations are outstanding"]

    PRODUCT CONTEXT: [Describe the product and the component where this content
    appears. Include any constraints relevant to the revision — character limits,
    recovery options available to the user.]

    Apply the Rules and Recommendations from the supplied grounding context.
    For each change made, identify the applicable Rule, Recommendation, or Contextual
    decision from the supplied grounding. Do not invent criteria or assign guidance
    levels to decisions that are not covered by the supplied standards.

    OUTPUT FORMAT: Present each revised version as a numbered item. For each
    revised version, include:
    - The revised content (complete, not a diff)
    - A change log: for each change, quote the original text, state the revised text,
      name the criterion addressed (Rule, Recommendation, or Contextual decision),
      confirm whether the change was required (Rule) or for consideration
      (Recommendation or Contextual), and indicate whether the change directly
      addresses an identified issue or is a supporting edit for coherence or
      restructuring. For supporting edits, link to the relevant issue where possible.

    Label all outputs as revised versions for human evaluation.

---

**Output format:** One or two complete revised versions, each followed by a change log. The change log makes every revision traceable to a specific criterion and guidance level, so the content designer can evaluate the revision against the original without returning to the review output.

**Usage notes:**

- **Apply this template after a review, not instead of one.** A compliance rewrite works from an existing list of issues. If you have not yet reviewed the content, use the [pattern compliance review template](review-prompts.md#2-pattern-compliance-review) first to identify what needs to change, then use this template to produce the revision.
- **Rules take priority.** Address Rule violations before Recommendations. If the REVISION SCOPE is "Rules only", the change log should note any outstanding Recommendations so the content designer is aware of them, even if the revision does not address them.
- **One content item at a time.** For sets of items (multiple error messages, a series of notifications), revise each item in a separate prompt unless they share the same issues. Combining multiple distinct items in one prompt increases the risk of issues being applied to the wrong item.
- **A revision may need to change more than the flagged text.** Fixing a Rule violation sometimes requires restructuring a sentence or adjusting adjacent text for coherence. The change log should note any changes beyond those directly required by the identified issue.
- **Text-level revision cannot fix accessibility implementation.** Rewriting the text of an error message will not fix a missing `aria-describedby` attribute. If the review identified accessibility implementation issues, flag them separately for engineering review — do not attempt to address them through a text revision.

---

## 2. Voice rewrite

**Purpose:** Revise copy that is functionally correct — it meets applicable Rules and contains the right content — but does not reflect the product's established voice attributes. Use when copy sounds too generic, too formal, too casual, or otherwise out of character for the product, and you need a revised version for evaluation.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes (Clear, Human, Helpful), writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | The specific voice and tone guidance for the product, if established; tone variations by context | [Module 1 — Voice principles](../../01-foundations/voice-principles.md) |

The voice rewrite works from the voice attributes. If the content also has pattern compliance issues, address those first with the compliance rewrite — voice rewriting copy that also fails Rules produces a well-voiced but still non-compliant result.

---

**Template:**

    Revise the following content to better reflect the voice attributes in the
    supplied grounding. Present [1 / 2] revised version(s) for human evaluation.

    ORIGINAL CONTENT:
    [Paste the content here. Label each item if revising multiple pieces.]

    CONTENT TYPE: [Describe what this content is and where it appears. For example:
    "Error messages from a file upload component" / "Button labels for a destructive
    action confirmation dialog"]

    PRODUCT CONTEXT: [Describe the product and audience. For example: "A project
    management product for small creative teams. The voice is Clear, Human, and
    Helpful — conversational but not casual."]

    VOICE CONCERN: [Name the specific voice attribute or writing standard involved
    (Clear, Human, Helpful, Direct, or Consistent), and explain what the original
    copy does that works against it. For example: "The copy is functional but
    sounds clinical — it reads like a system log entry, not a message from a helpful
    product. It lacks the Human attribute: there is no acknowledgement of the user's
    situation, and the phrasing is passive throughout." / "The copy is trying to be
    friendly but undershoots the Clear attribute — the first sentence doesn't tell the
    user what happened."]

    PRESERVE: [Specify any elements that must be kept as written — a specific
    term, a required phrase, an approved link text, a legal notice. For example:
    "Keep the phrase 'unsaved changes' — this is the established product terminology."
    / "The link text 'Contact support' must remain unchanged."]

    Apply the voice attributes from the supplied grounding context.
    For each change made, identify the applicable voice attribute or writing standard
    from the supplied grounding. Do not invent criteria or assign guidance levels to
    decisions that are not covered by the supplied standards.

    OUTPUT FORMAT: Present each revised version as a numbered item. For each
    revised version, include:
    - The revised content (complete)
    - A voice decision log: for each change, quote the original text, state the
      revised text, name the voice attribute or writing standard it addresses (Clear,
      Human, Helpful, Direct, or Consistent), describe how the revision moves the
      copy closer to that attribute, and where the change involves a Contextual
      decision, identify it as Contextual and explain the situational factors behind
      the decision

    Label all outputs as revised versions for human evaluation.

---

**Output format:** One or two complete revised versions, each followed by a voice decision log. The log attributes each change to a specific voice attribute or writing standard, making the revision rationale explicit for the content designer's evaluation.

**Usage notes:**

- **Voice rewriting should not change meaning.** The compliance of the original — its Rules, its factual content, its structure — should be preserved. If the revision changes what the message communicates or removes information the user needs, that is a content decision, not a voice decision. Flag any such changes in the PRESERVE field before prompting, or evaluate them carefully in the output.
- **Be specific about the voice concern.** A VOICE CONCERN that says only "it doesn't sound right" will produce a generic revision. Name the specific attribute and what specifically the original does that works against it. The illustrative examples in [Module 1 — Voice principles](../../01-foundations/voice-principles.md) can help diagnose the issue.
- **Two attributes may be in tension.** The Human attribute (acknowledge the user's situation, use natural language) and the Clear attribute (direct, plain, unambiguous) can point in opposite directions for a short piece of copy. The revision may need to make a contextual call; note this in your evaluation.
- **Identify compliance issues first.** If you are uncertain whether the original meets the Rules, run a [pattern compliance review](review-prompts.md#2-pattern-compliance-review) before rewriting for voice. Revising voice in copy that also has Rule violations may inadvertently fix some issues while introducing others, and the change log will not reflect the compliance dimension.
- **The Consistent standard is cross-product.** An AI tool revising a single piece of copy cannot check consistency with terminology used elsewhere in the product. After a voice rewrite, verify that any new phrasing introduced by the revision does not conflict with established terminology.

---

## 3. Length rewrite

**Purpose:** Revise copy to meet a specific character limit or length target while preserving its meaning and Rules compliance. Use when existing copy is correct and appropriate in voice, but too long for the available space.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes (Clear, Human, Helpful), writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | The Module 2 pattern for the content type being shortened, including its Rules and any length-specific Recommendations | The relevant file in [Module 2 — UX writing standards](../../02-ux-writing-standards/) |

---

**Template:**

    Revise the following content to meet the specified length target while preserving
    its meaning and Rules compliance. Present [1 / 2] revised version(s) for human
    evaluation.

    ORIGINAL CONTENT:
    [Paste the content here. Label each item if revising multiple pieces.]

    CONTENT TYPE: [Name the content type and Module 2 pattern being applied.
    For example: "Error messages — Module 2 error messages pattern"]

    LENGTH TARGET: [Specify the constraint precisely. For example:
    "Maximum 80 characters including spaces" / "Maximum 2 sentences" /
    "One line at [n]-point type at [n]px wide" / "Fit within [n] words"]

    PRODUCT CONTEXT: [Describe the product and the component where this content
    appears. Include any context relevant to what can be shortened — for example,
    whether the user has access to supporting documentation, or whether a full
    explanation is available on a linked page.]

    PRESERVE: [Specify any elements that cannot be shortened or removed. For example:
    "Must retain the product's name as written" / "The recovery step ('Try again or
    contact support') must remain" / "Do not remove the specific error cause"]

    Apply the Rules and voice attributes from the supplied grounding context.
    Preserve the original's voice attributes and writing standards (Clear, Human,
    Helpful, Direct, Consistent) as well as its meaning and Rules compliance.

    If no version can meet the length target while preserving all Rule requirements,
    do not present a non-compliant shortened version as a solution. State that the
    target cannot be met compliantly. If useful, provide the nearest compliant
    revision separately, clearly labelled as exceeding the target.

    For each change made, identify whether it removes, consolidates, or rephrases
    content, and state what Rule, Recommendation, or Contextual decision — from the
    supplied grounding — governs the content that was changed.

    OUTPUT FORMAT: Present each revised version as a numbered item. For each
    revised version, include:
    - The revised content, with its word or character count
    - A cut log: for each change, state what was removed or shortened, why it was
      considered cuttable (what guidance-level decision it represents — Rule,
      Recommendation, or Contextual decision), identify any Contextual decisions and
      the situational factors that informed them, and confirm that all Rules
      requirements and voice attributes are still preserved in the revised version

    Label all outputs as revised versions for human evaluation.

---

**Output format:** One or two complete revised versions, each with a word or character count and a cut log. The cut log makes the trade-offs explicit: what was removed, what drove the decision, and whether all Rules requirements are preserved.

**Usage notes:**

- **Establish Rules compliance before shortening.** A length rewrite that starts with non-compliant copy may shorten out a Rule requirement. If you have not reviewed the original for compliance, run a [pattern compliance review](review-prompts.md#2-pattern-compliance-review) first.
- **Some targets cannot be met without a Rule violation.** The template instructs the AI to flag this rather than produce a compliant-looking but incomplete revision. If this happens, the content designer's options are: adjust the target, work with the UI team on more space, or accept a shorter version and note the trade-off. The AI output is the starting point for that conversation, not the end of it.
- **The cut log drives the evaluation.** A short revised version that looks fine may have dropped a Rule-required element (a next step, a specific error cause, a path forward). The cut log lets you verify what changed, not just compare the two versions side by side.
- **Shortening affects reading level.** Compression often introduces compound clauses ("Please sign in to continue and save your draft") or omits the context that makes the message readable. After shortening, check the revised version against the readability target for the content type.
- **Length rewrites can produce over-compressed copy.** An AI told to cut to 80 characters will cut to 80 characters. Evaluate the revised version against the original's voice and Rules compliance, not only its character count. A version that meets the target but drops the Human attribute or removes the next step is not an improvement.

---

## Related documents

- [Prompt templates — README](README.md) — Template anatomy, grounding requirements, and default constraints
- [Review prompts](review-prompts.md) — Identify issues before rewriting
- [Microcopy generation prompts](microcopy-prompts.md) — Generate from scratch rather than revising
- [Grounding guide](../grounding-guide.md) — How to structure reusable instructions and reference context before using these templates
- [AI content principles](../ai-content-principles.md) — Pre-prompt checklist and responsible-use requirements
- [Output evaluation rubric](../output-evaluation-rubric.md) — How to evaluate the revised versions these templates produce
- [Failure modes](../failure-modes.md) — What to watch for in AI rewriting outputs specifically
- [Module 1 — Voice principles](../../01-foundations/voice-principles.md)
- [Module 2 — UX writing standards](../../02-ux-writing-standards/)
- [Module 2 — Readability standards](../../02-ux-writing-standards/readability-standards.md)
