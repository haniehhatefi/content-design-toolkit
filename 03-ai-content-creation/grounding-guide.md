# Grounding guide

Grounding is the practice of supplying an AI tool with the context it needs to perform a task according to your standards, before the task begins. For content design work, that means giving the tool the voice principles, writing standards, and guidance level framework from this toolkit — structured in a way that shapes how it generates, evaluates, or rewrites content.

Without grounding, an AI tool uses its training data to decide what "good content" looks like. With grounding, it uses your standards.

---

## Three types of context

Not all context belongs in the same place or at the same level of persistence. Structuring context by type produces grounding that is reusable, targeted, and within the token limits most AI tools impose.

### Reusable instructions

Reusable instructions are the standing guidance that applies to every content task you do with this toolkit. They define the standard the AI should apply, independent of any specific piece of content or content type.

For content design work, reusable instructions typically include:
- The voice attributes the content should demonstrate (Clear, Human, Helpful)
- The cross-cutting writing standards (Direct, Consistent)
- The guidance level framework (Rule, Recommendation, Contextual) and how to apply it
- Accessibility requirements that apply across all content types (device-neutral language, reading level targets)

**How to supply them:** Reusable instructions belong in the most persistent position your AI platform offers — a system prompt, custom instructions field, project knowledge, or persona field, depending on the tool. They are set once and applied to every interaction in that workspace or project.

### Reference context

Reference context is specific to the task type you are working on. It tells the AI which standards apply to this kind of content — not all content in general.

For content design work, reference context typically includes:
- The Module 2 pattern relevant to the task (for example, the error messages pattern when generating error messages)
- The readability target for this content type
- Content-type-specific Rules and Recommendations from Module 2 (for example, error messages must give the user a next step [Rule], and should be specific about what went wrong where possible [Recommendation])

**How to supply them:** Reference context is usually supplied once at the start of a task conversation, before the task-specific request. It is not reused across unrelated task types.

### Task-specific requests

The task-specific request is the prompt for the specific piece of content you need. It includes the content brief, the constraints for this task, and the output format you want.

**How to supply them:** Task-specific requests are the user turn — written fresh for each task. The prompt template files in this module provide starting points.

---

## Platform differences

The term "system prompt" originates from AI APIs, where you supply a `system` role message that persists above the conversation. Not every platform surfaces this in the same way. The concept of persistent grounding context is consistent across platforms; the mechanism for supplying it varies.

| Platform type | How grounding context is typically supplied | Notes |
|---|---|---|
| **AI API** (Claude API, OpenAI API, Gemini API) | A `system` parameter or role, with `user` messages for each turn | Full control over what goes where; reusable instructions belong in the system role |
| **Consumer chat with persistent instructions** (Claude.ai Projects, ChatGPT Custom Instructions) | A persistent instructions or project knowledge field, separate from the conversation | The field name varies; the principle is the same — set once, applies to all interactions in that workspace |
| **Enterprise AI tools** (Microsoft Copilot, Gemini for Workspace, similar) | "Instructions", "persona", or "prompt" fields in settings or templates | Often less flexible; available fields vary by tool and organisation configuration |
| **LLM-integrated product features** (AI writing features in design or productivity tools) | Varies; often no direct grounding access | Grounding may be limited to what you include in the task request itself |

**The principle is platform-agnostic; the mechanism is not.** The templates in this guide are written as reusable instructions and task requests, without assuming a specific prompt hierarchy. Where grounding access is available, use it; where it is not, include the most relevant reference context in the task request itself.

---

## How much context is too much

More context is not always better. Practical limits apply to all platforms:

- Most AI tools have context window limits; very long grounding prompts consume tokens that could otherwise carry task-relevant content
- Overly long grounding prompts may cause some tools to weight earlier instructions less consistently
- Including all of Modules 1 and 2 as grounding is counterproductive — the tool needs focused guidance, not a full reference library

A useful rule of thumb: **reusable instructions should cover principles; reference context should cover the specific pattern.** For a task generating an error message, the reusable instructions supply the voice attributes and guidance level framework; the reference context supplies the error messages pattern from Module 2. The two together are sufficient grounding for that task.

---

## Reusable instructions template

The following template is a starting point for grounding an AI tool with this toolkit's standards. It draws directly on the voice attributes and guidance level framework from Modules 1 and 2. Adapt it to match what your platform supports and what your task requires.

Supply this in the most persistent grounding position your platform offers, before any task-specific requests.

---

    You are assisting a content designer working on digital product copy. Apply the
    following standards when generating, reviewing, or rewriting content.

    VOICE

    The product's voice has three core attributes:

    Clear: Use plain language. Prefer short sentences and common words. Avoid
    jargon, nominalisations, and passive constructions. Write for the user's reading
    level, not the organisation's.

    Human: Sound like a person, not a system. Use active voice. Write in second
    person ("you", not "the user"). Acknowledge context and emotion where
    appropriate — do not write as if the user has no reaction to what is happening.

    Helpful: Tell the user what to do next. Focus on what is possible, not only
    what has gone wrong. Give the user the specific information they need to
    continue their task.

    Additionally, all content should be:

    Direct: Get to the point. Put the most important information first. Remove
    preamble such as "Please note that" or "In order to".

    Consistent: Use the same term for the same thing every time. Do not vary
    terminology for stylistic variety.

    GUIDANCE LEVEL FRAMEWORK

    This toolkit applies a three-level framework to content standards:

    Rule — A requirement without exceptions. Do not vary it.
    Recommendation — A strong default. Exceptions are possible with a clear reason.
    Contextual — A decision that depends on the specific situation.

    When you evaluate content against this toolkit, identify the guidance level of
    each criterion you apply. Do not treat Recommendations as Rules, or Contextual
    decisions as Recommendations.

    WRITING STANDARDS (apply to all content types)

    Use sentence case as the default for labels, headings, and button text, unless
    an established style guide specifies otherwise. [Recommendation]

    Use device-neutral language for interactive instructions — "select" rather than
    "click"; "choose" rather than "tap" — in copy that applies to all users. When
    documenting a specific interaction method, name it explicitly. [Recommendation]

    Set a reading-level target appropriate to the audience and content type. [Contextual]

    Error messages and microcopy in high-stress moments must target Grade 6–7. [Rule]

    Every error message must tell the user what to do next. [Rule]

    Be specific about what went wrong where the available information makes this
    possible. [Recommendation]

    Never blame the user, and use plain language rather than technical codes or
    system terminology. [Rule]

    Labels must remain visible during and after input. Do not use placeholder text
    as a substitute for a label. [Rule]

    EVALUATION APPROACH

    When reviewing or evaluating content against this toolkit:

    1. Apply each criterion at its guidance level (Rule, Recommendation, or
       Contextual).
    2. For each issue found, name the criterion, the guidance level, and what
       specifically in the content triggers it.
    3. Distinguish between issues that require a change (Rules) and observations
       for the content designer to consider (Recommendations, Contextual decisions).
    4. Do not invent criteria. If a standard is not in the supplied grounding
       material, do not apply it.

---

## Structuring reference context

When you add task-specific reference context before a prompt, include the following:

- The content type and the Module 2 pattern it corresponds to
- Any Rules from that pattern that must be applied without exception
- The readability target for that content type (from [readability standards](../02-ux-writing-standards/readability-standards.md))
- The specific field or component the content is for, if relevant

**Example structure for reference context (illustrative):**

    Task type: Error message for a file upload component.

    Reference: Module 2 — Error messages pattern.

    Rules for this content type:
    - Tell the user what to do next.
    - Do not blame the user.
    - Use plain language; avoid technical codes and system terminology.

    Recommendations for this content type:
    - Be specific about what went wrong where possible.
    - Provide a path forward, such as a link to the relevant place.

    Reading level target: Grade 6–7.

    Context: The user has attempted to upload a file that exceeds the size limit.
    The limit is [file size limit]. The user can reduce the file size or choose a
    different file.

---

## Illustrative example: well-structured vs. poorly-structured grounding

*(These examples demonstrate the contrast in approach. Neither is a real model output.)*

### Poorly structured grounding

> "You are a helpful content writer for a tech company. Write friendly, professional copy. Keep it short and avoid jargon."

This grounding:
- Does not define what "friendly" or "professional" means in this context
- Provides no criteria that can be used to evaluate whether the output meets requirements
- Cannot be linked back to any documented standard
- Will produce content that varies depending on the tool's interpretation of "friendly professional"

### Well-structured grounding

> "Apply the voice and writing standards below when generating error messages. Voice: Clear (plain language), Human (second person, active voice), Helpful (tell the user what to do next). Rule: Every error message must tell the user what to do next. Rule: Never blame the user. Rule: Use plain language and avoid technical codes or system terminology. Recommendation: Be specific about what went wrong where the available information makes this possible."

This grounding:
- Defines voice attributes in operational terms the tool can apply
- Separates Rules (non-negotiable) from Recommendations (strong defaults)
- Gives criteria that can be used to check the output during human review
- Is traceable to documented standards from Modules 1 and 2

---

## Related documents

- [AI content principles](ai-content-principles.md) — Responsible-use boundaries to review before grounding any task
- [Prompt templates: README](prompt-templates/README.md) — How the prompt library uses grounding context
- [Module 1 — Voice principles](../01-foundations/voice-principles.md) — Source of the voice attributes used in the template above
- [Module 1 — Content principles](../01-foundations/content-principles.md) — Source of the writing standards used in the template above
- [Module 2 README](../02-ux-writing-standards/README.md) — Guidance level framework definition
- [Readability standards](../02-ux-writing-standards/readability-standards.md) — Reading level targets by content type
