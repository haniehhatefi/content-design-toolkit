# Phase 6: Findings and Recommendations

---

## 1. Overview

Phase 6 of the Content Design Toolkit comprises five practical experiments examining AI-assisted content creation across different content types, guidance conditions, and oversight requirements. Each experiment constructed two illustrative outputs under different specification conditions and evaluated what a human reviewer could establish about each output given the available context.

The experiments followed a consistent nine-section format — research question, hypothesis, test scenario, materials, procedure, observations, evaluation, limitations, and recommendations — and each was designed to introduce one analytical contribution: a distinction, observation, or oversight principle that extends the toolkit's practical framework.

The five experiments are:

| Experiment | Focus | Scenario | File |
|---|---|---|---|
| 01 | Voice consistency | Notification-preferences screen (page heading, helper text, toggle sub-label, confirmation toast, empty state) | `experiment-01-voice-consistency.md` |
| 02 | Grounding and specificity | Error message | `experiment-02-grounding-comparison.md` |
| 03 | Accessible language | Form upload instructions | `experiment-03-accessibility-and-inclusion.md` |
| 04 | Localisation readiness | Subscription renewal notification | `experiment-04-localisation-readiness.md` |
| 05 | Human-in-the-loop oversight | Help centre article | `experiment-05-human-in-the-loop.md` |

This document synthesises cross-cutting findings from all five experiments and derives practical recommendations for teams using the toolkit. It assumes familiarity with the toolkit's core frameworks — the five evaluation dimensions: three voice attributes and two cross-cutting writing standards (Phase 2), the three-tier guidance structure and output evaluation rubric (Phase 4), the five human oversight checkpoints (Phase 5), and the localisation workflow (Phase 5) — but can be read alongside those documents without prior knowledge of the individual experiments.

---

## 2. Cross-cutting findings

### 2.1 Guidance scope and review scope are interdependent

Across all five experiments, what a human reviewer could assess was shaped by what the workflow provided — to both the AI generating the content and the reviewer assessing it. This held whether the input was a voice standard (Experiment 01), product grounding materials (Experiment 02), accessible language guidance (Experiment 03), localisation guidance (Experiment 04), or a content brief (Experiment 05).

This is a workflow property, not a property of AI capability or reviewer expertise. A capable reviewer given only an AI-assisted output and a minimal brief can assess surface quality. The same reviewer given the output and a complete brief can assess compliance with stated requirements. Workflow inputs establish the context and requirements against which review can take place; reviewer capability determines how effectively those requirements are assessed. Better inputs expand the scope of review; they do not independently guarantee review quality.

The implication is directional: investment in upstream workflow inputs — complete briefs, grounding materials, explicit guidance — expands what can be assessed at each review stage. What those inputs establish about drafting requirements also defines the reference against which review takes place. Workflow inputs and review context are therefore worth planning together, as changes to one affect the other.

### 2.2 Well-specified conditions still contained deliberately constructed weaknesses or unresolved decisions

Each experiment included a deliberately constructed weakness, inconsistency, or unresolved decision in its more fully specified condition. These examples took different forms: cross-content voice inconsistency, an ungrounded suggestion, an unverified workaround, an unresolved localisation convention, and a factual claim outside the defined scope.

| Experiment | Constructed issue | Condition in which it was introduced |
|---|---|---|
| 01 | Voice inconsistency across the five-piece content set | Complete-guidance condition |
| 02 | Ungrounded suggestion not established by the supplied grounding materials | Grounded condition |
| 03 | Workaround instruction not covered by the accessibility guidance | Guidance condition |
| 04 | Salutation convention not addressed by the localisation guidance | Guidance condition |
| 05 | Factual claim about notification behaviour excluded by the brief | Complete-brief condition |

The experiments were deliberately designed to include examples of this type in the well-specified conditions, not only in the minimal-specification conditions. This design choice illustrates a practical consideration: a review check for unverified additions, inconsistencies, and unresolved decisions should be applied routinely at the appropriate checkpoint, regardless of guidance completeness. The constructed examples do not establish that all well-specified AI-assisted drafts will contain such issues; they demonstrate why the check remains necessary even when specification is thorough.

### 2.3 More complete specification changes the nature of oversight required

Across the constructed scenarios, more complete specification was associated with outputs that demonstrated different characteristics — more specific terminology, more appropriate register, more correctly scoped content — and a more defined basis for human review. These comparisons illustrate how specification changes the nature of oversight required, rather than establishing a measured improvement in AI-generated content:

- Grounding materials (Experiment 02) shifted oversight from authoring mode — adding missing specificity — to fact-checking mode — verifying specificity produced. The grounded output was richer but required verification against the product.
- Accessible language guidance (Experiment 03) improved linguistic form but did not eliminate the need for accessibility review. Well-specified language is not automatically task-accessible.
- Localisation guidance (Experiment 04) improved structural readiness for translation but did not establish locale appropriateness. A source prepared for translation is not automatically appropriate for every target locale.
- A complete brief (Experiment 05) enabled compliance review but surfaced the accuracy-verification gap: compliance with the brief does not confirm accuracy against the actual product.

Specification and oversight are complementary, not interchangeable. More complete specification produces better-defined review requirements; it does not eliminate them.

### 2.4 Reviewer context and reviewer capability are distinct dimensions of review quality

This distinction was directly examined in Experiment 05, which held reviewer capability constant and varied the completeness of the brief. The experiment demonstrated that a reviewer working from an incomplete brief can assess surface quality only — not because they lack expertise, but because the brief does not establish the requirements against which compliance would be assessed. The same reviewer, with the same expertise and a complete brief, can assess compliance with stated requirements and identify additions beyond those requirements.

The pattern was also present across the preceding experiments, where the reviewer's available context — voice standards, grounding materials, guidelines — shaped what could be assessed at each oversight stage. The broader synthesis is a conceptual implication of the series, rather than a directly tested result in each individual experiment.

**Reviewer context** is what the workflow provides — the brief, guidelines, grounding materials, and reference against which the output is assessed.

**Reviewer capability** is what the reviewer knows — their domain expertise, product knowledge, and familiarity with content criteria.

A highly capable reviewer working without a complete brief cannot assess dimensions the brief does not define. A complete brief reviewed by someone without the relevant domain expertise does not produce a complete review. Neither variable alone determines review quality; both must be present for a checkpoint to function reliably.

### 2.5 Some review requirements fall outside the toolkit's guidance scope by design

Experiments 02, 03, 04, and 05 each identified a review requirement that the toolkit can prepare content for but cannot itself satisfy:

- **Product accuracy verification** (Experiments 02 and 05) — requires access to the actual product interface or documentation, which the brief and grounding materials can reference but cannot replace
- **Task accessibility review** (Experiment 03) — accessible linguistic form does not guarantee that proposed actions are achievable for the intended audience; Experiment 03 illustrated this through a constructed output that satisfied specified language requirements while including a workaround instruction that assumed tool access the scenario did not establish; reviewing task accessibility requires assessing whether users can actually complete what the content asks of them, which may draw on domain knowledge or audience research that the accessible language guidance cannot supply
- **Locale appropriateness review** (Experiment 04) — requires target-locale knowledge and cultural familiarity that cannot be encoded in source-language guidance

The toolkit's scope is to prepare content for these reviews — through structured guidance, well-specified briefs, and appropriate grounding — not to eliminate the need for them. Teams should plan for the external expertise or access that each review stage requires, alongside the toolkit's structured workflow.

---

## 3. Experiment findings at a glance

| Experiment | Central finding | Concept introduced |
|---|---|---|
| 01: Voice Consistency | Individual content pieces in a set can each display some voice-aligned characteristics while the collection as a whole remains inconsistent; the constructed scenario demonstrates that cross-content consistency requires reviewing all pieces together, as no single output carries sufficient context to assess cross-document alignment | Cross-content review context as a distinct oversight requirement |
| 02: Grounding and Specificity | Grounding materials shift the nature of human oversight from authoring (supplying missing specificity) to fact-checking (verifying specificity produced); both modes require human judgment, but they require different reviewer access | Authoring mode vs. fact-checking mode |
| 03: Accessible Language | A constructed output can satisfy specified language requirements — shorter sentences, simpler vocabulary, reduced passive construction — while including an instruction that assumes capabilities not established by the content scenario; the distinction between linguistically accessible language and a fully accessible user action requires assessing whether users can actually complete what the content asks of them | Linguistic accessibility vs. task accessibility |
| 04: Localisation Readiness | Source-level guidance reduces structural barriers to translation but does not establish whether the content is appropriate for a specific target locale; these are distinct stages that require different expertise | Translation readiness vs. locale appropriateness |
| 05: Human-in-the-Loop Oversight | Brief completeness sets the ceiling of brief-based compliance review at the Quality checkpoint; a reviewer working from an incomplete brief can assess surface quality only — not because they lack expertise, but because the brief does not establish the requirements against which compliance would be assessed | Checkpoint scope vs. reviewer capability |

---

## 4. Recommendations

The following recommendations are derived from cross-cutting patterns across all five experiments. They extend the individual experiment recommendations to address findings that only become visible across the full Phase 6 series.

### 4.1 Coordinate upstream workflow inputs as a system

Complete briefs, grounding materials, voice standards, and localisation guidance each define drafting requirements and establish the context against which review takes place. These inputs shape what can be assessed at each review stage and are worth coordinating together: a well-specified brief without accessible language guidance leaves a gap in the review context; accessible language guidance without a complete brief creates a checkpoint that cannot assess compliance. Evaluate upstream workflow inputs as a system, not as independent documents.

### 4.2 Plan for domain-specific human oversight at each review stage

Each experiment identified a form of review expertise the toolkit can prepare content for but cannot substitute:

| Review type | Required reviewer access |
|---|---|
| Cross-content voice review | Familiarity with the full content set and the voice standard |
| Product accuracy verification | Access to the actual product and its specifications |
| Task accessibility review | Expertise in relevant accessibility criteria and audience context |
| Locale appropriateness review | Target-locale knowledge and cultural familiarity |
| Quality compliance review | Access to the complete content brief |

These are not interchangeable. Assigning a capable reviewer without the appropriate context, or providing appropriate context to a reviewer without the relevant expertise, produces a structurally incomplete checkpoint.

### 4.3 Include a check for additions beyond the brief as a standard Quality checkpoint step

Experiments 02, 03, and 05 included constructed examples of content that went beyond or was not established by the supplied grounding materials, guidance, or brief. Experiment 04 highlighted a different issue: an unresolved localisation decision that required target-locale knowledge. Together, these examples demonstrate why review must examine both the traceability of content claims and decisions that remain unspecified, even when guidance is thorough.

The Quality checkpoint should include an explicit step: for each factual claim and scope extension in the output, confirm it is traceable to the brief or grounding materials. Resolution depends on the nature of the addition:

- A claim within scope but not grounded in the brief can be grounded or verified against the product.
- A claim that falls within an explicitly excluded scope area must be removed, or the scope definition formally revised before the claim is retained.

At the Localisation checkpoint, unresolved locale-dependent conventions should also be identified and resolved through appropriate target-locale review before approval.

### 4.4 Distinguish brief compliance from factual accuracy at the Quality checkpoint

A complete brief enables compliance review. It does not establish factual accuracy against the actual product. These are distinct assessments that may require different reviewer access:

- **Brief compliance** — whether the output meets the requirements the brief specifies — can be assessed by a reviewer with the brief and the output.
- **Product accuracy** — whether claims in the output accurately describe the product — requires access to the product interface, documentation, or a subject-matter expert.

Voice alignment and audience fit can often be assessed from the brief. Task completion requires qualification: a reviewer can assess whether the output follows the brief's intended step structure, but whether a user following those steps can complete the actual task may require product access or testing. Factual accuracy of product-specific claims typically requires a separate verification step, even when the brief is complete.

### 4.5 Use the three-tier guidance structure to calibrate direction, not to specify everything

The toolkit's rules, recommendations, and contextual guidance provide structured direction at different levels of prescription. The Phase 6 experiments illustrate how different guidance tiers shape the characteristics that can be assessed, which aspects remain unresolved, and what additional review requirements emerge.

This suggests the three-tier structure is most effective when used to distinguish which decisions should be consistent (rules), which should follow a default but allow judgment (recommendations), and which require case-by-case assessment (contextual guidance). Content that must be consistent across a product — terminology, error patterns, structural conventions — belongs in rules. Content that benefits from defaults — sentence length, punctuation, variable format — belongs in recommendations. Content that changes by locale, audience, channel, or context belongs in contextual guidance.

---

## 5. Limitations of Phase 6 as a whole

1. **All outputs are illustrative constructions.** No experiment produced actual AI runs. The outputs were designed to represent plausible characteristics of AI-assisted content under each guidance condition. Actual AI-assisted outputs will differ in structure, detail, and the specific nature of any additions beyond the brief. The experiments illustrate principles; they do not measure AI performance or predict AI behaviour.

2. **The experiments cover a range of content types and formats, but not all scenarios.** Experiment 01 deliberately examined five different content types within a single notification-preferences screen, as cross-content consistency is its central contribution; the other experiments each examined one content type. This range does not represent the full scope of contexts where this toolkit would be applied. Findings may apply differently in long-form content, technical documentation, regulated domains, or content produced at high volume.

3. **Each experiment included a deliberately constructed weakness, inconsistency, or unresolved decision.** Real AI-assisted content workflows will produce unintended additions, inconsistencies, and gaps that may not follow the same patterns as these constructed examples.

4. **Interactions between guidance dimensions were not examined.** Each experiment varied one dimension of guidance while holding others constant. The combined effects of applying all five guidance dimensions simultaneously — voice standards, grounding, accessible language guidance, localisation guidance, and a complete brief — were not examined. Interactions between dimensions may produce effects that the individual experiments do not address.

5. **Reviewer scenarios were held constant within experiments.** Each experiment assumed a reviewer of fixed capability and access. Real review workflows involve reviewers with varying familiarity with the toolkit, the brief, and the content domain. The checkpoint framework identifies where certain expertise is required; developing and managing that expertise is outside this toolkit's scope.
