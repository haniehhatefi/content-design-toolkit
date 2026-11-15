# Microcopy generation prompts

This file contains four prompt templates for generating microcopy: error messages, button labels and CTAs, empty states, and notifications. Each template produces candidate options for human evaluation — not final, ready-to-publish copy.

Before using any template, work through the [pre-prompt constraint checklist](../ai-content-principles.md#pre-prompt-constraint-checklist) and ensure your grounding context is in place. See [grounding-guide.md](../grounding-guide.md) for how to structure reusable instructions and reference context.

---

## 1. Error messages

**Purpose:** Generate candidate error messages for inline validation, form-level errors, system alerts, or error pages. Use when creating new error messages or when existing error messages need to be evaluated for rewriting.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes (Clear, Human, Helpful), writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | Error messages pattern: anatomy, Rules, and Recommendations | [Module 2 — Error messages](../../02-ux-writing-standards/microcopy-patterns/error-messages.md) |
| Reference context | Readability target: Grade 6–7 for all error messages | [Module 2 — Readability standards](../../02-ux-writing-standards/readability-standards.md) |

Supply both grounding levels before the task-specific request. The reusable instructions go in the most persistent position your platform offers; the reference context goes at the start of the conversation or task.

---

**Template:**

    Generate [number] candidate error messages for the following situation. Present
    them as options for human evaluation, not final copy.

    ERROR TYPE: [inline validation / form-level / system alert or banner / error page]

    SITUATION: [Describe what went wrong. For example: "The user has attempted to upload
    a file that exceeds the size limit of [n] MB."]

    PRODUCT CONTEXT: [Describe the product and the component where the error appears.
    For example: "A file management product. The error appears adjacent to an upload
    field in a document submission form."]

    CONSTRAINTS:
    - [List any specific constraints, such as character limits, recovery options
      available to the user, or related content the error must be consistent with]
    - [Include the specific next step available to the user, if known]

    Apply the error message Rules and Recommendations from the supplied grounding
    context. For each option, identify the applicable Rules, Recommendations, or
    Contextual decisions from the supplied grounding. Do not invent criteria or
    assign guidance levels to decisions that are not covered by the supplied
    standards.

    OUTPUT FORMAT: Present each option as a numbered item. For each option, include:
    - The error message text
    - A brief annotation: the applicable Rule, Recommendation, or Contextual
      decision, and any trade-off in the approach (for example, specificity vs.
      brevity)

    Label all outputs as options for evaluation.

---

**Output format:** A numbered list of [number] options, each with message text and an annotation identifying the applicable guidance level and any trade-off in the approach. The annotation makes options comparable and reviewable.

**Usage notes:**

- **Verify any specific claims.** AI-generated error messages may include specific recovery steps (links, paths, timeframes) that do not exist in your product. Verify every recovery instruction against your product's actual flows before use. See [AI content principles — Factual and product-specific claims](../ai-content-principles.md#factual-and-product-specific-claims).
- **Check the three Rules.** Every generated error message must tell the user what to do next [Rule], must not blame the user [Rule], and must use plain language without technical codes [Rule]. These are non-negotiable; do not select an option that fails any of them, regardless of how well it handles the Recommendations.
- **Inline validation placement is not in scope.** This template generates message text only. The requirement to place inline errors adjacent to their field [Rule] is an implementation decision, not a writing decision — but confirm it is met in the final design.
- **High-stakes errors need extra review.** For errors involving data loss, failed payments, or security issues, review the output against the Recommendation to confirm what has been preserved, not only what went wrong. AI outputs in these scenarios tend to focus on the failure and omit the reassurance.
- **Reading level.** Check the generated output against the Grade 6–7 target [Rule for error messages]. AI tools generally produce readable error messages, but verify any option that uses conditional structures ("If [condition], then [action]") or compound clauses.

---

## 2. Button labels and CTAs

**Purpose:** Generate candidate labels for primary actions, destructive actions, secondary or cancellation buttons, loading states, and multi-step navigation buttons. Use when creating new button labels or evaluating whether existing labels are specific enough.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes (Clear, Human, Helpful), writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | Buttons and CTAs pattern: Rules, Recommendations, and type-specific guidance | [Module 2 — Buttons and CTAs](../../02-ux-writing-standards/microcopy-patterns/buttons-and-ctas.md) |

---

**Template:**

    Generate [number] candidate labels for the following button or CTA. Present them
    as options for human evaluation, not final copy.

    BUTTON TYPE: [primary / secondary / destructive / ghost or tertiary / loading state /
    multi-step navigation]

    ACTION: [Describe what the button does when selected. For example: "Submits the
    user's completed job application to the system."]

    OBJECT: [Name the specific thing being acted on, if applicable. For example:
    "job application" / "account" / "team member [name]"]

    CONTEXT: [Describe where the button appears and what the user is doing.
    For example: "The final step of a four-step application flow. The user has
    reviewed their application and is ready to submit."]

    CONSTRAINTS:
    - [Character limit, if any]
    - [Whether this is a destructive action requiring a secondary label]
    - [Whether a loading state label is also needed]
    - [Any established product vocabulary the label must be consistent with]

    Apply the button label Rules and Recommendations from the supplied grounding
    context. For each option, identify the applicable Rules, Recommendations, or
    Contextual decisions from the supplied grounding. Do not invent criteria or
    assign guidance levels to decisions that are not covered by the supplied
    standards.

    OUTPUT FORMAT: Present each option as a numbered item. For each option, include:
    - The button label (and loading state label if requested)
    - A brief annotation: the applicable Rule, Recommendation, or Contextual
      decision, and any trade-off in the approach (for example, specificity vs.
      brevity)

    If a destructive action label is requested, include the corresponding secondary
    label ("Cancel" or equivalent) for each option.

    Label all outputs as options for evaluation.

---

**Output format:** A numbered list of [number] options. For destructive actions, each option includes both the primary destructive label and the secondary label. Each option includes an annotation identifying the writing decision made.

**Usage notes:**

- **Apply the Rules before selecting.** Every button label must begin with an action verb [Rule] and must be specific — not "Submit", "OK", or "Yes" [Rule]. No end punctuation [Rule]. For destructive actions, the label must name the specific destructive action, not confirm generically [Rule]. Do not select an option that fails any of these.
- **Sentence case is a Recommendation, not a Rule.** If your product's established style guide specifies title case or all caps for button labels, that takes precedence. The toolkit default is sentence case [Recommendation]. Note which convention you are applying when evaluating options.
- **AI tends toward generic.** Even with grounding context, AI-generated button labels can default to common patterns ("Get started", "Continue", "Next") that are less specific than the product requires. Evaluate whether the generated label tells the user what specifically will happen, not just that something will.
- **Multi-step flows.** For navigation buttons in multi-step flows, verify that the label reflects the specific destination or action, not just the direction ("Review your order", not "Next"). AI may generate generic navigation labels even when the prompt specifies a step-specific context.
- **Marketing CTAs.** The Recommendation to use first-person language for marketing CTAs ("Start my free trial" rather than "Start free trial") is a contextual decision that depends on the product's established voice. The template does not assume this by default; add it as a constraint if needed.

---

## 3. Empty states

**Purpose:** Generate candidate copy for first-use empty states, user-cleared empty states, and no-results states. Use when creating empty state copy for a new view or when an existing empty state lacks a clear next step.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes (Clear, Human, Helpful), writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | Empty states pattern: three types, anatomy, Rules, and Recommendations | [Module 2 — Empty states](../../02-ux-writing-standards/microcopy-patterns/empty-states.md) |
| Reference context | Buttons and CTAs pattern: for the CTA within the empty state | [Module 2 — Buttons and CTAs](../../02-ux-writing-standards/microcopy-patterns/buttons-and-ctas.md) |

---

**Template:**

    Generate [number] candidate empty states for the following view. Present them as
    options for human evaluation, not final copy.

    EMPTY STATE TYPE: [first use / user-cleared / no results]

    VIEW: [Describe the view or component that will show the empty state. For example:
    "A project list view in a project management product."]

    PRODUCT CONTEXT: [Describe the product and the user's situation. For example:
    "A project management product for small teams. The user has just created their
    account and has not yet created any projects."]

    PRIMARY ACTION: [Name the specific primary action this product supports, using the
    product's own terminology. For example: "Create project" / "Add team member" /
    "Upload document"]

    [For no-results states only — include this block:]
    SEARCH OR FILTER CONTEXT: [Describe what was searched or filtered. For example:
    "The user searched for 'Q4 reports' and no projects match that search term."]
    RECOVERY OPTIONS: [List the ways the user can adjust their search or filter.
    For example: "Clear the search, broaden the date range, or remove a status filter."]

    CONSTRAINTS:
    - [Character or length limit, if any]
    - [Whether the view supports different user roles that need different empty states]
    - [Any product-specific terminology the copy must use]

    Apply the empty state Rules and Recommendations from the supplied grounding
    context. For each option, identify the applicable Rules, Recommendations, or
    Contextual decisions from the supplied grounding. Do not invent criteria or
    assign guidance levels to decisions that are not covered by the supplied
    standards.

    OUTPUT FORMAT: Present each option as a numbered item. For each option, include:
    - The empty state copy: explanation, invitation, and CTA label (all three
      components, even if the final design may omit one)
    - A brief annotation: the applicable Rule, Recommendation, or Contextual
      decision, and any trade-off in the approach

    Label all outputs as options for evaluation.

---

**Output format:** A numbered list of [number] options. Each option includes all three structural components (explanation, invitation, CTA label) with an annotation. Including all three components even when the design may omit one allows the content designer to evaluate each component independently.

**Usage notes:**

- **Apply the Rules before selecting.** Every empty state must include an explanation and a next step [Rule]. For first-use states, the CTA must match the product's primary action — not a generic "Get started" [Rule]. For no-results states, the message must not imply the fault is the user's [Rule].
- **Supply the primary action vocabulary.** AI tools will generate plausible-sounding CTAs that may not match your product's established action terminology. Supply the exact primary action label in the prompt, and verify that the generated options use it.
- **Role differences.** If the view is used by both users who can add content and users who cannot, generate separate empty states for each role. A single prompt will not produce both unless the role constraint is included explicitly.
- **No-results states need the search term.** The Recommendation to include the search term in the message requires knowing what was searched. Supply this in the SEARCH OR FILTER CONTEXT field. Without it, the AI will generate a generic template with a placeholder that you will need to fill.
- **Avoid AI apology defaults.** AI tools often generate empty states that begin with "Sorry" or "Unfortunately". The Recommendation is to avoid apologising for states that are a normal part of the product lifecycle. Flag this in your evaluation and revise.

---

## 4. Notifications

**Purpose:** Generate candidate copy for toast confirmations, warning banners, error notifications, and timed alerts. Use when creating new notification text or when existing notifications lack specificity or a clear action.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes (Clear, Human, Helpful), writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | Notifications pattern: types, Rules, and Recommendations | [Module 2 — Notifications](../../02-ux-writing-standards/content-components/notifications.md) |

---

**Template:**

    Generate [number] candidate notification messages for the following situation.
    Present them as options for human evaluation, not final copy.

    NOTIFICATION TYPE: [toast or snackbar / banner (inline) / alert (modal-adjacent) /
    notification centre / badge]

    EVENT OR STATE: [Describe what happened, or what the user needs to know. For example:
    "A background export of [n] records has completed successfully." / "The user's
    account plan expires in [n] days."]

    ACTION REQUIRED: [yes / no — if yes, describe the available action and where it
    leads]

    PRODUCT CONTEXT: [Describe the product and the component or view where the
    notification appears. For example: "A data management product. The notification
    appears in the notification centre after a background process completes."]

    CONSTRAINTS:
    - [Character limit, if any]
    - [Whether the notification is timed — if so, include the specific time or
      timeframe to include in the message]
    - [Whether the notification should include a link — if so, describe where it leads]
    - [Any product-specific terminology the copy must use]

    Apply the notification Rules and Recommendations from the supplied grounding
    context. For each option, identify the applicable Rules, Recommendations, or
    Contextual decisions from the supplied grounding. Do not invent criteria or
    assign guidance levels to decisions that are not covered by the supplied
    standards.

    OUTPUT FORMAT: Present each option as a numbered item. For each option, include:
    - The notification text (including link text if a link is requested)
    - A brief annotation: the applicable Rule, Recommendation, or Contextual
      decision, and any trade-off in the approach (for example, brevity vs.
      specificity in toasts)

    Label all outputs as options for evaluation.

---

**Output format:** A numbered list of [number] options. Each option includes the notification text (and link text, if requested) and an annotation identifying the applicable guidance level and any trade-off in the approach. When badge is selected as the notification type, each option includes the badge content (numeric count, text label, or accessible label as specified in CONSTRAINTS) rather than notification text.

**Usage notes:**

- **Match notification type to urgency and persistence.** Verify that the notification type specified in the template is appropriate for the urgency and persistence of the information [Rule]. A low-urgency confirmation and a critical warning should not use the same notification format.
- **Apply the remaining Rules before selecting.** Every notification must state what happened and, where action is required, what to do [Rule]. It must use specific language — naming the item, action, or state — not generic language [Rule]. Critical information or required actions must not be placed in auto-dismissing toasts [Rule]. Do not select an option that fails any of these.
- **Verify specific claims.** AI-generated notifications may include specific timeframes, item names, or recovery links that do not match your product's behaviour. Treat any notification that references specific product states (plan names, feature names, timeframes, paths) as a placeholder pending verification.
- **Timed notifications require the actual time.** The Recommendation to include the specific time remaining ("expires in 5 minutes", not "is about to expire") requires that you supply this in the CONSTRAINTS field. Supply the actual value, not a placeholder, to avoid generating a template that will need re-prompting.
- **Success toasts tend to be over-written.** The Recommendation for success toasts is one sentence confirming what was completed. AI tools often generate longer confirmations with unnecessary explanation. Evaluate brevity alongside specificity.
- **Warning banners need reason and consequence.** The Recommendation for warning banners includes the reason and the consequence, not only the warning. AI tools may generate banners that name the event without explaining the impact ("Your trial ends soon" rather than "Your trial ends on [date]. [Renew to keep access]"). Evaluate whether the generated options include both.
- **Badge type.** If you select badge as the notification type, specify in the CONSTRAINTS field whether you need a numeric count format, a text label, or an accessible label for screen reader announcement. Without this, the AI will generate a generic count format, which may not match what the design requires.
- **Narrator voice.** The contextual decision on first vs. third person ("We couldn't sync" vs. "Your data couldn't sync") requires consistency with your product's established voice. The template does not assume either; evaluate the options against your existing notifications before selecting.

---

## Related documents

- [Prompt templates — README](README.md) — Template anatomy, grounding requirements, and default constraints
- [Grounding guide](../grounding-guide.md) — How to structure reusable instructions and reference context before using these templates
- [AI content principles](../ai-content-principles.md) — Pre-prompt checklist and responsible-use requirements
- [Output evaluation rubric](../output-evaluation-rubric.md) — How to evaluate the options these templates produce
- [Failure modes](../failure-modes.md) — What to watch for in microcopy outputs specifically
- [Module 2 — Error messages](../../02-ux-writing-standards/microcopy-patterns/error-messages.md)
- [Module 2 — Buttons and CTAs](../../02-ux-writing-standards/microcopy-patterns/buttons-and-ctas.md)
- [Module 2 — Empty states](../../02-ux-writing-standards/microcopy-patterns/empty-states.md)
- [Module 2 — Notifications](../../02-ux-writing-standards/content-components/notifications.md)
