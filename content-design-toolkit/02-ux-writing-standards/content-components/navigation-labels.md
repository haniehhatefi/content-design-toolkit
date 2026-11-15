# Navigation labels

Navigation labels are the words users use to find their way around a product: menu items, tabs, breadcrumbs, section headings in sidebars, and wayfinding links. They are among the most consequential content in a product because they are used continuously — a confusing navigation label causes repeated friction for the lifetime of the product.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Types of navigation labels

| Type | Purpose | Writing considerations |
|---|---|---|
| **Primary navigation** | Top-level destinations | Scannable; distinct; concise |
| **Secondary navigation** | Sub-destinations within a section | Specific; clearly subordinate |
| **Tabs** | Parallel views of a single context | Parallel structure; mutually exclusive |
| **Breadcrumbs** | Current location in a hierarchy | Reflect exact page or section titles |
| **Sidebar items** | Secondary destinations or tools | Noun-based for destinations; verb-based for actions |
| **In-page navigation** | Anchors to sections within a long page | Match the section heading exactly |

---

## Rules

**`Rec`** Use nouns or noun phrases as the default for navigation labels. Navigation typically describes destinations, not journeys — "Reports" is clearer than "See all your reports here". Exception: in task-oriented products (tools, creative software, workflows) where the primary destinations are actions, verb-based labels are appropriate. Do not mix noun and verb labels at the same navigation level without a clear structural reason.

> ❌ "See all your reports here" → ✅ "Reports" (destination-based)
> Task-oriented nav: ✅ "Create", "Publish", "Export" (verb-based, used consistently)

**`Rule`** Navigation items within the same level must follow parallel grammatical structure. If the first item is a noun, all items at that level should be nouns.

> ❌ "Dashboard / My settings / Help and support / Log out" (mixed forms)
> ✅ "Dashboard / Settings / Support / Sign out" (parallel nouns or noun phrases)

**`Rule`** Use sentence case. No title case unless following a product's established convention that explicitly requires it.

> ❌ "My Projects" / "Team Settings" → ✅ "My projects" / "Team settings"

**`Rule`** Breadcrumb labels must reflect the exact title of the page or section they link to. Do not abbreviate, paraphrase, or reword breadcrumb labels.

**`Rule`** Avoid ambiguous or jargon-heavy labels. If the label requires explanation, the information architecture needs attention — a tooltip on a nav item is a warning sign, not a solution.

---

## Recommendations

**`Rec`** Use the words the user would use to describe the destination, not the words the product team uses internally. Test label terms with real users when in doubt.

**`Rec`** Keep primary navigation labels short: one or two words is the target. Long labels in primary navigation increase cognitive load and cause overflow issues at smaller viewports.

**`Rec`** For products with both destinations and actions in navigation (a sidebar with both "Dashboard" and "Create report"), distinguish actions visually (icon, button style, position) so users can tell a destination apart from an action.

**`Rec`** For tabs, ensure the labels cover the full range of content mutually exclusively. Users should not have to guess which tab their content lives in.

**`Rec`** Avoid "My" as a possessive prefix in navigation unless there is a parallel "Team" or "Shared" label that makes the contrast meaningful. "My projects" is useful only if "Team projects" or "All projects" also exists.

---

## Contextual decisions

**`C`** Whether to use noun labels or verb labels for the primary navigation depends on the product's model. Destination-based products (content libraries, data products, settings areas) benefit from noun labels. Task-based products (tools, creative software, workflows) may benefit from verb labels. Do not mix unless there is a clear structural reason.

**`C`** For international products, test whether translated navigation labels fit the available space. Labels that work in English may be significantly longer in other languages.

**`C`** For icon-only navigation (collapsed sidebars, mobile bottom bars), every icon-only label must have a text alternative and a visible tooltip identifying the destination. Apply the [tooltips](tooltips.md) guidance for icon-only navigation items.

---

## Accessibility

- Navigation landmarks should use semantic HTML (`<nav>`) with an `aria-label` to distinguish multiple navigation regions on a page (for example, "Main navigation" vs. "Account navigation")
- Current page or active tab must be communicated programmatically with `aria-current="page"` or `aria-selected="true"` — not only visually
- Breadcrumb navigation should use `aria-label="Breadcrumb"` on the `<nav>` element and `aria-current="page"` on the final crumb
- Icon-only navigation items must have an accessible name via `aria-label` or visually hidden text — `title` attribute alone is not sufficient

---

## Illustrative examples

*(These examples demonstrate the patterns. Replace bracketed placeholders with your own context.)*

### Parallel structure

| Avoid (mixed forms) | Use (parallel nouns) |
|---|---|
| "Overview / View reports / Your team / Help" | "Overview / Reports / Team / Help" |
| "Dashboard / Create a project / Settings / Logging out" | "Dashboard / Projects / Settings / Sign out" |

### Specific vs. generic labels

| Generic | Specific |
|---|---|
| "Data" | "Analytics" / "Reports" / "Exports" (whichever reflects the content) |
| "Tools" | "Integrations" / "Automations" / "API" (name what is actually there) |
| "More" | List the items directly, or use "Settings" / "Account" with clear sub-navigation |

### Tab labels (parallel and mutually exclusive)

| Avoid | Use |
|---|---|
| "Active / My tasks / Done / Archived tasks" | "Active / Assigned to me / Completed / Archived" |
| "Overview / The details / Stats" | "Overview / Details / Statistics" |

---

## Real-world example

GOV.UK's navigation patterns are tested with real users and prioritise plain, commonly understood language. Their documentation on helping users navigate a service describes the principle that labels should use the words users would use, and should orient users by telling them where they are heading rather than describing the route. *(Source: [GOV.UK Design System — Help users navigate a service](https://design-system.service.gov.uk/patterns/navigate-a-service/), accessed 2024)*

---

## Review checklist

Before publishing, verify:

- [ ] All items at the same navigation level follow parallel grammatical structure
- [ ] Labels use sentence case
- [ ] Labels are nouns or noun phrases (or consistently verb-based for action-oriented nav)
- [ ] Breadcrumb labels match page/section titles exactly
- [ ] No ambiguous, jargon-heavy, or internally-focused labels
- [ ] Active/current state is communicated programmatically, not only visually
- [ ] Icon-only items have accessible labels

---

## Related patterns

- [Tooltips](tooltips.md) — For icon-only navigation labels and supplementary context
- [Buttons and CTAs](../microcopy-patterns/buttons-and-ctas.md) — For action items within navigation (distinct from destinations)
