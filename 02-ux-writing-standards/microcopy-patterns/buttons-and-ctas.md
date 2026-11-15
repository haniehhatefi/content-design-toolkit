# Buttons and calls to action

Button labels are among the most-read text in any product. They appear at the moment of decision, carry the full weight of what the user is about to do, and must be unambiguous in a fraction of a second. They are also the most common place for inconsistent or vague writing to accumulate.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Types of buttons

| Type | Purpose | Writing implication |
|---|---|---|
| **Primary** | The main action on a screen | Must be specific and unambiguous |
| **Secondary** | Alternative or supporting action | Distinguish clearly from primary; avoid competition |
| **Destructive** | Permanently removes or deletes something | Label the specific destructive action; confirm before executing |
| **Ghost / tertiary** | Low-priority action or navigation | Often shorter; "Cancel", "Back", "Skip" |
| **Icon-only** | Action communicated visually | Requires a text alternative for accessibility |
| **Loading** | Busy state while an action processes | Reflects the action in progress |

---

## Rules

**`Rule`** Use an action verb. Every button label should begin with a verb that tells the user what will happen when they select it.

> ❌ "Confirmation" → ✅ "Confirm"
> ❌ "Deletion" → ✅ "Delete [item]"
> ❌ "Settings" (as an action) → ✅ "Edit settings"

**`Rule`** Be specific. Generic labels like "Submit", "OK", and "Yes" do not tell the user what they are committing to. Use the specific action and, where space allows, the object.

> ❌ "Submit" → ✅ "Send application"
> ❌ "OK" → ✅ "Got it" or the specific action
> ❌ "Yes" in a dialog → ✅ "Delete account"

**`Rec`** Use sentence case by default. Button labels follow the same capitalisation convention as the rest of the UI: sentence case unless a proper noun. If a product's established style guide specifies a different convention, follow it consistently across all buttons.

> ❌ "Save Changes" → ✅ "Save changes" (default)
> ❌ "Sign In" → ✅ "Sign in" (default)

**`Rule`** No punctuation. Button labels do not end with a full stop, exclamation mark, or question mark.

**`Rule`** For destructive actions, the button label must name the destructive action, not confirm it generically.

> ❌ "Yes, I'm sure" → ✅ "Delete account"
> ❌ "Confirm" → ✅ "Remove [item]"

**`Rule`** Icon-only buttons must have a text alternative (accessible label). The visible label is the action; the accessible label is what screen readers announce.

---

## Recommendations

**`Rec`** Keep labels short. Three words or fewer is a useful target for primary actions. Longer labels are acceptable when specificity matters more than brevity (for example, in a destructive action confirmation).

**`Rec`** Match the label to the page heading or task context. If the page is titled "Create a new account", the primary button should say "Create account", not "Continue" or "Next".

**`Rec`** Pair the primary action with a clear secondary option. If the primary action is "Delete account", the secondary should be "Cancel" — not "Go back" or "No".

**`Rec`** For multi-step flows, use step-specific labels rather than generic "Next". "Next" tells the user nothing; "Review order" or "Add payment details" tells them exactly where they are going.

**`Rec`** For loading states, reflect the action in progress rather than showing a spinner with no text.

> ❌ [spinner only]
> ✅ "Saving…" / "Sending…" / "Processing…"

**`Rec`** For CTAs in marketing contexts (landing pages, email, in-app promotions), use first-person language if it increases clarity and engagement. This is a contextual decision in UI copy.

> UI: "Start free trial"
> Marketing CTA: "Start my free trial"

---

## Contextual decisions

**`C`** Whether to include the object in a button label ("Save changes" vs. "Save") depends on context. In a dense interface with many save points, include the object for clarity. On a simple single-purpose screen, "Save" may be sufficient.

**`C`** "Cancel" vs. "Go back" vs. "No, keep [item]": the right label for a secondary action in a confirmation dialog depends on what the user is cancelling. When the consequence of the primary action is significant (deleting something), "No, keep [item]" is more helpful than "Cancel" because it confirms what will be preserved.

**`C`** For products with international audiences, avoid idioms and culturally specific expressions in button labels. "Let's go", "Get cracking", or "Dive in" may not translate clearly.

---

## Accessibility

- Every button must have an accessible name, either as its visible label or as an `aria-label` for icon-only buttons
- The accessible name should match (or start with) the visible label to support voice control users who activate buttons by speaking their label
- Avoid button labels that only make sense in context ("Click here", "Learn more"). Add context to the label itself, or use `aria-label` to provide the full context
- Distinguish destructive buttons visually (colour, weight) *and* through their label — do not rely on colour alone

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

### Primary actions

| Avoid | Use | Why |
|---|---|---|
| "Submit" | "Send application" | Specific action and object |
| "Continue" | "Review your order" | Tells the user what happens next |
| "OK" | "Got it" or the specific action | "OK" is non-committal |
| "Yes" | "Delete [item]" | Names the specific action |

### Destructive action dialogs

| Dialog | Avoid primary label | Use primary label | Use secondary label |
|---|---|---|---|
| Deleting a file | "Yes, delete" | "Delete [file name]" | "Cancel" |
| Removing a team member | "Remove" | "Remove [name] from team" | "Cancel" |
| Cancelling a subscription | "Confirm" | "Cancel subscription" | "Keep subscription" |

### Loading states

| Action | Static label | Loading label |
|---|---|---|
| Submitting a form | "Send" | "Sending…" |
| Saving work | "Save" | "Saving…" |
| Downloading a file | "Download" | "Preparing download…" |

---

## Real-world example

Apple's Human Interface Guidelines specify that action button titles "use a verb or verb phrase that describes the action — for example, 'Add', 'Delete', 'Save', or 'Get'." They also note that "Avoid using generic button titles like Yes and No, which don't convey what will happen when people tap them." *(Source: [Apple Human Interface Guidelines — Buttons](https://developer.apple.com/design/human-interface-guidelines/buttons), accessed 2024)*

---

## Review checklist

Before publishing, verify:

- [ ] Every button label begins with an action verb
- [ ] No labels use "Submit", "OK", or "Yes" as a final action
- [ ] Destructive action labels name the specific destructive action
- [ ] Labels follow the established capitalisation convention (sentence case by default) without end punctuation
- [ ] Icon-only buttons have an accessible label
- [ ] Multi-step flows use step-specific labels, not "Next"
- [ ] Loading states reflect the action in progress

---

## Related patterns

- [Confirmation dialogs](confirmation-dialogs.md) — For the full pattern around destructive action buttons
- [Error messages](error-messages.md) — For button labels in error recovery contexts
- [Form fields](form-fields.md) — For form submission button placement and labelling
