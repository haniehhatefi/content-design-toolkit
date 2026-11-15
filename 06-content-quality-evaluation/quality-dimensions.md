# Quality Dimensions

**Phase 7: Content Quality Evaluation**

---

## Overview

This document defines the quality dimensions used in Phase 7's evaluation framework. Five established content-quality dimensions — accuracy, voice alignment, audience fit, task completion, and concision — are incorporated here with extended guidance on what is needed to assess each one fully. These dimensions are referenced in the Phase 6 experiments and are distinct from the Phase 4 output evaluation rubric, which uses a different dimension set designed specifically for evaluating AI-assisted outputs against supplied guidance. Additional dimensions cover quality criteria not addressed by brief-based compliance review alone: structural clarity, within-piece consistency, completeness, localisation readiness, and collection-level quality.

**Relationship to Phase 4:** The Phase 4 output evaluation rubric uses its own dimension set for evaluating AI-assisted outputs against supplied guidance at an in-workflow checkpoint. This framework is designed for a broader range of evaluation contexts: individual pieces assessed with or without a complete brief, existing content assessed outside the creation workflow, and content collections assessed for cross-piece quality. The Phase 3 rubric and this framework serve different purposes and can be used at different stages of the content lifecycle; neither replaces the other.

---

## Assessment contexts

Each dimension is mapped to one or more assessment contexts, indicating what is needed for a reliable evaluation.

| Context | Label | What it means |
|---|---|---|
| Brief-assessable | **B** | Does not require product access. Evidence may come from the brief and supplied reference materials, from the content itself, or from both. Where a dimension depends on a brief or specific reference material — voice alignment requires a voice reference, for example — it cannot be assessed if that material is absent. |
| Product- or expertise-dependent | **P** | Requires access to the actual product interface, authoritative documentation, or relevant subject-matter expertise. The nature of the expertise depends on the dimension. |
| Collection-dependent | **C** | Requires reviewing content in relation to other pieces in a set, product area, or content family. Not applicable to standalone single-piece evaluation. |

A dimension may belong to more than one context. Where a brief enables a partial assessment — for example, verifying that terminology matches the brief while noting that product-verified accuracy requires further review — both what was established and what remains unassessed are documented separately.

---

## Quality dimensions

### Established content-quality dimensions

The following five dimensions are referenced in the Phase 6 experiments and established through the toolkit's evaluation work. Phase 7 provides extended guidance on their assessment contexts and what constitutes a complete versus partial assessment.

---

#### 1. Accuracy
*Assessment contexts: B + P*

Accuracy has two components that require different assessment contexts and produce distinct findings.

| Component | Context | What is needed | Finding |
|---|---|---|---|
| Brief consistency | B | The brief and grounding materials | Whether each claim is consistent with what the brief and supplied materials establish |
| Product-verified accuracy | P | The actual product, its documentation, or a subject-matter expert | Whether each claim correctly describes actual product behaviour |

These are distinct assessments. A claim that is consistent with the brief is not independently verified as accurate: the brief may omit claims, state them incompletely, or in some cases contain errors itself. Where the brief does not establish a claim, the finding is "Cannot be assessed from the brief" — not "Brief-consistent."

*Phase 6 connection:* Experiment 05 established this distinction as its central finding. Brief-based compliance review sets the ceiling for brief-based accuracy assessment; product verification is a separate step that the brief cannot substitute for.

---

#### 2. Voice alignment
*Assessment context: B*

Whether the output's sentence structure, register, tone, and stylistic choices match the voice reference in the brief.

If no voice reference is supplied, voice alignment cannot be assessed. The finding is "Cannot be assessed" — not "Meets" or "Does not meet." Voice alignment is fully assessable from the brief alone; it does not require product access.

---

#### 3. Audience fit
*Assessment contexts: B + P*

| Component | Context | What is needed | Finding |
|---|---|---|---|
| Specified-audience fit | B | The audience definition in the brief | Whether register, vocabulary, format, and assumed knowledge are appropriate for the described audience |
| Task accessibility | P | Knowledge of the audience's actual context, tools, and capabilities | Whether users in that audience can complete the actions the content asks of them |

Specified-audience fit is assessable from the brief. Task accessibility requires expertise in the audience's actual context. A linguistically accessible output — meeting specified plain language criteria — does not automatically produce accessible actions: the content may assume tools, workflows, or capabilities not established by the brief or available to the intended audience.

*Phase 6 connection:* Experiment 03 illustrated this distinction through a constructed output that satisfied specified language requirements while including a workaround instruction that assumed tool access the scenario did not establish.

---

#### 4. Task completion
*Assessment contexts: B + P*

| Component | Context | What is needed | Finding |
|---|---|---|---|
| Structural task completion | B | The brief's scope definition and success criteria | Whether the content addresses the intended task or information outcome defined in the brief, including any required components or sequence |
| Verified task completion | P | Access to the actual product | Whether the content enables the intended user to achieve that outcome in the actual product or context |

A reviewer with a complete brief can assess whether the content addresses the intended task or information outcome as the brief defines it. Whether users can achieve that outcome in the actual product or context requires product access or testing. These are distinct findings; confirming structural task completion does not establish verified task completion.

This dimension applies to any content type — not only procedural instructions. It applies equally to content that helps users understand a concept, make a decision, or locate information: the brief defines the intended outcome, and structural task completion assesses whether the content is organised to address it.

---

#### 5. Concision
*Assessment context: B*

Whether the output meets target length requirements and contains no redundant or out-of-scope material. Fully assessable from the brief. Some aspects of concision — identifying redundant phrases or repeated content — can be assessed from the content itself where a target length is not specified; in those cases, the finding should note the basis for the judgement.

---

### Additional dimensions for individual content pieces

The following dimensions extend the established set to cover quality criteria not addressed by brief-based compliance review alone.

---

#### 6. Structural clarity
*Assessment context: B*

Whether the output's information hierarchy is logical, its headings and labels are descriptive, and the content can be navigated without reading in full where the format supports scanning. For procedural content: whether the step sequence is unambiguous and the relationship between steps is clear.

Structural clarity can be assessed from the content itself; it does not depend on a brief or reference material.

---

#### 7. Completeness
*Assessment contexts: B + P*

| Component | Context | What is needed | Finding |
|---|---|---|---|
| Brief-defined completeness | B | The brief's scope definition | Whether the output covers everything the brief defines as in-scope; whether anything required by the brief is absent |
| Product-verified completeness | P | Access to the actual product | Whether the output includes all information a user actually needs to complete the task, including steps or caveats not specified in the brief |

A brief-complete output covers the scope the brief defines. It may still omit steps that are necessary in the actual product if those steps were not in the brief. Where product-verified completeness cannot be assessed, the finding should note which completeness claims were established from the brief and which remain unverified.

---

#### 8. Within-piece consistency
*Assessment context: B*

Whether terminology, formatting conventions, and structural patterns are applied consistently throughout a single content piece. This dimension covers internal consistency within one piece and can be assessed from the content itself; a brief is not required. Consistency across multiple pieces is addressed under collection-level dimensions.

Sub-dimensions:
- **Terminology consistency:** the same term is used for the same concept, UI element, or action throughout the piece
- **Format consistency:** heading levels, list styles, numbering conventions, and emphasis markers are applied consistently
- **Voice consistency:** register and tone remain stable throughout; shifts in register within a single piece are intentional and signalled

---

### Localisation dimension

---

#### 9. Localisation readiness
*Assessment contexts: B + P*

| Component | Context | What is needed | Finding |
|---|---|---|---|
| Translation readiness | B | The brief and applicable localisation guidance | Whether the source content avoids structures that create translation barriers: idioms, hardcoded UI strings, ambiguous pronoun references, or implicit cultural dependencies |
| Locale appropriateness | P | Target-locale expertise: cultural conventions, regulatory requirements, locale-specific terminology | Whether the content is appropriate for a specific target locale — not only structurally translatable but culturally suitable |

Translation readiness is a source-content property that can be assessed without target-locale expertise. Locale appropriateness is a target-locale property that requires knowledge of the specific locale the content is being localised for.

*Phase 6 connection:* Experiment 04 established this as the central distinction of localisation review — a source prepared for translation is not automatically appropriate for every target locale.

---

### Collection-level dimensions

The following dimensions apply when evaluating content in relation to other pieces. They are not assessable for a standalone single piece and require the full content set or a defined sample.

---

#### 10. Cross-content voice consistency
*Assessment context: C*

Whether voice characteristics are consistent across a set of related content pieces reviewed together against the voice standard.

A single piece may display individually voice-aligned characteristics while the collection as a whole remains inconsistent. This dimension is not assessable from any individual piece: the reviewer must have access to the full content set and the voice standard.

*Phase 6 connection:* Experiment 01 established cross-content voice consistency as a distinct oversight requirement — one not visible when reviewing any single piece in isolation.

---

#### 11. Terminology uniformity
*Assessment contexts: C + P*

| Component | Context | What is needed | Finding |
|---|---|---|---|
| Cross-content uniformity | C | The full content set | Whether the same terms are used consistently across related pieces for the same concepts, UI elements, and actions |
| Product-aligned uniformity | P | The actual product interface | Whether terminology across the content set matches actual product labels consistently |

---

#### 12. Format coherence
*Assessment context: C*

Whether structure, layout, and format conventions are applied consistently across comparable content types within a collection — for example, whether all help articles of the same type follow the same structural pattern. What is needed: the full set of comparable content and any applicable format standards.

---

#### 13. Coverage coherence
*Assessment contexts: C + B*

| Component | Context | What is needed | Finding |
|---|---|---|---|
| Scope-based coherence | B | The brief or content plan defining the intended scope | Whether individual pieces cover their defined scope without significant overlap or gaps relative to the brief |
| Collection-level coherence | C | The full content set | Whether the collection as a whole covers its area without material gaps or duplications when reviewed together |

---

## Summary reference table

| # | Dimension | Context(s) |
|---|---|---|
| 1 | Accuracy | B + P |
| 2 | Voice alignment | B |
| 3 | Audience fit | B + P |
| 4 | Task completion | B + P |
| 5 | Concision | B |
| 6 | Structural clarity | B |
| 7 | Completeness | B + P |
| 8 | Within-piece consistency | B |
| 9 | Localisation readiness | B + P |
| 10 | Cross-content voice consistency | C |
| 11 | Terminology uniformity | C + P |
| 12 | Format coherence | C |
| 13 | Coverage coherence | C + B |

Dimensions 10–13 are collection-dependent and cannot be assessed for a standalone single piece.

---

## Notes on applying this framework

**When a brief is minimal or absent:** Brief-assessable dimensions vary in what they require. Some depend on a brief or supplied reference materials — voice alignment requires a voice reference; specified-audience fit requires an audience definition — and cannot be assessed when those materials are absent. Others — structural clarity, within-piece consistency — can be evaluated from the content itself regardless of brief availability. Where a dimension depends on specific reference materials, the finding is "Cannot be assessed" for that dimension — not a presumed pass or fail.

**When an assessment is partial:** Where a dimension spans multiple contexts and only one context is available, document what was assessed and what remains. For example: "Voice alignment assessed against brief. Terminology consistent with brief; not verified against product interface."

**Applying dimensions to collections:** Dimensions 10–13 require the full content set. For efficiency, complete brief-assessable and product-dependent assessments for each piece first, then apply collection-dependent dimensions across the set.

**Relationship to Phase 4's output evaluation rubric:** The Phase 4 rubric uses its own dimension set for evaluating AI-assisted outputs at an in-workflow checkpoint. This framework uses a different set of dimensions suited to a broader range of evaluation contexts: content assessed outside the creation workflow, existing content, and content collections. The two frameworks serve different purposes and can be used at different stages of the content lifecycle.
