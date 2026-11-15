# Empty states

Empty states appear when a view has no content to display. They are among the most neglected pieces of interface copy — often written last, left as placeholders, or given the bare minimum. Yet empty states appear at the moments when a user most needs orientation: their first time in a product, when a search returns nothing, or when they have cleared their own content.

A well-written empty state turns an absence into an invitation.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Three types of empty state

Each type has a different user situation and requires different writing.

| Type | Situation | User state | Writing goal |
|---|---|---|---|
| **First use** | The user has not yet added any content | Curious, possibly uncertain | Invite; orient; remove friction |
| **User-cleared** | The user has deleted or archived all their content | Intentional; possibly relieved | Confirm the action; offer a next step |
| **No results** | A search, filter, or query returned nothing | Possibly frustrated | Explain what happened; help the user adjust |

---

## Anatomy of an empty state

A complete empty state has three parts. All three are not always necessary — apply judgement.

```
1. Explain        — What is this space for, or why is it empty
2. Invite         — What the user can do here
3. Call to action — The specific next step (a button or link)
```

**Illustrative example** *(Demonstrates the anatomy. Adapt to your context.)*

| Part | First-use example | No-results example |
|---|---|---|
| Explain | "You haven't added any [items] yet." | "No results for '[search term]'." |
| Invite | "Start by adding your first [item]." | "Try a different word or remove a filter." |
| CTA | "Add [item]" (button) | "Clear filters" (link or button) |

---

## Rules

**`Rule`** Every empty state must have at least an explanation and a next step. A blank screen, a spinner that never resolves, or the word "Empty" is not an empty state — it is an oversight.

**`Rule`** The call to action in a first-use empty state must match the product's primary action. If the product is for creating [items], the CTA should say "Create your first [item]", not a generic "Get started".

**`Rule`** For no-results states, never imply the fault is the user's. State what happened neutrally, then offer a way forward.

> ❌ "Your search didn't match anything."
> ✅ "No results for '[term]'. Try a different word or phrase."

---

## Recommendations

**`Rec`** For first-use empty states, write in the second person and address the user directly. This is a moment of invitation, not a system notification.

> ❌ "No items have been created."
> ✅ "You haven't added anything yet. Start by [CTA]."

**`Rec`** For user-cleared empty states, acknowledge the action briefly before moving to the next step. Confirming that the action worked reduces anxiety about data loss.

> "All [items] have been archived. [CTA: View archive] or [CTA: Add new [item]]"

**`Rec`** For no-results states, include the search term in the message so the user can verify what was searched.

> "No results for 'invoices from 2023'. Try removing the date filter or searching for a different term."

**`Rec`** Avoid apologising for empty states that are a normal part of the product lifecycle (first use, cleared view). Apology is appropriate only for unexpected failures.

**`Rec`** If the empty state offers a way to populate content, make the CTA the same as the primary action used elsewhere in the product — do not create a new, emergency-only CTA pattern just for empty states.

---

## Contextual decisions

**`C`** Whether to include an illustration or icon in an empty state is a design decision, but the writing should work without it. Do not write copy that relies on a visual to make sense.

**`C`** For products with multiple roles (admin vs. end user), the empty state may need to be different for each. An admin who can add content should see an invitation; an end user who cannot add content themselves may need a message pointing them to their administrator.

> Admin: "No [items] yet. Add your first [item] to get started."
> End user: "No [items] have been added yet. Contact your administrator to add [items]."

**`C`** For search-heavy products, consider whether a no-results state should offer related or suggested content, or only advice on adjusting the search. This depends on whether the product has the data to make relevant suggestions.

---

## Accessibility

- Empty state messages should be announced to screen readers when the view changes from populated to empty — ensure the content is in the DOM and not hidden from assistive technology
- CTAs in empty states follow the same rules as all buttons: begin with an action verb, be specific, and have an accessible label
- Avoid empty state designs that rely entirely on illustrations or icons with no text — these fail users who cannot see them

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

### First-use empty states

| View | Avoid | Use |
|---|---|---|
| Dashboard | "No data available." | "Nothing here yet. Add your first [item] to get started." [Add [item] button] |
| List view | "You have no [items]." | "You haven't created any [items] yet. [Create [item] button]" |
| Inbox | "Inbox empty." | "You're all caught up. New [messages] will appear here." |

### User-cleared states

| View | Avoid | Use |
|---|---|---|
| Completed tasks | "No tasks." | "No tasks here. [items] you complete will be archived automatically." |
| Deleted items | "Trash is empty." | "Nothing in the trash. [items] you delete will appear here for 30 days." |

### No-results states

| Search context | Avoid | Use |
|---|---|---|
| Keyword search | "No results found." | "No results for '[term]'. Try a different word or phrase." |
| Filtered view | "Nothing matches your filter." | "No [items] match these filters. [Clear filters link]" |
| Date range | "No results for this period." | "No [items] found between [date] and [date]. Try a wider date range." |

---

## Review checklist

Before publishing, verify:

- [ ] Every empty state has at least an explanation and a next step
- [ ] First-use states invite action, not describe absence
- [ ] No-results states include the search term and a way to adjust
- [ ] User-cleared states confirm the action briefly before offering a next step
- [ ] CTAs match the product's primary action verb and label
- [ ] The state is accessible: visible in the DOM, not colour-only, with specific CTA labels

---

## Related patterns

- [Buttons and CTAs](buttons-and-ctas.md) — For the call to action within empty states
- [Error messages](error-messages.md) — For when an empty state is caused by a failure, not just an absence
- [Onboarding](onboarding.md) — For first-use orientation beyond the empty state itself
