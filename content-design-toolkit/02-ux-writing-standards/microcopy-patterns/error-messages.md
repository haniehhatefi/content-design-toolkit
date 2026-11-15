# Error messages

Error messages appear when something prevents the user from completing their task. They are among the highest-stakes content in any product: a user reading an error message is already blocked, often frustrated, and looking for a way forward. Well-written error messages reduce that friction; poorly written ones compound it.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Types of error messages

This document covers four error types. Each has distinct writing requirements.

| Type | Where it appears | Trigger |
|---|---|---|
| **Inline validation** | Adjacent to a specific form field | Field-level input failure |
| **Form-level error** | At the top of a form or form section | Multiple field failures, or a submission-level failure |
| **Alert or banner** | Persistent across a page or screen | System-level issue affecting the current session |
| **Error page** | Replaces the entire page | Navigation failure, server error, permission denied |

---

## Anatomy of an error message

A complete error message has three parts. The third part is optional depending on context.

```
1. What went wrong     — State the problem clearly
2. Why (optional)      — Add only when the reason helps the user act
3. What to do          — Tell the user what to do next
```

**Illustrative example** *(Demonstrates the anatomy. Adapt to your context.)*

| Part | Example |
|---|---|
| What went wrong | "We couldn't save your changes." |
| Why (optional) | "Your session expired while you were editing." |
| What to do | "Sign in again to continue. Your draft has been kept." |

Not every error needs all three parts. A short inline validation error that says "Enter a valid email address" is complete. A system error affecting data the user worked on needs all three.

---

## Rules

**`Rule`** Every error message must tell the user what to do next, not only what went wrong.

**`Rule`** Never blame the user. Write errors from a neutral or system perspective, not an accusatory one.

> ❌ "You entered an invalid date."
> ✅ "Enter a date in DD/MM/YYYY format."

**`Rule`** Use plain language. Avoid technical codes, system terminology, or stack trace language in user-facing error messages. Log these internally; do not surface them.

> ❌ "HTTP 403: Forbidden. Access denied by resource policy."
> ✅ "You don't have permission to view this page. Contact your administrator if you think this is a mistake."

**`Rule`** For inline validation errors, place the error message adjacent to the field it refers to — not only at the top of the form.

**`Rec`** Use sentence case. No full stops on single-sentence inline errors; use full stops on multi-sentence messages.

---

## Recommendations

**`Rec`** Be specific. A specific error is more helpful than a generic one, even when the specific reason is technical — translate it into user-readable language.

> ❌ "Something went wrong."
> ✅ "We couldn't process your payment. Check your card details and try again."

**`Rec`** Distinguish user errors from system errors in your language. User errors (wrong input) should guide the user to fix their input. System errors (server failures, outages) should acknowledge that it is not the user's fault.

> User error: "Enter a date in DD/MM/YYYY format."
> System error: "Something went wrong on our end. Try again in a moment."

**`Rec`** Provide a path forward. Where possible, link to the specific place the user needs to go, rather than giving general instructions.

**`Rec`** Avoid multiple exclamation marks, all-caps, or dramatic language. Errors should be calm and practical, not alarming.

**`Rec`** For high-stakes errors (data loss, failed payment, security issue), confirm what has been preserved as well as what went wrong.

> "We couldn't complete your purchase. Your cart has been saved. Try again or contact support."

---

## Contextual decisions

**`C`** Whether to surface a *why* clause depends on whether it helps the user act. "Your session expired" is worth including when the user can re-trigger the action. "Our payment processor is temporarily unavailable" is worth including if it sets a reasonable expectation. Generic system-state information ("an internal error occurred") adds no value.

**`C`** The tone of an error message should match the severity of the consequence. A recoverable validation error (wrong format in a field) warrants a brief, calm correction. An unrecoverable data-loss event warrants a more considered message that acknowledges the impact.

**`C`** For products in regulated industries (finance, healthcare, legal), error messages may need to meet specific disclosure requirements. Consult your compliance or legal team before drafting error copy for sensitive flows.

---

## Accessibility

- Associate inline validation errors with their field using `aria-describedby` so screen readers announce them when the field receives focus
- Do not rely on colour alone to communicate an error — always include a text label or icon with a text alternative
- Ensure error messages are announced to screen readers when they appear; use `aria-live="assertive"` for critical errors, `aria-live="polite"` for less urgent validation feedback
- Avoid automatically moving focus to an error message unless the user has attempted to submit — interrupting mid-entry is disruptive

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

### Inline validation

| Situation | Avoid | Use |
|---|---|---|
| Required field left empty | "This field is required." | "Enter your [field name]." |
| Invalid email format | "Invalid email." | "Enter a valid email address, like name@example.com." |
| Password too short | "Password too short." | "Your password needs at least [n] characters." |
| File type not accepted | "Invalid file type." | "Upload a [accepted formats] file. This file is [actual format]." |

### System error

| Situation | Avoid | Use |
|---|---|---|
| Server error on page load | "Error 500." | "Something went wrong. Refresh the page or try again in a moment." |
| Cannot connect | "Connection failed." | "We can't reach our servers right now. Check your connection and try again." |
| Data not saved | "Save failed." | "We couldn't save your changes. Your last saved version is from [time]." |

### Error page

| Type | Heading | Body |
|---|---|---|
| Page not found (404) | "Page not found" | "The page you're looking for doesn't exist or has moved. [Link: Go to homepage]" |
| No access (403) | "You don't have access to this page" | "Contact your administrator if you think this is a mistake." |
| Server error (500) | "Something went wrong" | "We're having trouble right now. Try refreshing the page. If the problem continues, [link: contact support]." |

---

## Real-world example

Mailchimp's UX writing guidelines describe errors as an opportunity to be human: "Avoid jargon or abbreviations. Write like a smart friend who happens to be an expert." Their error messages consistently include both what went wrong and what to do next, in plain language. *(Source: [Mailchimp Content Style Guide — Writing for Errors](https://styleguide.mailchimp.com/writing-for-accessibility/), accessed 2024)*

---

## Review checklist

Before publishing, verify:

- [ ] The error says what went wrong (not only that something went wrong)
- [ ] The error tells the user what to do next
- [ ] The language is plain — no technical codes, jargon, or system terminology
- [ ] The error does not blame the user
- [ ] Inline errors are adjacent to the field they refer to
- [ ] The tone matches the severity (calm for minor errors, considered for data loss or high-stakes failures)
- [ ] The message is accessible: not colour-only, associated with its field, announced to screen readers

---

## Related patterns

- [Form fields](form-fields.md) — For validation message placement and field-level error states
- [Notifications](../content-components/notifications.md) — For persistent error alerts and banners
- [Confirmation dialogs](confirmation-dialogs.md) — For errors within destructive action flows
