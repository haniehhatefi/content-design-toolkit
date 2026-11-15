# Confirmation dialogs

A confirmation dialog asks the user to verify an action before the system executes it. The purpose is to prevent accidental or irreversible actions — not to slow down confident users who know what they are doing.

Well-written confirmation dialogs inform and protect. Poorly written ones are either alarming (causing unnecessary anxiety) or so generic (causing confirmation blindness) that users click through without reading.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Two categories of confirmation dialog

The writing requirements differ significantly based on whether an action can be reversed.

| Category | Reversibility | Writing approach |
|---|---|---|
| **Reversible action** | The user can undo or recover the action | Brief; clarifying; don't over-warn |
| **Irreversible action** | The action permanently removes, deletes, or commits something | Specific; states the consequence explicitly; labels name the action |

If a deletion can be recovered (from a trash folder, within a grace period), it is reversible. If it is permanent with no recovery path, it is irreversible.

---

## Anatomy of a confirmation dialog

```
1. Heading         — What is being confirmed, stated as action or question
2. Body            — The consequence, and any recovery information
3. Primary action  — The confirmation button (names the action specifically)
4. Secondary action — The cancel or dismiss button
```

---

## Rules

**`Rule`** For irreversible actions, the dialog body must state the consequence explicitly. "You can't undo this" or "This can't be recovered" must appear in the body — not only implied by the action label.

**`Rule`** The primary action button must name the specific action, not use a generic confirmation label. This is the last moment a user can understand what they are committing to.

> ❌ "Confirm" / "Yes" / "OK" → ✅ "Delete account" / "Remove [name]" / "Cancel subscription"

**`C`** The secondary action should make the safe alternative clear. "Cancel" is a good default for most confirmation dialogs triggered mid-task. Where naming the preserved object is clearer — for example, "Keep subscription" or "Keep file" — use the more specific label. Avoid "No" and "Go back": they are less explicit about what is being preserved or declined.

**`Rule`** Confirmation dialogs must not be used for actions that are easily reversible. Asking for confirmation on every action trains users to click through without reading — the opposite of the intended effect.

---

## Recommendations

**`Rec`** For irreversible actions, name the specific thing being deleted or removed in the body text, not only the type of object.

> ❌ "This will permanently delete your account."
> ✅ "This will permanently delete your account and all [n] [items]. You won't be able to recover it."

**`Rec`** For reversible actions, acknowledge the recovery path in the body. This reduces anxiety and makes the dialog feel proportionate.

> "Move [item name] to the trash? You can restore it from the trash within 30 days."

**`Rec`** Use a question for the heading of reversible actions, a statement for irreversible ones. The question form ("Move this to trash?") is appropriate when the user might reconsider; the statement form ("Delete this permanently") signals finality.

**`Rec`** Avoid phrases that perform alarm without adding information: "Warning!", "Are you absolutely sure?", "This cannot be undone (!!!)". State the consequence plainly.

**`Rec`** For destructive actions on content the user named (a file, a project, a contact), include the name in the dialog to confirm what is being acted on.

> "Delete 'Q4 Report Draft'? This can't be undone."

---

## Contextual decisions

**`C`** For deletion of multiple selected items, determine whether to summarise or list them. For 2–5 items, listing them gives users a final check. For more, summarise by count: "Delete 23 items? This can't be undone."

**`C`** Whether to use a question or a statement for the heading of an irreversible action depends on how certain the user is likely to be when they reach this point. If the user has gone through multiple deliberate steps to reach the deletion dialog, a statement heading is appropriate. If the action could be triggered accidentally, a question heading is more considered.

**`C`** Some products add a confirmation step (typing the name of what is being deleted) for high-consequence irreversible actions (deleting an account, purging a database, removing a workspace). This is appropriate when the consequence is catastrophic; it is not appropriate for routine deletions.

**`C`** For products in regulated industries, confirmation dialogs for sensitive actions may require additional legal review.

---

## Accessibility

- Focus must move to the dialog when it opens, so keyboard and screen reader users can interact with it
- The dialog must be trapped: focus should not be able to leave the dialog while it is open
- The heading, body, and buttons should be semantically structured so screen readers announce them in order
- Escape key should trigger the cancel action, not the confirmation
- The destructive button should not be the first focusable element in the dialog — ensure the cancel or secondary action is accessible without navigating past the destructive option

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

### Reversible action

| Element | Example |
|---|---|
| Heading | "Move '[item name]' to trash?" |
| Body | "You can restore it from the trash within 30 days." |
| Primary action | "Move to trash" |
| Secondary action | "Cancel" |

### Irreversible action — single item

| Element | Example |
|---|---|
| Heading | "Delete '[item name]' permanently" |
| Body | "This can't be undone. All [associated data] will also be removed." |
| Primary action | "Delete permanently" |
| Secondary action | "Cancel" |

### Irreversible action — account level

| Element | Example |
|---|---|
| Heading | "Delete your account" |
| Body | "This will permanently delete your account and all [n] [items]. You won't be able to sign in or recover your data." |
| Primary action | "Delete account" |
| Secondary action | "Cancel" |

### Reversible subscription change

| Element | Example |
|---|---|
| Heading | "Cancel your subscription?" |
| Body | "You'll keep access until [end date]. After that, you won't be charged again." |
| Primary action | "Cancel subscription" |
| Secondary action | "Keep subscription" |

---

## Review checklist

Before publishing, verify:

- [ ] The dialog is used only for actions that warrant confirmation (not every minor action)
- [ ] The body explicitly states the consequence for irreversible actions
- [ ] The primary action button names the specific action — no "Confirm", "Yes", or "OK"
- [ ] The secondary action clearly identifies the safe alternative ("Cancel" by default, or a specific "Keep [item]" where the object is named)
- [ ] Recovery paths are mentioned for reversible actions
- [ ] Focus management is implemented: dialog traps focus, Escape closes the dialog
- [ ] Specific item names are included for deletions where there is a risk of confusion

---

## Related patterns

- [Buttons and CTAs](buttons-and-ctas.md) — For destructive button labelling in general
- [Error messages](error-messages.md) — For handling errors within a confirmation flow
- [Notifications](../content-components/notifications.md) — For post-confirmation success or failure messages
