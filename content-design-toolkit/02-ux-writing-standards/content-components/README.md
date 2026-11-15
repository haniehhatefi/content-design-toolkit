# Content components

Content components are the larger-scale structural elements that carry information across a product: notifications, tooltips, helper text, and navigation labels. Where microcopy patterns focus on transactional moments (errors, confirmations, form completion), content components focus on the ongoing informational layer of a product.

---

## Components in this sub-module

| Component | What it covers |
|---|---|
| [Notifications](notifications.md) | Toasts, banners, alerts, notification centres, and badges |
| [Tooltips](tooltips.md) | Hover-triggered supplementary information |
| [Helper text](helper-text.md) | Persistent contextual guidance for fields and controls |
| [Navigation labels](navigation-labels.md) | Menu items, tabs, breadcrumbs, and wayfinding labels |

---

## How to use these documents

Each component document follows a consistent structure:

1. **Overview** — what the component is and when it applies
2. **Types** — the variants of the component and when to use each
3. **Rules** — must-follow standards
4. **Recommendations** — strong defaults; exceptions acceptable when justified
5. **Contextual decisions** — depends on product type, audience, or platform
6. **Accessibility** — programmatic and semantic requirements
7. **Illustrative examples** — context-independent examples with bracketed placeholders
8. **Review checklist** — a gate before content ships

For an explanation of the Rule / Recommendation / Contextual decision framework, see the [Module 2 README](../README.md).

---

## Principles that apply across all content components

**Match the component to its urgency.** The most common failure in notifications is using a high-urgency component (modal, error banner) for low-urgency information — and low-urgency components (toast, badge) for information the user needs to act on. The component choice sets user expectation.

**Persistent visibility is not always better.** Tooltips, notifications, and helper text occupy space. Show only what is relevant at the moment the user needs it. If a component is always visible and rarely read, reconsider whether it is adding value or noise.

**Navigation is wayfinding, not marketing.** Navigation labels should describe where users are going, not persuade them to go there. The most effective navigation labels are precise, mutually exclusive, and use the user's vocabulary.

**Every component that communicates something must be accessible.** Programmatic requirements (aria-live, aria-describedby, aria-current) are not optional enhancements. Each component document includes the specific implementation requirements.

---

## Related sub-modules

- [Microcopy patterns](../microcopy-patterns/README.md) — Short functional copy for transactional moments
- [Readability standards](../readability-standards.md) — Grade level targets; notifications and in-product help target Grade 7–8
- [Inclusive language guide](../inclusive-language-guide.md) — Inclusive language standards applied to component copy
