# Prompt templates — how to use this library

This folder contains prompt templates for three content design task types: generating microcopy, reviewing content against the toolkit's standards, and rewriting content for plain language and voice alignment.

The templates are starting points, not complete ready-to-send prompts. Each one requires grounding context from [grounding-guide.md](../grounding-guide.md) and task-specific information from you. Without relevant grounding, the AI may not apply the toolkit's standards consistently, even when using a well-structured template.

---

## Template anatomy

Every template in this library shares the same five-component structure.

| Component | What it is | What you do |
|---|---|---|
| **Purpose** | A one-line description of what the template produces and when to use it | Read before selecting a template |
| **Grounding requirements** | Which Module 1 and Module 2 standards to supply as context, and at what level (reusable or reference context) | Supply these before the task-specific request, using the position your platform supports |
| **Template** | The prompt text, with bracketed placeholders for task-specific content | Replace every bracketed item before sending |
| **Output format** | What to ask the AI to produce — options, evaluation, revised text, or similar | Included in the template; adapt if your workflow needs a different format |
| **Usage notes** | What to check in the output for this content type; known limitations | Read after receiving the output, before treating it as usable |

---

## How grounding and templates work together

The templates in this library are task-specific requests. They are designed to be used together with grounding context from [grounding-guide.md](../grounding-guide.md), not instead of it.

The grounding context supplies the persistent standards: voice attributes, guidance level framework, and cross-cutting writing requirements. The template supplies the task-specific request: what to generate, review, or rewrite, and under what constraints.

Both are required. The grounding context establishes the standard; the template applies it to a specific task.

**Where each piece goes** depends on your platform. See [grounding-guide.md — Platform differences](../grounding-guide.md#platform-differences). In all cases, grounding context should be in place before the task-specific request.

**If your platform provides no persistent grounding position,** include the most relevant section from the reusable instructions template at the top of your prompt, before the task-specific content.

---

## How to adapt a template

Templates use bracketed placeholders for content that varies by task. Replace every placeholder before sending. A prompt sent with unreplaced brackets will produce generic or confused output.

**Common placeholder types:**

| Placeholder | Example | What to supply |
|---|---|---|
| `[content type]` | Error message, notification banner | The specific type of content you are creating or reviewing |
| `[product context]` | "A file upload component in a data management product" | Enough context for the AI to understand what the product does and who uses it |
| `[specific constraint]` | "The file size limit is 10 MB" | Facts, rules, or conditions the output must respect |
| `[output format]` | "Three options presented as a table" | How you want the output structured for review |

**What to keep when adapting:** The grounding references, guidance level labels, and output format instructions. These are what connect the output to the toolkit's standards and make it reviewable.

**What to change:** The content brief, specific constraints, number of options requested, and product-specific context.

**Before sending:** Work through the [pre-prompt constraint checklist](../ai-content-principles.md#pre-prompt-constraint-checklist). This takes under two minutes and covers privacy, accuracy requirements, and review responsibilities.

---

## Default constraints

These four constraints are present in every template in this library. They apply regardless of task type and should not be removed when adapting a template.

| Constraint | Why it is included by default |
|---|---|
| Apply the voice attributes (Clear, Human, Helpful) | Without voice grounding, outputs default to a generic professional register that may not match the product's voice |
| Apply the guidance level framework (Rule, Recommendation, Contextual) | Without guidance levels, the AI cannot distinguish between non-negotiable requirements and stylistic defaults |
| Specify the output format | Structured outputs — a table of options, an evaluation list — are easier to review systematically than unstructured prose |
| Label outputs as options to evaluate, not final copy | This sets the right expectation for human review and prevents outputs from being used directly without evaluation |

One constraint applies to all tasks but is supplied through the pre-prompt checklist rather than the template itself: **verify factual and product-specific claims against authoritative sources, prioritising primary sources where available.** No amount of well-structured grounding removes this requirement.

---

## The three template files

| File | Task type | Use when |
|---|---|---|
| [microcopy-prompts.md](microcopy-prompts.md) | **Generation** | Creating new error messages, button labels, empty states, or notifications |
| [review-prompts.md](review-prompts.md) | **Review** | Evaluating existing content against voice, accessibility, and guidance level standards |
| [rewriting-prompts.md](rewriting-prompts.md) | **Rewriting** | Improving existing content for plain language, readability, or voice alignment |

These three task types correspond to stage 3 of the five-stage workflow described in the [Module 3 README](../README.md). The [worked examples](../worked-examples.md) show each task type end to end, from grounded prompt to human-reviewed final version.

---

## Related documents

- [Grounding guide](../grounding-guide.md) — How to structure context before using any template
- [AI content principles](../ai-content-principles.md) — Responsible-use requirements and the pre-prompt checklist
- [Output evaluation rubric](../output-evaluation-rubric.md) — How to evaluate the output once you have it
- [Failure modes](../failure-modes.md) — What to watch for in outputs from each task type
