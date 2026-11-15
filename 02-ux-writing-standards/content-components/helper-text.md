# Helper text

Helper text provides contextual guidance associated with a form field, control, or section of content. Essential guidance should remain persistently visible; supplementary guidance may be disclosed on focus when appropriate. Unlike tooltips (hover-triggered) or placeholder text (disappears on input), helper text does not require a hover or other interaction trigger to be available. It is the appropriate place for information the user needs before or during interaction, not only after a mistake.

This document covers helper text as a standalone component: its purpose, writing, accessibility, and behaviour. For the relationship between helper text, labels, placeholder text, and validation messages within a form, see [Form fields](../microcopy-patterns/form-fields.md).

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Helper text vs. related patterns

| Pattern | Triggered by | Persistence | Use for |
|---|---|---|---|
| **Helper text** | None — persistent | Visible or available on focus | Required context, constraints, format guidance |
| **Placeholder text** | Empty field | Disappears on input | Format examples only |
| **Tooltip** | Hover or focus | Transient | Supplementary information; not required |
| **Validation message** | User interaction | Appears after interaction | Error or success states |

If the user needs the information to complete the field correctly, use helper text — not placeholder text or a tooltip.

---

## Rules

**`Rule`** Use helper text for information that is needed before the user interacts with the field. If a constraint (password length, file size limit, accepted formats) can cause an error, it must be communicated in helper text, not only in a validation message.

**`Rule`** Helper text must remain visible when the field is in an error state. Do not replace helper text with the validation message in a way that removes the original guidance — the user may need both.

**`Rule`** Use sentence case. Full stop at the end of a complete sentence.

---

## Recommendations

**`Rec`** Structure helper text with the template: *[What to enter] / [Format] / [Why, if non-obvious].* Not all three components are always needed.

| Component | Example |
|---|---|
| What to enter | "Enter the email address you used at registration." |
| Format | "Use the format DD/MM/YYYY." |
| Why (optional) | "This is shared with your team." |

**`Rec`** Keep helper text to one or two short sentences. If a field requires more explanation than that, the design of the field or its surrounding context should be reconsidered.

**`Rec`** Use the reader's language, not the system's. Avoid describing fields in terms of their data type or technical behaviour.

> ❌ "This field accepts strings of alphanumeric characters, maximum 128 bytes."
> ✅ "Use letters and numbers only. Up to 128 characters."

**`Rec`** For fields with character limits, use a live counter that shows characters remaining, not only a static limit statement.

---

## Contextual decisions

**`C`** Whether to show helper text at all times or only when the field is focused depends on the importance of the information and the density of the form. Essential instructions — anything that could cause an error if missed — should be persistently visible. Supplementary context (a "why" clause, an example) can appear on focus only in dense forms where visual noise is a concern. The key distinction: essential information must not depend on a hover or focus trigger that a user might miss.

**`C`** For multi-step forms, helper text from a previous step should not carry over into subsequent steps — but decisions made in a previous step (a plan selected, a file already uploaded) that affect what a later step requires should be referenced.

---

## Accessibility

- Helper text must be associated with its field using `aria-describedby` so screen readers announce it when the field receives focus
- Do not hide helper text from assistive technology — if it is visible to sighted users, it must be accessible to screen reader users
- Ensure helper text has sufficient contrast against the background (WCAG 1.4.3: minimum 4.5:1 for normal text)
- Do not use helper text to convey information that is already in the label — this causes screen readers to announce redundant information

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

| Field | Label | Helper text |
|---|---|---|
| Password (new account) | "Create a password" | "At least 8 characters, including one number." |
| Upload field | "Upload your document" | "PDF, Word, or Excel files only. Maximum [size] MB." |
| Username | "Username" | "Letters, numbers, and underscores only. This will be visible to other users." |
| Payment reference | "Payment reference (optional)" | "If you have a reference number from your invoice, add it here." |
| Date field | "Date of birth" | "Enter as DD/MM/YYYY." |

---

## Review checklist

Before publishing, verify:

- [ ] Helper text covers information needed before the user interacts, not only after an error
- [ ] Helper text uses sentence case and ends with a full stop
- [ ] Copy is 1–2 sentences; uses plain language, not technical terminology
- [ ] Helper text remains visible (or accessible) in error states alongside the validation message
- [ ] Associated with its field via `aria-describedby`
- [ ] Contrast meets WCAG 1.4.3 minimum

---

## Related patterns

- [Form fields](../microcopy-patterns/form-fields.md) — Full guidance on the four text types in a form
- [Tooltips](tooltips.md) — For supplementary hover-triggered guidance
- [Error messages](../microcopy-patterns/error-messages.md) — For validation messages that complement helper text
