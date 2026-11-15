# Content review prompts

This file contains three prompt templates for reviewing existing content against the toolkit's standards: a voice alignment review, a pattern compliance review, and a comparative review. Each template produces a structured evaluation for human decision-making — not a verdict, and not a replacement for the content designer's judgment.

Before using any template, work through the [pre-prompt constraint checklist](../ai-content-principles.md#pre-prompt-constraint-checklist) and ensure your grounding context is in place. See [grounding-guide.md](../grounding-guide.md) for how to structure reusable instructions and reference context.

**What review prompts do not replace.** AI-assisted review identifies potential issues and flags them against the supplied grounding. It does not understand your product, your users, or the full context in which the content will be read. The content designer makes the final determination on what requires a change, what warrants a note, and what is correct as written.

---

## 1. Voice alignment review

**Purpose:** Evaluate existing content against the three voice attributes (Clear, Human, Helpful) and two writing standards (Direct, Consistent). Use when you need to assess whether copy reflects the product's established voice, or when onboarding a new contributor whose drafts need to be evaluated against the voice framework.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes (Clear, Human, Helpful), writing standards (Direct, Consistent), and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | The specific voice and tone guidance for the product, if established; tone variations by context | [Module 1 — Voice principles](../../01-foundations/voice-principles.md) |

The voice attributes are cross-cutting standards that apply to all content types. This template does not require Module 2 reference context unless a content-type-specific Rule is relevant to the review.

---

**Template:**

    Review the following content against the voice attributes and writing standards
    supplied in the grounding context. The purpose of this review is to identify
    where the content diverges from the established voice — not to rewrite it.

    CONTENT TO REVIEW:
    [Paste the content here. If reviewing multiple items (for example, a set of
    button labels or a series of error messages), include all items. Label each
    item if they are distinct (for example: "Button label:", "Error message:")]

    CONTENT TYPE: [Describe what this content is and where it appears. For example:
    "Error messages from a file upload component" / "Onboarding copy for a new user
    registration flow"]

    PRODUCT CONTEXT: [Describe the product and audience briefly, so the review can
    assess fit. For example: "A project management product for small creative teams.
    The voice is Clear, Human, and Helpful — conversational but not casual."]

    For each issue found, identify:
    1. The specific voice attribute or writing standard it concerns (Clear, Human,
       Helpful, Direct, or Consistent)
    2. The exact text that triggers the issue
    3. What specifically about that text diverges from the standard
    4. The guidance level: Rule, Recommendation, or Contextual decision, as specified
       in the supplied grounding

    For each finding, identify the applicable Rules, Recommendations, or Contextual
    decisions from the supplied grounding. Do not invent criteria or assign guidance
    levels to decisions that are not covered by the supplied standards.

    If no issues are found for a voice attribute, state that explicitly.

    OUTPUT FORMAT:
    - Organise findings by voice attribute (Clear, Human, Helpful, Direct,
      Consistent)
    - Under each attribute: list issues found, or "No issues identified"
    - For each issue: quote the specific text, name the criterion and guidance level,
      and describe what diverges
    - Close with a summary: total issues by guidance level (Rules / Recommendations /
      Contextual decisions)

    Label the output as a structured evaluation for human review.

---

**Output format:** A structured evaluation organised by voice attribute. Each section identifies issues (or confirms none), quoting the specific text and naming the criterion and guidance level. The closing summary allows the content designer to quickly assess the overall severity of findings.

**Usage notes:**

- **This review evaluates voice, not correctness.** The voice alignment review identifies divergence from the established voice attributes and writing standards. It does not evaluate factual accuracy, accessibility compliance, or content-type-specific Rules (such as error message anatomy). For those, use the pattern compliance review.
- **Rules vs. Recommendations in voice review.** Most voice guidance operates at Recommendation or Contextual level — the Clear, Human, and Helpful attributes describe a direction, not a binary pass/fail. The clearest Rule relevant to voice review is the readability target (Grade 6–7 for error messages and high-stress microcopy [Rule]). The recommendation to use "select" rather than "click" or "tap" for primary interactive actions is a Recommendation [Recommendation]. The broader requirement to avoid copy that assumes physical or cognitive ability is a Rule in the inclusive language guide and should be assessed through the pattern compliance review. An AI review may over-classify voice observations as Rules — verify guidance levels in the [grounding-guide.md reusable instructions](../grounding-guide.md#reusable-instructions-template) before acting on a finding.
- **Consistency check limitations.** The Consistent standard requires the same term for the same thing across the product. An AI tool reviewing a single excerpt cannot check consistency across the full product — it can only flag inconsistency within the supplied content. For cross-product consistency checks, the review must supply a broader sample or a terminology list.
- **AI may flag style preferences as issues.** AI tools trained on general content can flag plain, correct writing as "unclear" or "informal" because it departs from generic professional language. Apply the product's own voice attributes as the benchmark, not the tool's default register.

---

## 2. Pattern compliance review

**Purpose:** Evaluate existing content against a specific Module 2 pattern — checking Rules (required), Recommendations (strong defaults), and accessibility requirements for the content type. Use when auditing content against the toolkit's documented standards for a specific component, or when preparing a detailed content brief that identifies what must change before publication.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes, writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | The Module 2 pattern for the content type being reviewed: its Rules, Recommendations, anatomy, and accessibility requirements | The relevant file in [Module 2 — UX writing standards](../../02-ux-writing-standards/) |
| Reference context | Readability target for this content type | [Module 2 — Readability standards](../../02-ux-writing-standards/readability-standards.md) |

Supply the full Rules and Recommendations from the Module 2 pattern as reference context — not a summary. The review can only check what is in the grounding.

---

**Template:**

    Review the following content against the [content type] pattern from the
    supplied grounding context. Identify issues with specific reference to the
    Rules, Recommendations, and accessibility requirements supplied.

    CONTENT TO REVIEW:
    [Paste the content here. For sets of items (for example, all error messages
    for a form), include all items. Label each item clearly.]

    CONTENT TYPE: [Name the specific content type and Module 2 pattern being
    applied. For example: "Error messages — Module 2 error messages pattern" /
    "Button labels — Module 2 buttons and CTAs pattern"]

    PRODUCT CONTEXT: [Describe what the product does and who uses it. Include
    any constraints relevant to the review — character limits, platform, user
    reading level if known.]

    REVIEW SCOPE: [Specify what this review covers. For example: "Review for
    Rules compliance only" / "Full review: Rules, Recommendations, and
    accessibility" / "Accessibility requirements only"]

    For each issue found, identify:
    1. The criterion from the supplied grounding (quote or name it)
    2. The guidance level: Rule (required change), Recommendation (strong default,
       exceptions possible with reason), or Contextual (situation-dependent)
    3. The specific text in the content that triggers the issue
    4. What specifically the content does that the criterion does not permit or
       recommends against

    For each issue, identify the applicable Rules, Recommendations, or Contextual
    decisions from the supplied grounding. Do not invent criteria or assign guidance
    levels to decisions that are not covered by the supplied standards.

    Organise findings so that Rule violations (required changes) are listed
    separately from Recommendation observations (for the content designer to
    consider). List accessibility issues separately.

    If a finding concerns a Contextual decision, include it under Recommendation
    observations, clearly label it as Contextual, and explain which situational
    factors affect the decision. Do not reclassify it as a Recommendation.

    If no issues are found in a category, state that explicitly.

    OUTPUT FORMAT:
    Section 1 — Rule violations: issues that require a change
    Section 2 — Recommendation observations: issues for the content designer
    to consider
    Section 3 — Accessibility issues: issues with the accessibility
    requirements in the supplied pattern
    Section 4 — Summary: total findings by section; overall status flags: select
    the applicable Rule status (No Rule violations identified / Rule revisions
    required) and independently indicate whether Manual accessibility verification
    is required.

    Do not present "No Rule violations identified" as confirmation that the content
    is fully accessible — text-level review cannot verify ARIA implementation,
    contrast ratios, or focus management.

    Label the output as a structured evaluation for human review.

---

**Output format:** A four-part evaluation: Rule violations, Recommendation observations, accessibility issues, and a summary. The first three sections separate required changes, discretionary improvements, and accessibility concerns; the summary gives the content designer an overall picture.

**Usage notes:**

- **Supply the full pattern, not a summary.** A pattern compliance review can only check the criteria in the grounding. If the reference context omits a Rule — for example, if you paraphrase the error messages pattern rather than including its Rules verbatim — the AI may miss Rule violations or misclassify their guidance level.
- **Accessibility findings require verification.** The accessibility requirements in Module 2 patterns reference ARIA attributes, contrast ratios, and focus behaviour. AI tools can identify whether text-level requirements are met (device-neutral language, reading level) but cannot verify ARIA implementation, contrast ratios, or focus management from text content alone. Flag accessibility findings for manual verification.
- **Watch for invented WCAG criteria.** AI tools with general knowledge of accessibility may apply WCAG success criteria not in the supplied grounding. Any accessibility finding that cannot be traced to the Module 2 pattern's accessibility section is outside the scope of this toolkit-grounded review. Do not present it as a toolkit violation. If the criterion may be relevant, verify it separately against the applicable accessibility standard before acting on it.
- **Rules compliance as a minimum bar.** The pattern compliance review treats Rule violations as the minimum bar for publication. Content that passes all Rules but fails several Recommendations is still eligible for publication — the Recommendation observations are for the content designer's judgment, not a blocklist.
- **Character limits and platform constraints.** If the content type has a character limit, include it in PRODUCT CONTEXT. The AI cannot verify that generated or reviewed text fits a specific UI without this constraint. Without it, Recommendation observations about length may be inaccurate.

---

## 3. Comparative review

**Purpose:** Evaluate two or three versions of the same content against the toolkit's standards and identify which best meets the requirements. Use when multiple versions of a piece of content exist — from stakeholder drafts, previous iterations, or generation outputs — and a structured comparison is needed to inform the final decision.

**Grounding requirements:**

| Level | What to supply | Source |
|---|---|---|
| Reusable instructions | Voice attributes, writing standards, and guidance level framework | [grounding-guide.md — Reusable instructions template](../grounding-guide.md#reusable-instructions-template) |
| Reference context | The Module 2 pattern for the content type being compared, including its Rules, Recommendations, and any readability target | The relevant file in [Module 2 — UX writing standards](../../02-ux-writing-standards/) |

---

**Template:**

    Compare the following [number] versions of [content type] against the voice
    attributes and [content type] pattern supplied in the grounding context.

    VERSION A:
    [Paste Version A here]

    VERSION B:
    [Paste Version B here]

    [VERSION C: (optional)
    [Paste Version C here, if applicable]]

    CONTENT TYPE: [Name the content type and the Module 2 pattern being applied.
    For example: "Error messages — Module 2 error messages pattern"]

    PRODUCT CONTEXT: [Describe the product, the specific scenario, and any
    constraints. For example: "A data management product. This is a system error
    message for a failed background export. The user cannot take immediate action;
    the error should acknowledge the failure and provide a next step."]

    For each version, evaluate:
    1. Rule compliance: does it meet all Rules for this content type? List any
       violations.
    2. Recommendation alignment: how well does it reflect the Recommendations?
       Note any gaps.
    3. Voice and writing standards: how well does it reflect the voice attributes
       (Clear, Human, Helpful) and writing standards (Direct, Consistent)?
    4. Relative strengths: what does this version do better than the others?

    For each finding, identify the applicable Rules, Recommendations, or Contextual
    decisions from the supplied grounding. Do not invent criteria or assign guidance
    levels to decisions that are not covered by the supplied standards.

    OUTPUT FORMAT:
    - For each version: a structured assessment covering the four evaluation areas
    - A comparison summary: which version best meets the Rules, and which best
      reflects the Recommendations and voice. If no version clearly performs best
      in a category, state that rather than forcing a ranking
    - A recommended starting point for revision, with the specific changes needed
      to bring it into full compliance

    Label the output as a structured evaluation for human decision-making. The
    final choice remains with the content designer.

---

**Output format:** A structured assessment for each version, followed by a comparison summary and a recommended starting point for revision. The comparison identifies which version meets the Rules and which best reflects the voice — these may not be the same version, and the summary makes that visible.

**Usage notes:**

- **The recommended starting point is a starting point, not a verdict.** The comparative review is designed to give the content designer a structured basis for a decision, not to make the decision. The AI tool does not know the full context — the product's history, the audience's characteristics, or the constraints that produced each version. Use the comparison to structure your own evaluation, not to replace it.
- **Versions that fail Rules are not automatically excluded.** A version that violates a Rule may still be the better starting point for revision if it handles the voice or the structure better than a Rule-compliant but less effective version. The comparison identifies what needs to change, not which version to discard.
- **Parity in input.** For a meaningful comparison, all versions should be at the same stage — all first drafts, or all reviewed drafts. Comparing a first draft against a carefully revised version does not produce a useful signal.
- **Comparative reviews work best with 2–3 versions.** More than three versions produce output that is harder to act on. If you have more than three, narrow to the best candidates before using this template.
- **AI may anchor on Version A.** AI tools can apply more critical scrutiny to later versions when Version A is presented first. If you notice the comparison is uneven, re-run with the versions in a different order.

---

## Related documents

- [Prompt templates — README](README.md) — Template anatomy, grounding requirements, and default constraints
- [Grounding guide](../grounding-guide.md) — How to structure reusable instructions and reference context before using these templates
- [AI content principles](../ai-content-principles.md) — Pre-prompt checklist and responsible-use requirements
- [Output evaluation rubric](../output-evaluation-rubric.md) — How to evaluate the output these templates produce
- [Failure modes](../failure-modes.md) — What to watch for in AI review outputs specifically
- [Module 1 — Voice principles](../../01-foundations/voice-principles.md)
- [Module 2 — UX writing standards](../../02-ux-writing-standards/)
- [Module 2 — Readability standards](../../02-ux-writing-standards/readability-standards.md)
