# Notifications

Notifications inform users of events, states, or changes that require their attention or awareness. They range from brief success confirmations to persistent system-level warnings. Because notifications appear across the full range of emotional states — relief, frustration, urgency — they require careful calibration of tone and urgency.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Types of notifications

| Type | Persistence | Trigger | Use for |
|---|---|---|---|
| **Toast / snackbar** | Auto-dismisses (3–5 seconds) | Low-urgency system feedback | Confirmations, minor status changes |
| **Banner (inline)** | Persists until dismissed or resolved | Page or section-level state | Warnings, information, non-blocking errors |
| **Alert (modal-adjacent)** | Persists until action taken | Blocking state requiring a decision | Critical errors, required confirmations |
| **Notification centre** | Persists; user-managed | Asynchronous events | Activity, mentions, background completions |
| **Badge** | Persists until viewed | Unread count | Unread items in a feed or inbox |

---

## Rules

**`Rule`** Match the notification type to the urgency and persistence of the information. A confirmation that a file was saved does not need a persistent banner. A warning that a session is about to expire does.

**`Rule`** Every notification must state what happened and, where action is required, what to do. A notification that says only "Error" or "Update" is not complete.

**`Rule`** Use specific, not generic, language. The notification should tell the user exactly what happened — not that something happened.

> ❌ "Something was updated." → ✅ "[Item name] has been updated."
> ❌ "Error." → ✅ "We couldn't save your changes. Try again."

**`Rule`** For auto-dismissing toasts, do not place critical information or required actions in them. Users will not see them if they are looking elsewhere, and they cannot interact with a dismissed notification.

---

## Recommendations

**`Rec`** For success toasts, keep copy to one sentence: what was completed. The user knows they triggered the action; confirm it briefly and get out of the way.

> ✅ "[Item name] saved." / "File uploaded." / "Invitation sent to [name]."

**`Rec`** For warning banners, include the reason and the consequence, not only the warning.

> ❌ "Warning: check your settings."
> ✅ "Your [plan name] plan ends on [date]. [link: Renew to keep access]"

**`Rec`** For error notifications in the notification centre (background process failures), include a link or action that takes the user directly to the place they need to fix the issue.

**`Rec`** For timed notifications (session expiry, deadline approaching), include the specific time remaining, not vague urgency.

> ❌ "Your session is about to expire."
> ✅ "Your session expires in 5 minutes. [link: Extend session]"

---

## Contextual decisions

**`C`** Whether a notification should use first or third person depends on whether the product has a voice in the product: "We couldn't send your message" (product as narrator) vs. "Your message couldn't be sent" (passive, neutral). Both are acceptable; consistency within a product matters more than the choice itself.

**`C`** For notification centres aggregating asynchronous events, determine whether to group similar notifications ("3 new mentions") or list them individually. Grouping reduces noise for high-volume products; listing preserves context for low-volume ones.

---

## Accessibility

- Notifications that appear without user action should be announced by screen readers via `aria-live`. Use `aria-live="assertive"` for urgent/blocking notifications; use `aria-live="polite"` for non-urgent ones
- Do not use `aria-live="assertive"` for routine success messages — this interrupts screen reader users unnecessarily
- Notifications should not disappear before the user has had time to read them: 3 seconds is a minimum for short text; longer messages warrant more time. Providing a way to pause or extend auto-dismissing notifications is a good practice, particularly for users who need more time to process content.
- WCAG 2.2.2 (Pause, Stop, Hide) applies when a notification moves, blinks, scrolls, or auto-updates its content in a way that starts automatically and lasts more than 5 seconds in parallel with other content. A static toast that fades out is not typically covered by this criterion; an animated or continuously updating notification is. When in doubt, provide a way to pause the animation.

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

### Toast (success)

| Avoid | Use |
|---|---|
| "Done!" | "[Item name] saved." |
| "Success." | "Invitation sent to [email address]." |
| "Updated." | "[Item name] has been updated." |

### Banner (warning)

| Situation | Message |
|---|---|
| Trial ending | "Your trial ends in [n] days. [link: Upgrade to keep access]" |
| Unsaved changes | "You have unsaved changes. [link: Save now] or they'll be lost when you leave." |
| Read-only mode | "You're viewing a read-only copy. [link: Request edit access] to make changes." |

### Error notification

| Situation | Message |
|---|---|
| Background sync failed | "We couldn't sync your [items]. [link: Try again] or [link: check your connection]." |
| Export failed | "Your export of [n] [items] failed. [link: Retry export]" |

---

## Review checklist

Before publishing, verify:

- [ ] The notification type matches the urgency and persistence of the information
- [ ] Critical actions are not placed in auto-dismissing toasts
- [ ] Specific: names the item, action, or state — not generic "something happened"
- [ ] Warning and error notifications include the consequence and what to do
- [ ] Timed notifications include the specific time, not vague urgency
- [ ] `aria-live` levels are appropriate to notification urgency
- [ ] Auto-dismissing notifications persist long enough to be read

---

## Related patterns

- [Error messages](../microcopy-patterns/error-messages.md) — For detailed error message anatomy
- [Confirmation dialogs](../microcopy-patterns/confirmation-dialogs.md) — For blocking notifications requiring a decision
