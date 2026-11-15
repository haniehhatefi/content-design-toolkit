# Quality Issue Classification

**Phase 7: Content Quality Evaluation**

---

## Overview

This document is a reference taxonomy of quality issue types. It is used alongside `evaluation-methodology.md` when recording "Issue identified" findings, and alongside `content-audit-framework.md` when synthesising audit findings and planning remediation.

For each issue type, the taxonomy provides:

- **Identification signal** — what a reviewer observes when this issue is present
- **Evidence needed** — what is required to confirm the issue and document it reliably
- **Resolution path** — what action resolves the issue, and who is responsible
- **Checkpoint** — which Phase 5 checkpoint the finding routes to

**How to use this document:** when a finding is recorded as "Issue identified," locate the dimension the finding relates to, identify the issue type, and use the resolution path and checkpoint to complete the finding's "Next step" field in the evaluation record (following the finding format in `evaluation-methodology.md` Step 5). If the required evidence is not available, the finding should remain as "Cannot be assessed" or "Partial assessment" until it can be confirmed.

**Distribution and nature:** the distribution (systemic / localised) and nature (structural) classifications described in `content-audit-framework.md` apply per finding, not per issue type. Any issue type can appear in one piece or across many. Where an issue type commonly indicates a structural cause — a gap in the voice standard, an absent product terminology decision, a missing format standard — the resolution path notes this.

**Documents this taxonomy references:**
- `quality-dimensions.md` — the 13 dimensions, their assessment contexts, and their sub-components
- `evaluation-methodology.md` — the step-by-step assessment process, finding format, and checkpoint routing table

---

## Established content-quality dimensions

### 1. Accuracy

Accuracy has two components that require different assessment contexts and produce distinct findings. A finding may contain both issue types if the brief and the product diverge: a claim may be brief-consistent but product-inaccurate (see `quality-dimensions.md` for the established distinction).

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Brief inconsistency** | A claim, described behaviour, or scope statement in the content contradicts the supplied brief and grounding materials, or explicitly exceeds the scope they define | Brief and grounding materials; the specific content passage; the specific contradiction or scope excess identified | Revise to align with the brief and grounding. If the brief is ambiguous or incomplete, note the ambiguity in the finding; the brief clarification should be resolved before the content revision proceeds. | Quality |
| **Product inaccuracy** | A claim, instruction, or described behaviour does not match actual product behaviour | Product interface access, authoritative product documentation, or an SME with direct knowledge of the relevant feature area; the specific inaccurate claim; the correct product behaviour | Revise to reflect current product behaviour. If the inaccuracy reflects a recent product change, flag for product team awareness alongside the content revision. | Quality — reviewer requires product access, authoritative documentation, or appropriate SME expertise |

A claim that is not established or addressed by the brief — but does not contradict it — should be recorded as "Cannot be assessed from the brief," not as a brief inconsistency. The absence of supporting evidence in the brief is not itself evidence of inconsistency.

---

### 2. Voice alignment

If no voice reference is supplied, voice alignment cannot be assessed. Record the finding as "Cannot be assessed" and note that a voice reference is required.

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Register mismatch** | The content's overall register — formal, conversational, plain-language, or technical — does not match the register specified in the voice reference | Voice reference; specific passages where the register diverges | Revise to match the specified register throughout. | Quality |
| **Stylistic divergence** | Sentence structure, phrasing patterns, or use of active/passive voice diverge from the patterns the voice reference establishes | Voice reference; specific passages with divergent phrasing or structure | Revise sentence construction and phrasing to align with the voice reference. | Quality |

---

### 3. Audience fit

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Vocabulary or assumed-knowledge mismatch** | The content assumes a level of familiarity — specialist vocabulary, prior knowledge, conceptual background — that does not match the audience definition in the brief | Brief's audience definition; specific passages where vocabulary level or assumed knowledge diverges | Revise to match the vocabulary level and assumed knowledge defined in the brief. | Quality |
| **Task inaccessibility** | The content asks users to complete actions that are not achievable given the audience's actual tools, permissions, or capabilities in their real context | Expertise in the audience's actual context, tools, and capabilities; the specific instructions that assume unavailable access; evidence of the gap between instruction and actual capability | Revise the instructions or surface the prerequisite access and capability requirements explicitly. If the gap cannot be resolved in the content alone, flag for product or workflow owners. | Quality — reviewer requires expertise in the intended audience's actual context, tools, and capabilities |

---

### 4. Task completion

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Incomplete scope coverage** | The content does not address a component, sequence, or outcome that the brief defines as required — it ends before the task is fully covered or omits a required section | Brief's scope definition and success criteria; identification of the specific missing component or outcome | Revise to include the missing component or sequence. If the scope definition in the brief is unclear, note the ambiguity and flag for clarification before revision. | Quality |
| **Task not achievable in product** | Following the content's instructions does not enable the user to complete the intended outcome in the actual product or context | Product interface access; the specific step or sequence that fails; the gap between the content's instruction and the actual product flow | Revise instructions to reflect the actual product flow. If the product flow is itself undocumented or unclear, flag for product team input before revision. | Quality — reviewer requires product access |

---

### 5. Concision

Where the brief specifies a target length, it defines the ceiling for length assessment. Where no target length is specified, the finding should note the basis for the judgement — typically, that the content states the same point more than once, or covers ground outside the evident scope of the piece.

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Scope excess** | The content includes material that falls outside the scope defined in the brief — additional topics, context, or caveats not required by the brief | Brief's scope definition; the specific out-of-scope passages | Remove out-of-scope material. If the brief is ambiguous about what should be included, flag for scope clarification. | Quality |
| **Redundancy** | The same information is stated more than once within the piece without a structural rationale (such as a deliberate summary or recap) | Content itself; the specific passages that restate the same information | Consolidate or remove repeated content. | Quality |

---

## Additional dimensions for individual content pieces

### 6. Structural clarity

Structural clarity issues can be identified from the content itself; a brief is not required.

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Unclear information hierarchy** | Headings, subheadings, or labels do not reflect the content's logical structure; a reader scanning for a section cannot reliably predict what it contains from the heading or label text | Content itself; the specific structural elements where hierarchy is unclear or misleading | Revise heading and label text to describe the content they introduce accurately. Restructure sections where the written order does not match the logical order. | Quality |
| **Ambiguous step sequence** | In procedural content: steps are not in the order required to achieve the outcome, the relationship between steps is unclear, or a step depends on an action not stated in the content | Content itself; the specific step or steps where ambiguity or misordering occurs | Reorder steps or add transitional language to clarify sequence and dependencies. | Quality |

---

### 7. Completeness

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Brief-defined omission** | Something the brief defines as in-scope — a required section, a specified component, a mandatory caveat — is absent from the content | Brief's scope definition; identification of the specific missing element | Add the missing element. If the brief is ambiguous about what is required, note the ambiguity and flag for clarification before revision. | Quality |
| **Product-required omission** | A step, caveat, or piece of information that the user genuinely needs to complete the task in the actual product is absent — not because the brief didn't specify it, but because it is necessary in practice | Product interface access; the specific step or information that is missing; the consequence of its absence for the user | Add the missing information. If the product requires steps that the brief does not cover, flag for brief or scope update alongside the content revision. | Quality — reviewer requires product access |

---

### 8. Within-piece consistency

Within-piece consistency issues can be identified from the content itself; a brief is not required.

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Terminology inconsistency** | Different terms are used for the same concept, UI element, or action within a single piece | Content itself; the specific terms and the passages where each appears | Standardise on a single term throughout the piece. If the choice of term also involves cross-content consistency, note the connection to dimension 11. | Quality |
| **Format inconsistency** | Heading levels, list styles, numbering conventions, or emphasis markers are applied inconsistently within the piece | Content itself; specific instances where conventions differ | Apply a consistent convention throughout the piece. If the inconsistency reflects uncertainty in the format standard, flag for format guidance clarification. | Quality |
| **Register or voice shift** | The register or tone changes within the piece in a way that is not intentional or signalled | Content itself; the specific passages where the shift occurs | Revise to maintain a consistent register and tone. If the shift is intentional, assess whether it is appropriately signalled in the content. | Quality |

---

## Localisation dimension

### 9. Localisation readiness

Localisation readiness has two components that require different evidence and route to different checkpoints.

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Translation barrier** | The source content contains structures that create translation problems: idiomatic expressions, hardcoded UI strings, ambiguous pronoun references, or implicit cultural dependencies | Brief and applicable localisation guidance; the specific passages or elements that create barriers | Revise source content to remove the barrier: replace idioms with literal equivalents, externalise hardcoded strings, resolve ambiguous references, or make cultural dependencies explicit. | Quality |
| **Locale inappropriateness** | The content is not suitable for a specific target locale: it assumes cultural conventions, references regulatory contexts, or uses terminology that is inappropriate or incorrect for that locale | Target-locale expertise: knowledge of the locale's cultural conventions, regulatory requirements, and locale-specific terminology; the specific elements that are inappropriate and the reason | Revise for the target locale. Resolution typically requires a locale-specific SME. If the issue reflects a gap in localisation guidance, flag for guidance update alongside the content revision. | Localisation |

---

## Collection-level dimensions

### 10. Cross-content voice consistency

Voice inconsistency is not visible from any single piece; it is identified by reviewing the full content set against the voice standard.

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Voice inconsistency across set** | Individual pieces reviewed together reveal inconsistent register, tone, or stylistic choices that are not visible when reviewing any single piece in isolation | Full content set and voice standard; the specific pieces or passages where inconsistency is visible when reviewed together | Revise pieces that diverge from the voice standard. Where the inconsistency is widespread and indicates insufficient application of the standard, the resolution path extends beyond content revision: flag for voice standard clarification or reviewer guidance. | Quality — requires collection-level review |

A systemic voice inconsistency across a large set often indicates a structural cause. The resolution may need to address the upstream input — the voice standard or its application — not only the individual content pieces.

---

### 11. Terminology uniformity

Terminology uniformity has two components that require different evidence.

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Cross-content terminology inconsistency** | Different terms are used for the same concept, UI element, or action across related pieces when reviewed together | Full content set; the specific terms and the pieces where each appears | Standardise on a single term across the set. If the choice of term has not been established at the product level, flag for a product terminology decision before revising. This issue is structural when the underlying cause is an absent or undocumented terminology decision; the resolution path extends to that decision, not only to content revision. | Quality — requires collection-level review |
| **Product-misaligned terminology** | Terms used across the content set do not match the product interface labels consistently | Product interface; the specific discrepancies between content terminology and product labels | Revise to align with current product interface labels. If product labels have changed since the content was written, flag for content update tracking. | Quality — reviewer requires product access |

---

### 12. Format coherence

Format coherence issues are visible only when comparable content types are reviewed together.

| Issue type | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|
| **Structural inconsistency across comparable content types** | Content pieces of the same type — help articles, tooltips, error messages — do not follow the same structural pattern when reviewed together | Full set of comparable content; applicable format standards; the specific structural differences across comparable pieces | Revise outlying pieces to conform to the established structural pattern. If no format standard exists for the content type, the finding indicates a need to establish one: flag for format standard development. This issue is structural when the underlying cause is an absent format standard; the resolution path extends to that standard, not only to content revision. | Quality — requires collection-level review |

---

### 13. Coverage coherence

Coverage coherence has a brief-assessable component and a collection-dependent component; they address different levels of scope and are assessed separately.

- **13B — Scope-based coherence:** whether an individual piece covers the scope its brief or content plan defines. Assessable with a brief; does not require the full collection.
- **13C — Collection-level coherence:** whether the collection as a whole covers its area without material gaps or duplications. Requires the full content set.

Collection-level findings (13C) should be treated as qualitative indications rather than definitive conclusions when based on a sample rather than the full collection.

| Issue type | Component | Identification signal | Evidence needed | Resolution path | Checkpoint |
|---|---|---|---|---|---|
| **Scope-defined omission** | 13B | An individual piece does not cover a topic, task, or component that its defined scope or brief requires | Brief or content plan defining the piece's scope; identification of the specific missing element | Revise the piece to include the missing element. If the brief is ambiguous about what is required, note the ambiguity and flag for clarification before revision. | Quality |
| **Coverage gap** | 13C | Expected content is absent from the collection: a topic, task, or scenario that falls within the collection's defined scope is not addressed by any piece | Full content set; brief or content plan defining the collection's scope; identification of the specific absent topic or task | Create new content to fill the gap, or revise an existing piece's scope to cover it. If the scope definition does not establish whether the gap is in scope, flag for clarification before creating or revising. | Quality — requires collection-level review |
| **Coverage overlap** | 13C | The same topic, task, or scenario is covered by more than one piece without a structural rationale (such as an intentional overview-and-detail structure) | Full content set; the specific pieces that cover overlapping ground; the extent and nature of the overlap | Consolidate overlapping pieces, or define distinct scope boundaries for each. If the overlap is extensive, the resolution may require restructuring the content area. | Quality — requires collection-level review |
