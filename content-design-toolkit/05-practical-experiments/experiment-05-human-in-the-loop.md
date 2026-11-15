# Experiment 05: Human-in-the-Loop Oversight

**Phase 6: Practical Experiments**

---

## 1. Research question

How does brief completeness affect the scope of a Quality checkpoint review, and what can a reviewer establish about an AI-assisted output through brief-based compliance assessment when reviewing with a complete brief compared with a minimal brief?

---

## 2. Hypothesis

The experiment constructs two illustrative outputs that differ only in the completeness of the brief used to generate them. Where a complete brief is present, the constructed output is intended to demonstrate brief-aligned characteristics — specific UI terminology, audience-appropriate register, and content scoped to the brief's requirements. Where only a minimal brief is present, the constructed output demonstrates generic characteristics — non-specific UI references, unspecified register, and content whose scope relevance cannot be assessed without a scope definition. The experiment then examines what a Quality checkpoint reviewer can establish about each output through brief-based compliance assessment, given the brief available to them. Where the brief is complete, the reviewer is positioned to assess compliance with stated requirements and to identify output additions that go beyond those requirements. Where only a minimal brief is available, the reviewer can assess surface quality only; the requirements against which compliance would be assessed were not established.

---

## 3. Test scenario

The scenario is a short help centre article for a generic task management platform, explaining how to assign a task to a team member. The article is a single standalone piece intended to allow a user to complete the task without additional support.

The following task context is shared by both conditions.

| Element | Context established |
|---|---|
| Platform type | A generic task management platform |
| Article topic | Assigning a task to a team member |
| Article format | A standalone help centre article |
| Target length | Approximately 35–70 words including title |

The audience and the article's specific requirements are not defined in the shared task context. These are established in the complete brief used for Condition B.

The Quality checkpoint reviewer in this scenario has access to the brief and the AI-assisted output but not to the product interface or its documentation. The experiment therefore examines brief-based compliance assessment; independent verification using product access is not in scope.

---

## 4. Materials

This experiment draws on the following toolkit materials:

- `03-ai-content-creation/grounding-guide.md`
- `03-ai-content-creation/output-evaluation-rubric.md`
- `04-ai-content-workflow/human-checkpoints.md`

---

## 5. Procedure

### Step overview

1. Define the content task and establish the shared task context.
2. Construct an illustrative output for Condition A, representing possible characteristics of content produced from a prompt with a minimal brief.
3. Define the complete brief specification for Condition B.
4. Construct an illustrative output for Condition B, representing possible characteristics of content produced from a prompt that includes the complete brief specification.
5. Identify any claims in the constructed outputs that are not grounded in the brief specification.
6. Evaluate both outputs against the Phase 4 output evaluation rubric.
7. Assess what a Quality checkpoint reviewer can establish about each output through brief-based compliance assessment, given the brief available to them.
8. Compare the nature and scope of the review each brief condition enables.

---

## 6. Observations

### 6.1 Condition A: content with a minimal brief

**Prompt (Condition A):** The shared task context from Section 3 (platform type, article topic, format, target length) was included. The content instruction was:

> Write a short help centre article explaining how to assign a task to a team member.

**Output A (illustrative — constructed to represent possible characteristics of content produced without a complete brief):**

> **Assigning Tasks**
>
> To assign a task to a team member, open the task and select the assignment option. Find the user you want to assign the task to and confirm your selection. The task will then be associated with that team member, and they may be notified depending on your notification settings.
>
> You can update the assignment at any time by returning to the task and repeating the process.

**Characteristics of Output A:**

- UI references are generic: "assignment option," "confirm your selection" — not grounded in product-specific terminology
- Format: prose paragraphs rather than numbered steps
- Register: neutral and general; not calibrated for a specified audience
- Scope: includes a reference to notification settings ("they may be notified depending on your notification settings") and reassignment ("You can update the assignment at any time") — both topics whose inclusion cannot be assessed for scope appropriateness without a scope definition
- Word count: approximately 70 words

---

### 6.2 Complete brief specification

The following brief was used to anchor Condition B.

| Element | Specification provided |
|---|---|
| Audience | Team leads using the platform for the first time; comfortable with software but unfamiliar with this tool's interface and conventions |
| Voice reference | Direct, numbered steps; imperative constructions for user actions; short declarative statements for system responses; no jargon |
| UI terminology | "Assign" button; "Team members" panel; task "Owner" field |
| Article scope | Covers basic task assignment only; excludes reassignment, permission levels, and notification behaviour or settings |
| Success criteria | A user who follows the steps can complete a task assignment without leaving the article |

---

### 6.3 Condition B: content with a complete brief

**Prompt (Condition B):** The same shared task context and content task instruction as Condition A, with the complete brief specification from Section 6.2 added. The brief specification is the only substantive difference between the two prompts.

**Output B (illustrative — constructed to represent possible characteristics of content produced with a complete brief):**

> **Assign a task**
>
> Follow these steps to assign a task to a team member.
>
> 1. Open the task.
> 2. Select **Assign**.
> 3. In the **Team members** panel, select the team member.
> 4. A notification is sent to the assigned team member.

**Characteristics of Output B:**

- UI terminology from the brief: "Assign" button, "Team members" panel — consistent with the brief's specified terminology
- Format: numbered steps with imperative constructions for user actions and declarative statements for system responses — consistent with the voice reference
- Register: direct and specific; appropriate for a first-time user learning the tool's interface
- Scope: covers basic task assignment; does not cover reassignment or permission levels — consistent with the scope specification
- Word count: approximately 37 words

---

### 6.4 Claim beyond the brief specification

Output B reflects the brief's requirements in structure, terminology, and scope. However, Step 4 includes a claim that is not established in the brief specification: "A notification is sent to the assigned team member."

The brief specifies that the article should cover basic task assignment and explicitly excludes notification behaviour or settings. The notification claim is therefore ungrounded in two related ways: it asserts a fact about platform behaviour that the brief does not establish, and it falls directly within the area the scope specification explicitly excludes.

A Quality checkpoint reviewer assessing Output B against the complete brief can observe that:

1. UI terminology matches the brief's specifications.
2. The numbered step format, imperative user-action constructions, and declarative system-response statements match the voice reference.
3. Reassignment and permission levels are excluded, consistent with the scope specification.
4. Step 4 contains a claim — "A notification is sent" — that is not established in the brief and describes notification behaviour within the area the scope specification explicitly excludes.

The brief establishes a baseline that makes the gap visible.

Output A contains a structurally parallel reference: "they may be notified depending on your notification settings." This claim is equally ungrounded against the shared task context, but its conditional phrasing presents it as uncertain rather than confirmed. Neither claim is verifiable from the brief alone; both would require checking against the actual product. The difference is that the complete-brief reviewer assessing Output B is positioned to identify the notification claim as ungrounded and out of scope; the minimal-brief reviewer assessing Output A has no baseline against which to identify either notification reference as a scope issue.

This observation introduces the central distinction the experiment examines: **checkpoint scope** (what the brief establishes as assessable through brief-based compliance review) vs. **reviewer capability** (the reviewer's own knowledge and expertise). With a minimal brief, checkpoint scope is limited regardless of reviewer capability — the reviewer cannot assess dimensions the brief does not define. With a complete brief, checkpoint scope extends to those dimensions, enabling the reviewer to apply their capability fully.

This distinction applies specifically to brief-based compliance assessment. A reviewer with independent access to the product interface or documentation could potentially verify claims beyond what the brief establishes — for example, confirming whether a notification is actually sent on task assignment. That form of assessment is outside this experiment's scope, which examines the brief-based review scenario specified in Section 3.

---

### 6.5 Evaluation rubric

Both outputs were evaluated against the five dimensions of the Phase 4 output evaluation rubric. The reviewer is assumed to have access to the brief and the output but not to the product interface or its documentation (see Section 3).

| Dimension | Output A | Output B |
|---|---|---|
| Accuracy | Cannot be established from the minimal brief — the shared task context does not specify product terminology, notification behaviour, or article scope, so there is no reference against which to assess the output's claims through brief-based review | Partially brief-consistent but not independently verified — UI terminology and step structure are consistent with the brief specification; consistency with the brief does not confirm accuracy against the actual product interface; the notification claim in Step 4 is not grounded in the brief and conflicts with its scope specification |
| Voice alignment | Cannot be assessed — no voice reference was specified; the output has a neutral register and prose format, but whether these meet requirements cannot be determined without a voice reference | Meets — numbered steps, imperative user-action constructions, and declarative system-response statements are consistent with the voice reference; no jargon is used |
| Audience fit | Cannot be assessed — the audience was not specified; the output uses neutral language and prose format, but whether these are appropriate for the intended audience cannot be determined without an audience definition | Meets — the direct, step-by-step format with specific UI labels is appropriate for a first-time user learning the tool's interface |
| Task completion | Partially meets — the essential steps are present in the correct order; the prose format may require the user to interpret steps rather than follow them directly; the reassignment reference and notification caveat extend beyond the implied task, but their scope relevance cannot be assessed without a scope definition | Meets the brief's intended structure — the step sequence covers the specified procedure as defined by the brief; whether a user following these steps can complete the actual task cannot be confirmed through brief-based review alone, as this would require verifying the product interface |
| Concision | Approximately 70 words; at the upper end of the target range; the notification reference and reassignment note add content whose scope relevance cannot be assessed without a scope definition | Approximately 37 words; within the target range; the step format produces a shorter word count than prose; each step addresses one action |

**Rubric dimensions most visibly differentiating:** Voice alignment and audience fit. For Output B, both dimensions are assessable and show compliance with the brief. For Output A, both dimensions cannot be assessed — not because the output fails on those dimensions, but because the brief does not establish requirements against which compliance would be assessed. This makes voice alignment and audience fit simultaneously the most visible differentiators between the two outputs and the clearest illustration of what brief completeness enables at the Quality checkpoint.

**On brief compliance and factual accuracy:** The rubric distinguishes between what can be established through brief-based assessment and what would require independent verification. An output that is consistent with the brief is brief-compliant; it is not independently verified as accurate. These are distinct assessments: a UI term can match the brief without matching the actual product interface, and a step can follow the brief's procedure without accurately describing actual product behaviour.

---

### 6.6 Quality checkpoint comparison

The following table summarises what a Quality checkpoint reviewer can and cannot establish about each output through brief-based compliance assessment, given the brief available to them in each condition.

| | Output A — quality review with minimal brief | Output B — quality review with complete brief |
|---|---|---|
| Nature of review | Surface quality assessment — logical step order, language clarity, general appropriateness | Brief-based compliance assessment — checking output against specified requirements, identifying additions beyond those requirements |
| What the reviewer can establish | The article has a logical structure and uses clear language; the step sequence covers the basic task | UI terminology is consistent with the brief; voice and format are consistent with the reference; scope is consistent with the brief specification |
| What the reviewer can identify as a gap | Cannot identify — there is no baseline against which to determine whether the notification reference or the reassignment note represent scope issues | The notification claim in Step 4 is not grounded in the brief; the scope specification explicitly excludes notification behaviour or settings; the claim requires removal before publication |
| What cannot be established through brief-based review in either condition | — | Whether the notification claim is factually accurate; whether the UI terminology in the brief matches the actual product interface; whether a user following these steps can complete the task in the actual product |
| Risk if the output proceeds without further review | An article that may contain inaccurate terminology, may be misaligned with its audience, and may include content of uncertain scope — these gaps are not visible from the minimal brief | An article with one ungrounded factual claim that the brief establishes as identifiable; this gap is visible from the brief but requires product verification to resolve |

**Key observation:** Brief completeness determines the ceiling of brief-based compliance assessment at the Quality checkpoint. With a complete brief, the reviewer can confirm compliance with stated requirements and identify additions that go beyond those requirements. With a minimal brief, the reviewer can confirm surface quality only — not because they lack expertise, but because the brief does not establish the requirements against which compliance would be assessed. The same reviewer, with the same expertise, produces structurally different review value depending on what the brief provides.

This distinguishes two independent dimensions of checkpoint quality: **checkpoint scope** (determined by brief completeness, a workflow property) and **reviewer capability** (the reviewer's own knowledge and expertise, a person property). Brief completeness sets the ceiling on what can be established through brief-based compliance review; reviewer capability determines how much of that scope is actually covered. Neither dimension alone is sufficient: a complete brief without a capable reviewer does not produce a reliable quality review, and a capable reviewer without a complete brief cannot produce a complete compliance assessment.

---

## 7. Evaluation

### What the comparison illustrates

The comparison illustrates how two constructed outputs can differ when one is produced with a complete brief and the other with a minimal brief, and what that difference means for brief-based Quality checkpoint review. The complete-brief condition enables the reviewer to assess voice alignment and audience fit against explicit requirements. Output B meets the specified voice and audience criteria; these dimensions cannot be assessed for Output A because the minimal brief does not establish corresponding requirements. In structural terms, Output B provides a direct step sequence consistent with the brief's intended procedure; however, actual task completion remains unverified without product access, and Output A cannot be evaluated for scope appropriateness without a scope definition. For Output A, accuracy cannot be established from the minimal brief alone. For Output B, the output is partially brief-consistent but the notification claim remains ungrounded, and accuracy against the actual product cannot be confirmed through brief-based review. The comparison therefore demonstrates a difference in what can be established through brief-based review, rather than a measured improvement in output quality. Output B is shorter (approximately 37 words) than Output A (approximately 70 words), though the difference partly reflects the step format versus prose format rather than a concision advantage per se.

### What brief completeness does not establish

The experiment also illustrates a constraint on the complete-brief condition. A complete brief establishes what to review against, but it does not establish factual accuracy against the product. The notification claim in Output B is identifiable as ungrounded from the brief — but whether the claim is accurate requires verification against the actual product. A complete brief creates a reviewable baseline for compliance assessment; it does not substitute for product access at the accuracy verification stage. This constraint applies to both conditions: the difference is that the complete-brief reviewer knows where the gap is, and the minimal-brief reviewer does not.

### The nature of Quality checkpoint review

The comparison makes visible a distinction between two independent dimensions of checkpoint quality: **checkpoint scope** (what the brief establishes as assessable through brief-based review — a workflow property) and **reviewer capability** (what the reviewer knows — a person property). These factors are independent. Brief completeness sets the ceiling on checkpoint scope; reviewer capability determines how much of that scope is actually covered.

This relationship between reviewer context and assessment scope was present across the preceding experiments, though in different forms: Experiment 01 examined voice consistency requiring cross-content review context; Experiment 02 examined how grounding shifts oversight from authoring to fact-checking; Experiments 03 and 04 examined how the scope of provided guidance shapes the scope of reviewable outputs. Experiment 05 makes the structural principle explicit: brief completeness is a workflow property that determines the ceiling of brief-based compliance review at the Quality checkpoint.

---

## 8. Limitations

1. **Illustrative outputs.** Both outputs are constructed examples designed to represent possible characteristics of content produced under each brief condition. They are not the result of live AI runs. Actual AI-assisted content drafts may differ in structure, detail, and the nature of any additions beyond the brief.

2. **Single content type.** The experiment uses a procedural help centre article with specific UI steps. This content type has clear accuracy criteria (UI terminology either matches the product or it does not) that make the brief-completeness effect particularly visible. Other content types — campaign copy, editorial content, long-form articles — may present different review challenges where brief completeness affects quality in different ways.

3. **Quality checkpoint focus.** The experiment examines only the Quality checkpoint. The Direction checkpoint, which establishes the brief, and the Alignment checkpoint, which confirms direction before substantive work begins, are not examined in this scenario. The relationship between early-stage checkpoint quality and downstream checkpoint scope is a conceptual implication of the findings, not a directly observed effect of this experiment.

4. **Reviewer access assumption.** The reviewer is assumed to have access to the brief and the output but not to the product interface or its documentation (see Section 3). A reviewer with product access could independently verify claims beyond the brief, which would extend the scope of their assessment. This experiment examines brief-based compliance review only; the interaction between brief completeness and reviewer product access is not examined here.

5. **Binary brief completeness.** The experiment contrasts a minimal brief (task and shared context only) with a complete brief (task, context, audience, voice reference, UI terminology, scope, success criteria). Partial briefs — where some elements are specified but others are absent — would produce partial review capability at the Quality checkpoint. This graduated effect is not examined here.

6. **Reviewer expertise assumption.** Both conditions assume a reviewer of equal capability. The experiment examines brief completeness as a variable; reviewer expertise is held constant. The interaction between reviewer expertise and brief completeness — for instance, whether a domain expert with product knowledge can partially compensate for a minimal brief — is not examined in this scenario and is presented as a conceptual implication rather than an experimentally established finding.

---

## 9. Recommendations

1. **Establish review criteria at the Direction checkpoint, not the Quality checkpoint.** The Direction checkpoint should produce a brief that specifies success criteria, voice reference, accuracy baseline, and scope definition — not only the content task. A brief that specifies only the task creates a downstream compliance review gap at the Quality checkpoint, regardless of reviewer expertise. Direction-setting is load-bearing for the brief-based compliance assessment that the Quality checkpoint performs.

2. **Share the complete brief with the Quality checkpoint reviewer.** The reviewer's compliance review scope is bounded by what the brief establishes. Where the brief is not shared with the reviewer — or where the reviewer receives only the AI-assisted output without its context — the review is structurally limited to surface quality assessment. The complete brief is the reviewer's reference document, not an internal planning artefact.

3. **Distinguish surface quality review from brief-compliance review.** A surface quality review (clarity, grammar, logical order) is a different and more limited assessment than brief-compliance review (compliance with specified requirements, identification of additions beyond those requirements). When the output evaluation rubric is applied, dimensions not covered by the brief should be noted as unassessable, not assumed to be satisfied. A finding of "unassessable" is distinct from "meets" or "does not meet."

4. **Include an explicit check for claims beyond the brief specification.** As illustrated in the constructed examples of Experiments 02 and 05, possible outcomes of AI-assisted content drafting in both grounded and ungrounded conditions may include factual claims that go beyond the provided materials. The Quality checkpoint should include a standard check: for each specific factual claim in the output, confirm it is traceable to the brief or grounding materials. Claims that cannot be traced to the brief or grounding materials require resolution before publication. A claim that is within scope can be grounded in the brief or verified against the product. A claim that falls within an explicitly excluded scope area must be removed, or the scope definition formally revised before the claim is retained. This check requires a complete brief to perform reliably; with a minimal brief, the baseline for identifying what is and is not grounded — and what is within or outside scope — is not established.
