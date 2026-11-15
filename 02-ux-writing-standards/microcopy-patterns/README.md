# Microcopy patterns

Microcopy is the short, functional text that guides users through interactions: error messages, button labels, form fields, empty states, confirmation dialogs, and onboarding flows. It is often the content users notice least when it is working, and most when it is not.

This sub-module covers the six patterns that account for the majority of microcopy decisions in digital products.

---

## Patterns in this sub-module

| Pattern | What it covers |
|---|---|
| [Error messages](error-messages.md) | Inline validation, form-level errors, alert banners, and error pages |
| [Buttons and CTAs](buttons-and-ctas.md) | Action labels for all button types, from primary actions to destructive flows |
| [Form fields](form-fields.md) | Labels, placeholder text, helper text, and validation messages |
| [Empty states](empty-states.md) | First-use, user-cleared, and no-results states |
| [Confirmation dialogs](confirmation-dialogs.md) | Reversible and irreversible action dialogs |
| [Onboarding](onboarding.md) | Welcome screens, product tours, tooltips, and progress flows |

---

## How to use these patterns

Each pattern document follows a consistent structure:

1. **Overview** — what the pattern is and when it applies
2. **Rules** — must-follow standards; non-compliance represents a content error
3. **Recommendations** — strong defaults; exceptions are acceptable when justified
4. **Contextual decisions** — depends on product type, audience, or platform
5. **Accessibility** — programmatic and semantic requirements
6. **Illustrative examples** — context-independent examples with bracketed placeholders
7. **Review checklist** — a gate before content ships

For an explanation of the Rule / Recommendation / Contextual decision framework, see the [Module 2 README](../README.md).

---

## Principles that apply across all microcopy

These principles apply regardless of which pattern you are working on:

**Write for the moment.** Microcopy is read in context, under cognitive load, often mid-task. Write for the user's state at that moment — not for the user reading leisurely.

**Be specific.** Generic microcopy is the most common failure mode. "An error occurred" tells the user nothing. "Your file is too large. The maximum size is [n] MB." gives them a path forward.

**Include the next step.** Every piece of microcopy that tells a user something has gone wrong or changed should also tell them what to do next.

**Do not blame the user.** Error messages and confirmation dialogs should never imply the user made a mistake. Write around the user, not toward them.

---

## Related sub-modules

- [Content components](../content-components/README.md) — Longer-form content elements: notifications, tooltips, helper text, navigation labels
- [Readability standards](../readability-standards.md) — Grade level targets; error messages and microcopy target Grade 6–7
- [Inclusive language guide](../inclusive-language-guide.md) — Applying inclusive language standards to microcopy
