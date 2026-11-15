# Form fields

Forms are where users do their most concentrated work in a product. Every piece of text in a form — the label, the placeholder, the helper text, the validation message — either reduces that effort or adds to it. Getting form copy right is not a small detail; it is the difference between a form that gets completed and one that gets abandoned.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## The four text types in a form field

Each type serves a distinct purpose. They are not interchangeable.

| Text type | Where it appears | Purpose | Persistence |
|---|---|---|---|
| **Label** | Above or beside the input | Names the field. Always visible. | Always visible |
| **Placeholder text** | Inside the empty input field | Provides a format example or hint | Disappears when the user starts typing |
| **Helper text** | Below the input | Provides context, constraints, or format guidance | Always visible (or shown on focus) |
| **Validation message** | Below the input, alongside helper text | Reports success or error after the user has interacted | Appears after interaction |

---

## Labels

### Rules

**`Rule`** Every input field must have a visible label. Do not use placeholder text as the only label — it disappears as soon as the user starts typing, leaving them without context.

**`Rule`** Labels must be accessible and persistent. Every input must have a programmatic label — a `<label>` element associated via `for`/`id`, or an `aria-label` / `aria-labelledby` attribute — that remains available regardless of the field's interaction state.

**`Rec`** Avoid animated labels that disappear or become unreadable when a field is focused or filled. A floating label that moves upward but stays clearly visible and readable is acceptable. A label that is only present inside an empty field leaves users without context once they start typing.

**`Rec`** Labels use sentence case with no colon and no full stop. If a product's established style guide specifies a different capitalisation convention, follow that convention consistently.

> ❌ "Email Address:" → ✅ "Email address"
> ❌ "Date of birth." → ✅ "Date of birth"

### Recommendations

**`Rec`** Use noun phrases for labels, not questions. "Email address" is preferred to "What is your email address?" — the question form is wordier and more unusual in professional contexts.

**`Rec`** Mark optional fields explicitly rather than required ones, unless most fields are optional. If 8 out of 10 fields are required, mark only the 2 optional ones. If 8 out of 10 are optional, mark only the 2 required ones.

**`Rec`** Use the reader's vocabulary, not the system's. Test label terms with real users when possible.

---

## Placeholder text

### Rules

**`Rule`** Do not use placeholder text as a substitute for a label or helper text. It is not a primary communication channel — it disappears, it has low contrast in many implementations, and it is inaccessible to some screen reader configurations.

**`Rule`** If used, placeholder text should show a realistic example of the expected input format, not repeat the label.

> ❌ Label: "Email address" / Placeholder: "Email address"
> ✅ Label: "Email address" / Placeholder: "name@example.com"

### Recommendations

**`Rec`** Use placeholder text sparingly, only where a format example genuinely aids completion and cannot be communicated via helper text.

**`Rec`** Placeholder text should use a realistic but non-personal example. Avoid names and personal data.

> ❌ "John Smith" as a name example
> ✅ "Sam Taylor" (more neutral) or simply "Full name" (descriptive)

---

## Helper text

### Rules

**`Rule`** Helper text that describes a constraint (character limit, required format, specific rule) must be visible before the user submits, not only after a validation error.

> Example: "Password must be at least 8 characters and include one number" appears below the password field from the start, not only after a failed attempt.

### Recommendations

**`Rec`** Structure helper text with the template: *What to enter / Format / Why (if non-obvious).*

| Template component | Example |
|---|---|
| What to enter | "Enter the email address you used when you registered." |
| Format | "Use DD/MM/YYYY." |
| Why (optional) | "This is used to send your receipt." |

**`Rec`** Keep helper text to one or two short sentences. If a field requires more explanation than that, consider whether the form design itself needs rethinking.

**`Rec`** For fields with character limits, show a live character count and indicate the limit clearly — do not reveal the limit only after the user has exceeded it.

### Contextual decisions

**`C`** Whether to show helper text persistently or only on focus depends on the complexity of the field and the density of the form. For simple fields in a dense form, showing helper text on focus reduces visual noise. For fields with important constraints, persistent helper text is safer.

**`C`** For multi-step forms, helper text from a previous step does not need to persist to the next step — but decisions made in a previous step (such as a chosen plan or configuration) that affect what a later step requires should be visible.

---

## Validation messages

Validation messages are covered in depth in [Error messages](error-messages.md). Key principles for forms:

### Rules

**`Rule`** Show inline validation messages adjacent to the specific field they refer to, not only at the top of the form.

**`Rule`** Display validation messages inline, adjacent to the field they refer to. Where helper text is already visible, show the validation message alongside it rather than replacing it — the user may need both. Do not hide the error behind a tooltip or place it far from the field.

**`C`** When to trigger inline validation depends on the interaction and the type of error. Validating on blur (when the user leaves the field) is a reasonable default for most fields. For errors that cannot be detected until the full value is entered, validation on form submission with inline anchoring is appropriate. Avoid validating on each keystroke in a way that flags errors before the user has finished entering information — this is disruptive and creates premature anxiety.

### Recommendations

**`Rec`** For multi-field forms, provide a summary of errors at the top of the form *in addition to* inline errors — especially on page-level submission. Link each summary item to the relevant field.

**`Rec`** For positive validation (successfully formatted field), use a success indicator only when the confirmation genuinely reduces anxiety — for example, confirming a username is available, or that a password meets requirements. Avoid decorating every correct field with a green tick.

---

## Accessibility

- Every input must have a programmatic label: a `<label>` element associated via `for`/`id`, or an `aria-label` / `aria-labelledby` attribute
- Helper text must be associated with its field using `aria-describedby` so screen readers announce it
- Validation messages must be announced when they appear — use `aria-live` or associate the message with the field
- Required fields must be marked programmatically with `required` or `aria-required="true"`, not only visually
- Do not use colour alone to distinguish required fields, errors, or validated fields — always pair with a text or shape indicator
- Avoid using placeholder text to carry essential guidance. If placeholder text is used, it must meet applicable text contrast requirements (WCAG 1.4.3: minimum 4.5:1 for normal text); many browser defaults render placeholder text below this threshold. Placeholder text is also not reliably announced by all screen readers. Neither of these concerns prohibits placeholder text — they require it to be treated as a visual supplement, not a substitute for a label or helper text.

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

### Label and helper text

| Field | Label | Placeholder | Helper text |
|---|---|---|---|
| Email | "Email address" | "name@example.com" | "We'll use this to send your receipt." |
| Password (new) | "Create a password" | — | "At least 8 characters, including one number." |
| Date of birth | "Date of birth" | "DD/MM/YYYY" | — |
| Phone (optional) | "Phone number (optional)" | "+39 000 000 0000" | "Include your country code." |

### Validation messages

| Situation | Avoid | Use |
|---|---|---|
| Email format invalid | "Invalid email." | "Enter a valid email address, like name@example.com." |
| Password too short | "Password too short." | "Your password needs at least 8 characters." |
| Required field empty | "This field is required." | "Enter your [label]." |
| Date in wrong format | "Invalid date." | "Enter the date as DD/MM/YYYY." |

---

## Review checklist

Before publishing, verify:

- [ ] Every field has a persistent visible label (not placeholder-only)
- [ ] Labels use sentence case with no colon
- [ ] Required or optional fields are marked consistently using the right convention for the form
- [ ] Helper text for constrained fields is visible before the user submits
- [ ] Placeholder text, if used, shows a format example — not a repeat of the label
- [ ] Validation messages are specific: they name the problem and what to do
- [ ] Validation triggers at an appropriate point (on blur, on submission) — not on each keystroke in a way that flags errors prematurely
- [ ] All fields have programmatic labels; helper and validation text are associated via `aria-describedby`

---

## Related patterns

- [Error messages](error-messages.md) — Full guidance on validation message writing and anatomy
- [Buttons and CTAs](buttons-and-ctas.md) — For the form submission button
- [Helper text](../content-components/helper-text.md) — For the content component pattern
