# Brand voice audit template

Use this template to assess existing content against the voice principles and tone standards in this module. It is a process document, not just a scoring rubric — follow the phases in order.

An audit is most useful when you:
- Are joining a product team and want to understand the current state of its content
- Want to establish a baseline before introducing or updating voice guidelines
- Need evidence to make the case for content investment

---

## Before you start

**Define your scope.** A full audit of a large product can take weeks. For a first audit, pick one content area: a user flow, a notification set, a help section, or an onboarding sequence. Document the scope before you begin so you can communicate it clearly.

**Set up your inventory.** You will need a spreadsheet with one row per piece of content. The columns are defined in Phase 1 below.

**Align on the voice attributes.** Before scoring, make sure everyone involved in the audit agrees on what each voice attribute means. Use [voice principles](voice-principles.md) as the shared reference.

**Decide who is scoring.** A single scorer brings consistency; two scorers bring calibration. If two people score the same content independently and disagree by more than one point, discuss before finalising.

---

## Phase 1 — Inventory

Collect every piece of content in scope and record it in your inventory.

**Inventory columns:**

| Column | What to record |
|---|---|
| ID | A unique reference number (V001, V002, etc.) |
| Location | Where the content appears (screen name, flow step, component name) |
| Content | The exact text, copied verbatim |
| Content type | Button, error message, heading, body copy, tooltip, notification, placeholder text, etc. |
| Screenshot or reference | A link or file name so the content can be located easily |

**Collection tips:**
- Screenshot the content in context, not just the text — the surrounding interface affects how the text reads
- Include helper text, placeholder text, and microcopy, not just headings and body copy
- For flows, go through every possible path, including error and edge-case states
- Include email subject lines and notification copy, not just UI copy, if they are in scope

---

## Phase 2 — Score

Score each piece of content against the three core voice attributes and two cross-cutting writing standards using a 1–3 scale.

The distinction matters for how you interpret findings: a low score on Clear, Human, or Helpful indicates a voice alignment problem — the content does not sound like the product. A low score on Direct or Consistent indicates a writing quality issue — the content could be improved regardless of voice fit. See [voice principles](voice-principles.md) for the full explanation of this distinction.

**Scoring rubric:**

| Score | Meaning |
|---|---|
| **3 — On** | Clearly demonstrates this attribute or standard |
| **2 — Partial** | Shows some signs but inconsistently or incompletely |
| **1 — Off** | Contradicts or ignores this attribute or standard |
| **N/A** | Not relevant to this content type in this context |

**Scoring columns (add to your inventory):**

*Core voice attributes:*

| Attribute | Score (1–3 or N/A) | Notes |
|---|---|---|
| Clear | | |
| Human | | |
| Helpful | | |

*Cross-cutting writing standards:*

| Standard | Score (1–3 or N/A) | Notes |
|---|---|---|
| Direct | | |
| Consistent | | |

*Summary:*

| | Score | Notes |
|---|---|---|
| **Voice overall** | | Average of Clear, Human, Helpful (exclude N/A) |
| **Writing standards overall** | | Average of Direct, Consistent (exclude N/A) |

**Using the Notes column:** Record why you gave a score and what specifically would change it. Notes are what make the audit actionable — a score without a note is not useful when it comes to prioritising changes.

**Scoring examples:**

> *Content: "An error has occurred during the processing of your submission."*
> Clear: 1 — Off voice. Uses passive construction and nominalisations. Would score 3 as: "Something went wrong. Try again." Human: 1 — Off voice. Sounds like a system log, not a person.

> *Content: "Save changes"*
> Clear: 3 — On voice. Straightforward imperative. Direct: 3 — On voice. Consistent: N/A — cannot assess consistency from a single instance.

---

## Phase 3 — Identify patterns

Once all content is scored, look for patterns across the inventory.

**Questions to ask:**

- Which attributes consistently score low? This indicates a systemic gap.
- Which content types perform worst? This indicates where effort will have the highest impact.
- Which flows or areas score lowest? This indicates where users may be experiencing friction.
- Are there isolated pieces of content that score very differently from surrounding content? This may indicate inconsistency across writers or through incomplete updates.

**Pattern summary format:**

*Core voice attributes:*

| Attribute | Average score | Lowest-scoring content type | Key observation |
|---|---|---|---|
| Clear | | | |
| Human | | | |
| Helpful | | | |

*Cross-cutting writing standards:*

| Standard | Average score | Lowest-scoring content type | Key observation |
|---|---|---|---|
| Direct | | | |
| Consistent | | | |

---

## Phase 4 — Prioritise

Not all findings are equal. Prioritise based on two factors: user impact and effort to fix.

**Priority matrix:**

| | Low effort | High effort |
|---|---|---|
| **High user impact** | Fix first | Plan into the roadmap |
| **Low user impact** | Fix when passing through | Deprioritise |

**User impact is high when:**
- The content appears at a high-traffic moment (sign-in, checkout, error recovery)
- Getting it wrong causes the user to fail their task
- The content contributes to trust or safety decisions

**Effort is low when:**
- The fix is a wording change with no design or engineering change required
- The content appears in one place, not in a component used across the product
- The change does not need legal, compliance, or brand review

---

## Phase 5 — Document and share

**What to include in your audit report:**

1. **Scope** — What you audited and what you excluded, and why
2. **Method** — How you scored (link to this document and to [voice principles](voice-principles.md))
3. **Summary findings** — The pattern summary from Phase 3
4. **Priority recommendations** — Your top 10–15 items with priority ratings
5. **Raw inventory** — The full scored inventory as an appendix

**How to frame the audit:**

The audit is evidence for content investment, not a grade for the team. Frame findings as: *"This content area has an opportunity to better serve users by [improvement]"* rather than *"This content is bad."*

Share the summary findings with product, design, and engineering leads. Share the full inventory with anyone doing the fix work.

---

## Related documents

- [Voice principles](voice-principles.md) — The attributes you are scoring against
- [Tone spectrum](tone-spectrum.md) — Tone considerations for specific content types during scoring
- Before and after documentation — For capturing specific content changes recommended by the audit: record the original wording, the recommended revision, and the reason for the change
- Glossary — For standardising inconsistent terms identified during the audit: list the preferred term, any variants to retire, and the decision rationale
