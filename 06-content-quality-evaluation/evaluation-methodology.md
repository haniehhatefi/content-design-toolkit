# Evaluation Methodology

**Phase 7: Content Quality Evaluation**

---

## Overview

This document describes a structured process for scoping, conducting, and documenting a content quality evaluation using the dimensions defined in `quality-dimensions.md`. It applies whether the evaluation is part of an active content creation workflow, a review of existing content, or an assessment of a content collection.

The evaluation methodology does not introduce new approval steps or checkpoints. It provides a consistent process for identifying and documenting quality findings. Where findings require action — revision, verification, or escalation — they route to the existing Phase 5 checkpoints or the appropriate workflow owner. The checkpoints remain the approval and resolution mechanism; this methodology provides the structured evaluation that feeds them.

**Documents this methodology references:**
- `quality-dimensions.md` — the 13 dimensions and their assessment contexts (B, P, C)
- `quality-issue-classification.md` — issue types, identification methods, resolution paths, and relevant checkpoints

---

## Step 1: Establish evaluation scope

Before beginning the assessment, determine which reference materials and types of access are available. This shapes how each dimension is categorised in the scope record.

### Finding and scope categories

| Category | Meaning |
|---|---|
| **In scope — fully assessable** | All required contexts for the dimension or component are available |
| **In scope — partially assessable** | At least one required context is available, but not all |
| **Cannot be assessed** | The dimension or component is in scope, but the required evidence, reference material, access, or expertise is unavailable |
| **Out of scope** | The dimension or component is deliberately excluded from this evaluation, or is structurally not applicable to the content being evaluated (for example, collection-level components in a single-piece evaluation) |

The distinction between "Cannot be assessed" and "Out of scope" matters for the evaluation record. A "Cannot be assessed" finding is a known gap that may require follow-up. An "Out of scope" decision means the dimension was not part of the evaluation design; no finding or follow-up is expected.

### 1.1 Identify available contexts

Work through the following questions and record the answers before beginning.

| Available? | Context enabled | Dimensions affected |
|---|---|---|
| Content itself | Enables assessment of dimensions that do not depend on external reference materials | 6 (Structural clarity), 8 (Within-piece consistency), and qualitative aspects of 5 (Concision) |
| Brief or content specification | Enables assessment of B components that depend on defined requirements, scope, audience, or success criteria | B components of 1, 3, 4, 7, 9, 13; and reference-dependent aspects of 5 |
| Voice reference | Enables voice alignment assessment | 2 |
| Product access, authoritative documentation, or appropriate SME | Enables assessment of product-dependent accuracy, task completion, completeness, and terminology | 1P (product-verified accuracy), 4P (verified task completion), 7P (product-verified completeness), 11P (product-aligned terminology) |
| Expertise in the intended audience's actual context, tools, and capabilities | Enables task accessibility assessment | 3P (task accessibility) |
| Target-locale expertise: cultural conventions, regulatory requirements, locale-specific terminology | Enables locale appropriateness assessment | 9P (locale appropriateness) |
| Full content set (for a collection evaluation) | Enables C-context assessment | Collection-dependent components: 10, 11C, 12, 13C |

If a context is unavailable, dimensions or components that depend on it are recorded as "Cannot be assessed" — not as out of scope and not as a presumed pass or fail.

### 1.2 Determine how each dimension is categorised

Using the available contexts identified above and the summary reference table in `quality-dimensions.md`, categorise each dimension or component:

- **In scope — fully assessable:** all required contexts are available
- **In scope — partially assessable:** at least one required context is available; document which components can and cannot be assessed
- **Cannot be assessed:** the dimension is in scope but a required context, material, or access is unavailable — record what is missing
- **Out of scope:** the dimension is deliberately excluded, or is structurally not applicable to this evaluation

**For a single-piece evaluation:** collection-dependent components (10, 11C, 12, and 13C) are out of scope — they are not applicable to individual-piece assessment. Other components of dimensions 11 and 13 may still be assessable where their required contexts are available.

**For a single-piece evaluation with no brief and no product access:** structural clarity (6) and within-piece consistency (8) can be assessed directly from the content. Concision (5) may also be assessed qualitatively, although compliance with a specified target length or scope cannot be established without the relevant reference material. Other dimensions or components should be recorded as "Cannot be assessed" or "Out of scope", as applicable.

### 1.3 Record the scope

Before beginning the assessment, produce a scope record:

```
Evaluation scope
Evaluator: [name or role]
Evaluation date: [date]
Reference materials available: [list]
Product access available: [yes / no / partial — specify]
Collection review: [yes / no]

In scope — fully assessable: [list dimensions or components]
In scope — partially assessable: [list, with which components are assessable]
Cannot be assessed: [list, with reason for each]
Out of scope: [list, with reason for each]
```

This documentation ensures that any gap in coverage is attributed to evaluation conditions, not reviewer omission.

---

## Step 2: Assess brief-assessable dimensions

Assess B-context dimensions using the brief, supplied reference materials, and the content itself. Where a dimension also has a P or C component, assess only the B component in this step and note the remaining components as requiring a separate assessment.

**Recommended assessment order:**

1. **Within-piece consistency (8)** — assess from the content itself before applying external reference criteria; establishes the piece's internal coherence as a baseline
2. **Structural clarity (6)** — assess from the content itself
3. **Accuracy — brief consistency component (1B)** — verify each claim against the brief and grounding materials
4. **Voice alignment (2)** — verify against the voice reference in the brief
5. **Audience fit — specified-audience fit (3B)** — verify register, vocabulary, and assumed knowledge against the audience definition
6. **Task completion — structural task completion (4B)** — verify that the content addresses the intended task or information outcome as defined by the brief
7. **Concision (5)** — verify against target length and scope requirements
8. **Completeness — brief-defined completeness (7B)** — verify that everything the brief defines as in-scope is covered
9. **Localisation readiness — translation readiness (9B)** — if the content is intended for localisation; verify source-content properties against the brief and applicable localisation guidance
10. **Coverage coherence — scope-based coherence (13B)** — if a brief or content plan defines the scope across multiple pieces

For each dimension or component assessed in this step, record a finding using the format in Step 5.

---

## Step 3: Assess product- or expertise-dependent dimensions

Assess P-context dimensions using product access, authoritative documentation, or subject-matter expertise, as appropriate to each dimension.

| Dimension | Required access or expertise |
|---|---|
| Accuracy — product-verified accuracy (1P) | The actual product, its documentation, or an SME who can verify factual claims |
| Audience fit — task accessibility (3P) | Expertise in the audience's actual context, tools, and capabilities |
| Task completion — verified task completion (4P) | Access to the actual product |
| Completeness — product-verified completeness (7P) | Access to the actual product |
| Localisation readiness — locale appropriateness (9P) | Target-locale expertise: cultural conventions, regulatory requirements, locale-specific terminology |
| Terminology uniformity — product-aligned uniformity (11P) | The actual product interface |

Where product access or expertise is not available at the time of evaluation, record the finding as "Cannot be assessed" and note it as a known gap requiring follow-up at the appropriate checkpoint. This is a documented limitation of the evaluation, not a pass.

---

## Step 4: Assess collection-level dimensions

Collection-level dimensions are assessed after completing individual-piece assessments. They require the full content set and cannot be assessed from any single piece alone.

| Dimension | What is needed |
|---|---|
| Cross-content voice consistency (10) | The full content set + voice standard |
| Terminology uniformity — cross-content uniformity (11C) | The full content set |
| Format coherence (12) | The full set of comparable content + applicable format standards |
| Coverage coherence — collection-level coherence (13C) | The full content set |

If evaluating a single piece, collection-dependent components (10, 11C, 12, 13C) are out of scope. Skip this step and document those components accordingly.

---

## Step 5: Record findings

Use a consistent finding format for each assessed dimension or component. Findings should be specific enough for a reviewer encountering them later to understand what was assessed, what was found, and what action is required.

### Finding format

```
Dimension: [name and number]
Component: [if multi-component, e.g., "Brief consistency (B)" or "Product-verified accuracy (P)"]
Context used: [B / P / C]
Finding: [Pass / Issue identified / Cannot be assessed / Partial assessment]
Evidence: [specific observation, with reference to content section or element where relevant]
         For Pass and Issue identified: required — record the specific basis for the finding
         For Cannot be assessed: record what was needed and why it was unavailable
Next step: [if Issue identified — what action is needed, by whom, and at which checkpoint]
           [if Partial assessment or Cannot be assessed — what is needed to complete the assessment, and at which checkpoint]
```

### Finding types

**Pass** — the dimension's criteria are met for the available context. Record the specific evidence establishing this.

**Issue identified** — a quality problem was found. Record the specific evidence and the recommended next step. For guidance on issue types and resolution paths, see `quality-issue-classification.md`.

**Cannot be assessed** — the required reference material, access, or expertise was not available. Record what was needed and why the assessment could not be completed. This is a valid evaluation output — it makes the gap explicit.

**Partial assessment** — a multi-context dimension was assessed for one context only. Record what was established and what remains unassessed. Example:

```
Dimension: Accuracy (1)
Component: Brief consistency (B)
Context used: B
Finding: Partial assessment — B component assessed; P component requires product access
Evidence: All claims verified as consistent with supplied grounding materials.
          No claims identified that extend beyond the brief's established scope.
Next step: Product-verified accuracy assessment required at Quality checkpoint.
           Reviewer will need: product interface access or SME with knowledge of [specific feature area].
```

---

## Step 6: Route findings to Phase 5 checkpoints

Quality findings identified in this evaluation route to the existing Phase 5 checkpoints for resolution. The evaluation provides structured documentation; the checkpoints are where revision, verification, and approval decisions are made.

### Routing table

| Finding category | Relevant checkpoint |
|---|---|
| Brief- and reference-assessable content issues: accuracy against supplied grounding (1B), audience fit (3B), voice alignment (2), task completion against the brief (4B), concision (5), structural clarity (6), completeness against the brief (7B), within-piece consistency (8), and scope-based coverage coherence (13B) | Quality |
| Product-dependent content issues: product-verified accuracy (1P), verified task completion (4P), product-verified completeness (7P), and product-aligned terminology (11P) | Quality — reviewer requires product access, authoritative documentation, or appropriate SME expertise for 1P, 4P and 7P; 11P requires access to the actual product interface. |
| Task accessibility (3P) | Quality — reviewer requires expertise in the intended audience's actual context, tools, and capabilities |
| Source-content localisation readiness (9B) | Quality |
| Locale appropriateness (9P) | Localisation |
| Collection-level issues: cross-content voice consistency (10), cross-content terminology uniformity (11C), format coherence (12), and collection-level coverage coherence (13C). The product-aligned terminology component (11P) requires product access and routes with the product-dependent issues row above. | Quality — requires collection-level review |

### Intermediate AI output in an active workflow

The routing table above applies to content being evaluated at or approaching the Quality checkpoint. If the evaluation identifies a direction or brief-alignment problem in intermediate AI output — content that has not yet advanced to Quality — the finding may instead belong at the **Alignment** checkpoint, which handles whether intermediate output follows the intended direction before it advances. When routing such a finding, note the content's current workflow stage.

### When a finding spans checkpoints

Some dimensions have components that belong to different checkpoints. Localisation readiness, for example, has a source-content B component (Quality checkpoint) and a locale appropriateness P component (Localisation checkpoint). Document each component finding separately and route each to its relevant checkpoint.

### When the relevant checkpoint has already passed

If the content has already cleared a checkpoint and a new finding relates to that checkpoint's scope, flag the finding to the workflow owner as a potential exception rather than treating it as a routine checkpoint item.

---

## Step 7: Produce the evaluation record

At the end of the evaluation, compile a record that includes:

**1. Scope summary** — the evaluator, evaluation date, what was assessed, what was not, and why (referencing the scope record from Step 1)

**2. Findings summary** — a count of individual findings by type (Pass / Issue identified / Cannot be assessed / Partial assessment). Where a dimension has multiple components assessed separately, each component finding is counted independently.

**3. Issues for action** — each identified issue with:
- The dimension and component
- The specific finding and evidence
- The recommended next step
- The relevant checkpoint

**4. Deferred assessments** — findings recorded as "Cannot be assessed" or "Partial assessment", with what is needed to complete them and at which checkpoint that follow-up belongs

### Evaluation completeness

An evaluation is **complete** when every in-scope dimension or component has a recorded finding — Pass, Issue identified, Cannot be assessed, or Partial assessment.

An evaluation is **partial** when at least one in-scope dimension or component has not been assessed without a recorded reason. A partial evaluation that documents its own gaps is preferable to one that leaves gaps implicit.

---

## Reference: Applying this methodology in different situations

| Situation | Steps to apply | Notes |
|---|---|---|
| Quality checkpoint review for content in active workflow | Steps 1–6 | Focus on B-context dimensions; document P-context gaps as "Cannot be assessed" for follow-up at Quality checkpoint |
| Standalone review of existing content (no active workflow) | Full methodology | Available materials determine which dimensions are assessable; route findings to the appropriate process for revision or approval |
| Content collection audit | Full methodology | Complete individual-piece assessments (Steps 2–3) before collection-level assessment (Step 4); `content-audit-framework.md` provides additional guidance for large collections |
| Scoping what a reviewer needs before a checkpoint | Step 1 only | Produces a list of required access, materials, and expertise for a checkpoint to function reliably |
