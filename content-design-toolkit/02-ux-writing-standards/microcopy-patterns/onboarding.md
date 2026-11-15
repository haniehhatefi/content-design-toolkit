# Onboarding

Onboarding copy covers the first-use experience: orientation messages, welcome screens, setup flows, feature introductions, and progressive disclosure patterns. It is the content that helps a new user understand what a product does and how to get started.

Good onboarding copy is not a tour — it is a shortcut to the moment the product becomes useful.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Types of onboarding content

| Type | Purpose | When it appears |
|---|---|---|
| **Welcome screen** | Orients the user and sets expectations for setup | Immediately after first sign-in |
| **Setup flow** | Collects the information needed to personalise the experience | First-use configuration |
| **Empty state (first-use)** | Invites the user to take their first action | First time a view is empty |
| **Feature introduction** | Introduces a new feature to existing users | On first encounter after a release |
| **Tooltip / coach mark** | Contextual hint about a specific UI element | First time an element is encountered |
| **Progress indicator** | Shows how much of a setup or onboarding flow remains | Throughout a multi-step process |

For empty states specifically, see [Empty states](empty-states.md). For tooltips, see [Tooltips](../content-components/tooltips.md).

---

## Rules

**`Rule`** Onboarding copy must state what the product does or what the step achieves — not celebrate that the user exists.

> ❌ "Welcome! We're so excited to have you here!"
> ✅ "Welcome to [product]. Here's how to get started."

**`Rec`** When asking for information whose purpose is not self-evident, explain why it is needed alongside the field or step heading. This reduces abandonment and builds trust. Reserve the explanation for cases where users might genuinely wonder why a product is asking.

> ❌ Label: "Team size" (no explanation)
> ✅ Label: "Team size" + Helper text: "We use this to suggest the right [plan or feature]."

**`Rule`** Progress indicators in multi-step flows must accurately reflect progress. Do not show 3 steps when there are 7 — this causes abandonment when users realise the flow is longer than indicated.

**`C`** Include a skip or dismiss option for steps that are genuinely optional — where another route to the same outcome exists and completing the step is not required for the product to function. The key question is whether the step is truly optional: a step that unlocks a core feature may be essential even if it feels like personalisation. Where a step can safely be skipped, offer the option; requiring it creates friction and reduces trust.

---

## Recommendations

**`Rec`** Lead with the value, not the feature. Explain what the user will be able to do, not what the product has built.

> ❌ "We've built a powerful new dashboard with real-time analytics and customisable widgets."
> ✅ "Your dashboard shows everything you need to manage [task]. You can customise it once you're set up."

**`Rec`** Set expectations upfront. For setup flows with multiple steps, tell the user at the beginning approximately how long it will take and what they will need.

> "Setting up takes about 3 minutes. You'll need your [required item] and [required item]."

**`Rec`** Use short sentences and short steps. If a single onboarding screen requires more than 3 short sentences to explain, the step should be redesigned or split.

**`Rec`** Acknowledge what the user has already done before asking for the next thing. Progress validation reduces cognitive load.

> "Great, your account is set up. Now add your first [item] to get started."

**`Rec`** For feature introductions to existing users, acknowledge that the user knows the product already. Do not re-onboard; introduce.

> ❌ "Welcome to [product]. Here's how to use [feature]..."
> ✅ "New: [Feature name]. You can now [specific capability]. [CTA: Try it now]"

---

## Contextual decisions

**`C`** Whether to use a modal overlay, a full-page screen, or inline tooltips for onboarding depends on the complexity of the product and the confidence of the user. A product with a single clear first action may need only an empty state; a complex multi-module product may need a guided setup flow.

**`C`** Whether to include a product tour depends on the discoverability of core features. Tours should be opt-in, dismissable, and short — a tour of more than 5 steps is likely too long.

**`C`** For B2B products, the person completing setup may not be the person who will use the product day-to-day. Consider whether the onboarding copy addresses the administrator (setting up for others) or the end user (setting up for themselves).

---

## Accessibility

- Onboarding modals and overlay tours must be accessible to keyboard users: focus must be trapped in the modal, and Escape should dismiss it
- Coach marks and tooltips that appear automatically must not block interaction with the underlying interface for keyboard users
- Progress indicators should communicate progress both visually and in text: "Step 2 of 5" or an equivalent screen-reader announcement
- Avoid using colour alone to show which step is current in a progress indicator

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

### Welcome screen

| Element | Avoid | Use |
|---|---|---|
| Heading | "Welcome to [product]! 🎉" | "Welcome to [product]." |
| Body | "We're thrilled to have you on board. Let's get you started on your journey." | "Let's set up your account. This takes about 3 minutes." |
| CTA | "Let's go!" | "Set up your account" |

### Setup flow step

| Element | Example |
|---|---|
| Step label | "Step 1 of 3 — Your workspace" |
| Heading | "Name your workspace" |
| Helper text | "This is what your team will see when they're invited." |
| Input label | "Workspace name" |
| CTA | "Continue" (or "Set up team" for the final step) |

### Feature introduction (existing users)

| Element | Example |
|---|---|
| Heading | "New: [Feature name]" |
| Body | "You can now [specific capability]. [Short explanation of when it's useful — 1 sentence.]" |
| Primary CTA | "Try [Feature name]" |
| Secondary CTA | "Remind me later" |

---

## Review checklist

Before publishing, verify:

- [ ] The welcome copy states what the product does or the step achieves — not just that the user has arrived
- [ ] Steps asking for non-obvious information explain why it is needed
- [ ] Progress indicators accurately reflect the full number of steps
- [ ] Genuinely optional steps include a skip option (or the step is essential to the product's core function)
- [ ] The expected time and requirements are stated upfront for setup flows
- [ ] Feature introductions are addressed to existing users, not new ones
- [ ] Modals and tours are accessible: focus-trapped, keyboard-navigable, dismissable

---

## Related patterns

- [Empty states](empty-states.md) — For first-use empty states that form part of the onboarding experience
- [Tooltips](../content-components/tooltips.md) — For coach marks and contextual hints
- [Buttons and CTAs](buttons-and-ctas.md) — For step-specific CTA labelling in multi-step flows
