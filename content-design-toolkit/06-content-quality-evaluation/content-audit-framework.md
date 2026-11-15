# Content Audit Framework

**Phase 7: Content Quality Evaluation**

---

## Overview

This framework provides guidance for applying Phase 7's quality criteria to existing content collections. It covers defining an audit's scope and objectives, selecting content for assessment, conducting piece-level and collection-level evaluation, synthesising findings across a collection, and prioritising remediation.

An audit differs from an in-workflow evaluation in two important ways:

1. **The content already exists and is not in an active creation workflow.** Phase 5 checkpoints govern content in production; they are not the mechanism for resolving findings from a retrospective audit. Audit findings go to whoever owns revision decisions for the content being assessed.

2. **The scope is typically larger.** An audit may cover dozens or hundreds of pieces, requiring decisions about content selection and sampling that individual-piece evaluations do not.

This framework extends `evaluation-methodology.md`, which defines the step-by-step process for assessing individual pieces and components. For the actual assessment process — scope categories, finding format, finding types — refer to that document. This framework addresses the additional decisions specific to auditing a content collection.

**Documents this framework references:**
- `quality-dimensions.md` — the 13 dimensions and their assessment contexts
- `evaluation-methodology.md` — the step-by-step assessment process for individual pieces
- `quality-issue-classification.md` — issue types, resolution paths, and relevant checkpoints

---

## 1. Define the audit scope and objectives

Before selecting content or beginning assessment, establish what the audit is trying to answer. Audit objectives shape which dimensions to assess, which evidence is needed, and what level of sampling is appropriate.

### Common audit objectives

| Objective | Primary dimensions | Required context |
|---|---|---|
| Check whether existing content is consistent with the current voice standard | 2, 10 | B + C |
| Verify terminology is consistent and product-aligned | 11 | C + P |
| Assess structural clarity and internal consistency across a content area | 6, 8 | Content itself |
| Confirm factual accuracy against the current product | 1P | P |
| Identify coverage gaps or overlaps in a content area | 13 | B + C |
| Assess readiness of source content for a localisation project | 9B | B |
| Full quality review of a content area | All applicable dimensions | B + P + C |

An audit does not need to cover all 13 dimensions. Defining the objective first avoids collecting more information than the audit's purpose requires.

### Establish available contexts

For an audit of existing content, the available contexts often differ from those available during content creation:

**When original briefs are unavailable:** Assess each B component against the reference materials actually available. Voice alignment (2) may still be assessed if a voice standard exists independently; audience fit (3B) may be assessed if an authoritative audience definition is available; localisation readiness (9B) may be assessable using current localisation guidance. Components that depend on unavailable original requirements — brief consistency (1B), structural task completion (4B), and brief-defined completeness (7B) — cannot be assessed against the original brief. If a current content specification can be reconstructed from authoritative sources, document it separately as a reconstructed reference. Findings against it should not be presented as evidence of compliance with the original brief. Document absent briefs and any reconstructed references in the scope record.

**When product behaviour has changed:** product-verified accuracy (1P) reflects the product at the time of audit. If the content is known to have been accurate when it was written, note this context in the finding; the finding still identifies the gap between current content and current product.

**For collection-level assessment:** collection-dependent components (10, 11C, 12, 13C) require the full set of content being audited, or a sample large enough to draw collection-level conclusions.

Document available contexts as part of the scope record, following the format in `evaluation-methodology.md` Step 1.3, extended with the audit's objectives and content selection criteria.

---

## 2. Select content

### Full collection vs. sample

| Situation | Approach |
|---|---|
| Small collection (under approximately 20 pieces) | Assess the full collection |
| Specific compliance or regulatory requirement | Assess the full collection or the full relevant subset |
| Known issue in one content area | Assess the full area |
| Content in scope for an upcoming localisation project | Assess all pieces in localisation scope |
| Large collection; objective is to identify systemic patterns | Stratified sample — see below |

### Stratified sampling

When assessing the full collection is not practical, select a sample that represents the range of content rather than a convenience sample.

**Criteria to consider when selecting a sample:**

| Criterion | Purpose |
|---|---|
| Content type | Ensure each type in the collection is represented (help articles, tooltips, error messages, onboarding content, notifications, etc.) |
| Product area | Include content from different product areas; prioritise areas that have changed recently |
| Content age | Include both recently created and older content; older content is more likely to reflect earlier product states or voice standards |
| Reported issues | Include content flagged through support, user research, or internal review |
| Traffic and consequence | Prioritise content users encounter frequently or that covers high-consequence actions |

**On sample size:** there is no universal minimum sample size. Select enough pieces to identify recurring patterns across the relevant content types or product areas; the sample should be appropriate to the audit objective and its diversity. The 20-piece figure in the table above is a working guideline, not a fixed threshold — collection complexity and assessment effort also affect what is practical. Unless the sampling design supports statistical generalisation, findings should be treated as qualitative indications of patterns rather than estimates of their prevalence across the full collection.

**Document selection criteria** in the scope record. This makes the audit's coverage and limitations transparent and allows future audits to use comparable criteria.

---

## 3. Conduct piece-level assessment

For each piece in the audit scope, follow the evaluation process in `evaluation-methodology.md` Steps 1–3:

- Identify available contexts
- Assess brief-assessable dimensions (Step 2)
- Assess product-dependent dimensions (Step 3)
- Record findings using the format in Step 5

### Adaptations for the audit context

**When original briefs are unavailable:** record B components that require a brief as "Cannot be assessed — original brief not available." If a current content specification can be reconstructed from the content, product documentation, or other sources, document it as a reconstructed reference. Assess against it separately from the original brief, and do not present the findings as evidence of compliance with the original brief.

**When product behaviour has changed:** record findings against the current product state and note whether the content is known to have been accurate at the time of creation.

**At scale:** for large audits, assess a consistent set of dimensions across all pieces before moving to the next set — for example, assessing all pieces for structural clarity and within-piece consistency before beginning voice alignment review. This makes cross-piece patterns visible during assessment rather than only after all pieces are complete.

---

## 4. Conduct collection-level assessment

After completing piece-level assessment, apply the collection-dependent dimensions (10, 11C, 12, 13C) across the full set of assessed pieces.

| Dimension | What to look for |
|---|---|
| Cross-content voice consistency (10) | Whether voice characteristics are consistent across the set when reviewed together against the voice standard |
| Terminology uniformity — cross-content uniformity (11C) | Whether the same terms are used consistently across pieces for the same concepts, UI elements, and actions |
| Format coherence (12) | Whether structure and format conventions are consistent across comparable content types within the collection |
| Coverage coherence — collection-level coherence (13C) | Whether the collection covers its area without material gaps or duplications when reviewed as a whole |

Collection-level assessment reviews pieces as a unit rather than individually. Cross-reference findings from piece-level assessment — particularly terminology and voice findings — alongside the collection-level review.

**When the audit used a sample:** collection-level findings apply directly to the assessed sample. Any interpretation beyond the sample should be qualified by the selection criteria and coverage limitations. Do not assume that a pattern's frequency in the sample represents its frequency in the full collection.

---

## 5. Synthesise findings

After completing piece-level and collection-level assessment, synthesise individual findings into patterns before producing the audit output.

### Classify findings by scope

These classifications are not mutually exclusive. A finding may have both a distribution and a nature — for example, a missing terminology decision may be systemic (affects many pieces) and structural (the underlying problem is an absent product decision).

| Classification | Meaning |
|---|---|
| **Systemic** *(distribution)* | The issue appears across multiple pieces, content types, or product areas |
| **Localised** *(distribution)* | The issue appears in one piece or a small cluster of related pieces |
| **Structural** *(nature)* | The issue reflects an underlying content-design, planning, product, or guidance problem; may overlap with systemic or localised findings |

For each finding pattern, record:
- Which dimension or component is involved
- How many pieces are affected
- **Distribution:** whether the issue is systemic or localised
- **Nature:** whether the issue is structural, where applicable
- A hypothesis about root cause, where one is apparent from the evidence

### Cross-reference with quality-issue-classification.md

For each finding or finding pattern, refer to `quality-issue-classification.md` to identify the issue type, evidence needed to confirm it, and its resolution path. Where findings point to upstream causes — a gap in the voice standard, a missing terminology decision, an outdated or absent brief — the resolution path extends beyond individual content revision.

---

## 6. Prioritise remediation

Not all findings from an audit can be addressed at once. Prioritising ensures the most significant issues are resolved first.

### Prioritisation criteria

| Criterion | Description |
|---|---|
| **User impact** | Does the issue affect users' ability to complete tasks, understand the product, or trust the content? Accuracy failures and task-completion failures typically carry the highest impact. |
| **Frequency** | How many pieces are affected? Systemic issues affecting many pieces are generally higher priority than isolated issues. |
| **Severity** | Does the issue block task completion or produce incorrect behaviour, or does it degrade experience without blocking users? |
| **Dependencies** | Does resolving the issue require a decision or change outside the content team — a product terminology decision, a product change, a localisation review? Issues with external dependencies may need to be tracked and owned differently. |
| **Effort** | Is the fix a targeted revision, or does it require reworking a content area? Issues with high impact and low effort are strong candidates for immediate action. |

### Remediation list format

The remediation list produced by an audit should include, for each issue:
- Dimension and component
- Brief description of the finding
- Distribution (systemic / localised) and number of pieces affected
- Nature (structural, where applicable)
- Resolution path (from `quality-issue-classification.md`)
- Dependencies, if any
- Priority level
- Owner (content team, or external if the resolution requires a product or process decision)

The remediation list is not an approval gate. It is a structured record of what was found, in what order it should be addressed, and what is needed to address it.

---

## 7. Audit output

A complete audit produces four outputs:

**1. Scope record** — the audit objectives, available contexts, content selection criteria, and known limitations (following the format in `evaluation-methodology.md` Step 1.3, with selection criteria added)

**2. Individual findings** — a complete set of findings in the format defined in `evaluation-methodology.md` Step 5, covering all assessed pieces and components

**3. Findings synthesis** — a summary of patterns by dimension, distribution (systemic / localised), nature (structural, where applicable), and root-cause hypothesis

**4. Prioritised remediation list** — findings ranked for action, with resolution paths, dependencies, and ownership

### Relationship to Phase 5 checkpoints

Audit findings for existing content do not automatically enter the Phase 5 creation workflow. Phase 5 checkpoints govern content in active creation; they are not the mechanism for resolving retrospective audit findings.

If audit findings lead to content revisions, those revisions may re-enter the Phase 5 workflow at the appropriate stage — for example, substantive revisions to help articles may pass through the Quality checkpoint before publication. Whether and how revised content enters the creation workflow is a decision for the team managing the revision process.

Audit findings may also inform improvements to upstream workflow inputs. Gaps in the voice standard, missing terminology decisions, or incomplete localisation guidance identified through an audit are inputs to the toolkit's guidance documents — not only revision tasks for individual content pieces.
