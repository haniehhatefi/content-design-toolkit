# Tooltips

Tooltips provide brief contextual help about a specific UI element. They appear on hover or keyboard focus. Because they are transient and require deliberate discovery, they are not the right place for essential information — they supplement; they do not replace.

For tooltip content to be accessible, it must meet WCAG 1.4.13 (content on hover or focus): it must be dismissible without moving focus or hover (typically with Escape), hoverable (the user can move their pointer over the tooltip without it disappearing), and persistent (it stays visible until the trigger loses hover or focus, or the user dismisses it).

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## When to use tooltips

Use a tooltip when:
- An interface element (icon, control, truncated text) is not self-explanatory and a brief label would clarify it
- A constraint or requirement on a field or action benefits from extra context, but not enough to warrant persistent helper text
- An icon-only button needs to identify what it does for sighted users who do not use assistive technology

Do not use a tooltip when:
- The information is essential for the user to complete their task (use helper text or inline guidance instead)
- The user is on a touch device — hover-based tooltips are not accessible on mobile
- The explanation requires more than two short sentences (use a modal, side panel, or help article instead)

---

## Rules

**`Rule`** Tooltips must not contain information that is required to complete a task. Required information must be visible without hover or focus.

**`Rule`** Tooltips must be accessible: triggered by keyboard focus as well as mouse hover, and their content must be available to screen readers. Use `aria-describedby` with a matching `id` on the tooltip element, or `role="tooltip"`, to associate the tooltip content with its trigger.

**`Rule`** Keep tooltip copy to 1–2 sentences. If more is needed, link to documentation instead.

**`Rule`** Use sentence case. No full stop on a single-sentence tooltip; use full stops on multi-sentence tooltips.

---

## Recommendations

**`Rec`** Write tooltips as statements, not labels. A tooltip that says "Delete" is a label — it repeats what the button already shows. A tooltip that says "Permanently remove this item from your account" adds meaning.

**`Rec`** Lead with what the action does, not what the element is called.

> ❌ "Export button: exports your data."
> ✅ "Download your data as a CSV file."

**`Rec`** For tooltips on disabled controls, explain why the control is disabled and what the user can do to enable it.

> ❌ [Tooltip on disabled button: "Disabled"]
> ✅ [Tooltip on disabled button: "Only administrators can change this setting."]

---

## Contextual decisions

**`C`** Whether to use a tooltip or a helper text depends on how critical the information is and whether it needs to be available on mobile. If both desktop and mobile users need the information, use helper text. If the information is supplementary and desktop-only, a tooltip is appropriate.

**`C`** For information-dense professional tools (data products, developer tools, admin interfaces), tooltips can carry more technical detail without cluttering the UI. For consumer products, the bar for adding a tooltip should be higher — most interactions should be self-explanatory.

---

## Accessibility

- Tooltips must be triggerable by keyboard focus, not only by mouse hover
- Tooltip content must be associated with its trigger element using `aria-describedby` or `role="tooltip"` so screen readers announce it
- Do not use `title` attributes as the mechanism for tooltip content — they are not reliably announced by screen readers, are inaccessible on touch devices, and do not meet WCAG 1.4.13 requirements
- Tooltip content that appears on hover or focus must meet WCAG 1.4.13: dismissible without moving focus (typically Escape), hoverable (pointer can move over it without dismissal), and persistent until focus or hover is intentionally removed
- Do not place interactive content (links, buttons) inside a tooltip — these are not reachable by keyboard or touch
- Ensure the tooltip does not obscure other content when it appears

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

| Trigger element | Avoid | Use |
|---|---|---|
| Icon-only archive button | "Archive" (repeats the icon label) | "Move this [item] to your archive. You can restore it later." |
| Disabled "Publish" button | "Disabled" | "Complete all required fields before publishing." |
| "i" information icon on a field | "Information" | "This [setting] affects how [item] appears for all users in your workspace." |
| Character-limited field near its limit | (no tooltip) | "You have [n] characters remaining." |

---

## Review checklist

Before publishing, verify:

- [ ] The tooltip adds meaning beyond the element label — it does not simply repeat it
- [ ] The information is supplementary, not required for task completion
- [ ] Copy is 1–2 sentences; sentence case; full stop on multi-sentence only
- [ ] Tooltip is triggered by keyboard focus as well as hover
- [ ] Tooltip is associated with its trigger element for screen reader access
- [ ] No interactive content (links, buttons) inside the tooltip

---

## Related patterns

- [Helper text](helper-text.md) — For persistent contextual guidance that cannot rely on hover
- [Onboarding](../microcopy-patterns/onboarding.md) — For coach marks and first-use tooltips in guided tours
- [Navigation labels](navigation-labels.md) — For tooltips on icon-only navigation elements
