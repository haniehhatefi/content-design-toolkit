# Experiment 03: Accessible Language Guidance

**Phase 6: Practical Experiments**

---

## 1. Research question

How do two constructed content outputs compare when one is developed with explicit accessible language guidance and the other without it, and what does evaluating their characteristics against accessibility criteria require from a human reviewer?

---

## 2. Hypothesis

The experiment constructs two illustrative outputs that differ only in whether explicit accessible language guidance was applied. Where that guidance is present, the constructed output is intended to demonstrate accessible language characteristics — shorter sentences, plain vocabulary, active constructions, and a specific action label. Where it is absent, the constructed output demonstrates the kind of formal, passive language that accessible language guidance is designed to address. Confirming whether either output meets an accessible language standard requires the reviewer to evaluate it against defined criteria, not make a general quality judgment alone. Additionally, accessible language guidance shapes how content is expressed but does not address whether the instructions the content contains are grounded and appropriate for the target audience — a distinction that requires human judgment beyond linguistic review.

---

## 3. Test scenario

The scenario is a short content sequence for a generic self-service platform in which a user is completing a task that involves uploading a document and submitting a request.

The content set consists of four pieces:

| Piece | Type | Purpose |
|---|---|---|
| P1 | Page heading | Identifies the step the user has reached |
| P2 | Instruction text | Tells the user what to do before submitting |
| P3 | Upload field helper text | Explains accepted file types and size limit |
| P4 | Action button label | Labels the submission action |

The following task context is shared by both conditions.

| Element | Context established |
|---|---|
| File size limit | 10 MB |
| Accepted file formats | PDF, Word document (.docx), JPG image |
| Available workaround for oversized files | Not specified |

The audience is a broad public audience that may include users with limited literacy, limited familiarity with online forms, users whose first language is not English, or users who find formal register difficult to process.

The initial content set is a constructed illustrative example representing content that might result from AI-assisted drafting without explicit accessible language requirements.

---

## 4. Materials

This experiment draws on the following toolkit materials:

- `02-ux-writing-standards/inclusive-language-guide.md`
- `02-ux-writing-standards/readability-standards.md`
- `03-ai-content-creation/prompt-templates/microcopy-prompts.md`
- `03-ai-content-creation/output-evaluation-rubric.md`

---

## 5. Procedure

### Step overview

1. Define the content task, the target audience, and the platform context.
2. Construct an illustrative output for Condition A, representing possible characteristics of content produced from a prompt with no accessibility specification.
3. Define the accessible language specification for Condition B.
4. Construct an illustrative output for Condition B, representing possible characteristics of content produced from a prompt that includes the accessible language specification.
5. Evaluate both outputs against the Phase 4 output evaluation rubric.
6. Assess each output against the accessible language criteria specified in Condition B.
7. Compare the intervention each output would require from a human reviewer before it could be used.

---

## 6. Observations

### 6.1 Condition A: content without accessible language guidance

**Prompt (Condition A):** The shared task context from Section 3 (file size limit, accepted formats, audience description) was included. The content instruction was:

> Write guidance for a user completing a document upload and submission step in an online form.

**Output A (illustrative):**

> **Document Submission Requirements**
>
> Before you proceed, please ensure that the documentation you intend to upload meets the requirements outlined in the guidance. All documents must be submitted in a supported file format and must not exceed the maximum permitted size.
>
> Accepted file types are PDF, DOCX, and JPG. Files must not exceed 10 MB.
>
> **Proceed**

**Characteristics of Output A:**

- Instruction text sentence length: approximately 20–25 words per sentence; multiple clauses per sentence; shorter sentences follow for file types and size limit, but these carry requirements rather than guidance
- Passive construction: "must be submitted"
- Nominalised language: "documentation," "submission," "requirements"
- Vague action label: "Proceed" does not describe what the user is doing
- Register: formal; assumes document-handling familiarity
- No indication of what happens after the user acts

---

### 6.2 Accessible language specification

The following specification was used to anchor Condition B.

| Element | Guidance provided |
|---|---|
| Reading level target | Grade 8 or below as an operational target for this experiment; whether output meets this target is not numerically verified in the evaluation |
| Sentence length | One idea per sentence; aim for under 20 words |
| Voice | Active constructions; tell users directly what to do |
| Vocabulary | Everyday words where possible; avoid formal or technical language |
| Action labels | Use the specific action the button performs, not a generic term such as "proceed" or "continue" |
| Audience note | Broad public audience; may include users less familiar with online forms, non-native English speakers, or users who find formal register harder to process |

---

### 6.3 Condition B: content with accessible language guidance

**Prompt (Condition B):** The same shared task context and content task instruction as Condition A, with the accessible language specification from Section 6.2 added. The accessible language specification is the only substantive difference between the two prompts.

**Output B (illustrative):**

> **Upload your document**
>
> Add your document to this form before you submit. Check that it is complete and saved in one of these formats: PDF, Word document, or JPG image.
>
> Your file must be under 10 MB. If it is larger, try saving it as a PDF.
>
> **Submit your document**

**Characteristics of Output B:**

- Sentence length: under 20 words per sentence; single idea per sentence throughout
- Active constructions: "Add your document," "Check that it is," "try saving it"
- Plain vocabulary: "Add" replaces "upload," "Check" replaces "ensure," everyday phrasing used throughout
- Specific action label: "Submit your document" describes the action directly
- Shorter and more direct than Output A

---

### 6.4 Instruction beyond the accessible language specification

Output B improved the linguistic characteristics of all four pieces. However, the helper text introduces an instruction that was not in the accessible language specification and is not grounded in the shared task context: "try saving it as a PDF."

The shared task context established a 10 MB file size limit and three accepted formats. It did not specify any workaround for oversized files. The PDF-saving suggestion is therefore an addition Output B introduced beyond what was provided.

Although the instruction is linguistically simple, its practical accessibility cannot be established from the language specification alone. It assumes that users have access to a suitable file-conversion method and know how to use it. Whether this is a reasonable assumption depends on the target audience, available tools, and the actual task context — none of which are established in the shared scenario.

This is a compound finding. The accessible language specification reduced linguistic barriers in the output. But Output B still introduced an instruction whose practical accessibility depends on user capability and available tools, not on vocabulary or sentence length. Plain language criteria address how content reads; they do not establish whether the actions the content describes are within the capability of the target audience or supported by the product.

This distinction — between **linguistic accessibility** (how content reads) and **task accessibility** (whether the user can reasonably perform what the content asks them to do) — is not addressed by the accessible language specification. A human reviewer evaluating Output B must assess both: does the content read accessibly, and does the content ask the user to do something that is verifiable and appropriate?

---

### 6.5 Evaluation against the Phase 4 output evaluation rubric

| Dimension | Output A assessment | Output B assessment |
|---|---|---|
| **Accuracy** | Meets — the submission requirements stated are consistent with the shared task context; no information is introduced beyond what was provided | Partially meets — the file size limit and format instructions are consistent with the shared task context; the PDF workaround suggestion is not grounded in the provided information and cannot be verified as appropriate or available from the scenario alone |
| **Voice alignment** | Does not meet — formal, passive, and unspecified; constructions such as "must be submitted" and "please ensure" are not consistent with any accessible language guidance | Meets — the communication style requirements specified in the accessible language guidance are reflected throughout; active constructions, plain vocabulary, and direct labelling are applied consistently; this assessment concerns alignment with the specified communication style, not a separately defined product voice |
| **Audience fit** | Does not meet — formal register, nominalised language, and a vague action label create barriers for lower-literacy readers; "Proceed" gives no audience-appropriate indication of what happens next | Partially meets — shorter sentences, plain vocabulary, and a specific action label are linguistic improvements suited to the described audience; the PDF workaround introduces a task step whose suitability for the target audience cannot be confirmed from the specification alone |
| **Task completion** | Partially meets — the user is told the requirements and file types, but passive constructions obscure what specifically they need to do, and "Proceed" does not confirm what the action achieves | Partially meets — the user is given a clearer and more direct sequence (add, check, submit); however, the proposed workaround is not grounded in the provided context and cannot be verified as appropriate or available, so the task path is not fully confirmed |
| **Concision** | Approximately 55 words across four pieces (including headings and action labels); appropriate length, but passive constructions and nominalisation add words without adding clarity | Approximately 50 words across four pieces (same counting convention); shorter overall, with each sentence addressing a single task step |

---

### 6.6 Human intervention required

| | Output A | Output B |
|---|---|---|
| **Nature of intervention** | Revising language to meet accessible criteria — shortening sentences, replacing passive constructions, simplifying vocabulary, replacing the action label | Verifying alignment with the accessible language criteria; confirming product-appropriate terminology for the action label; establishing whether the PDF workaround is appropriate and available for the target audience |
| **Scope of intervention** | Substantial — the output requires a full language revision pass; accessible language criteria apply to this condition, though substantial revision is needed before those criteria can be assessed | Targeted — the output is largely usable; intervention focuses on criteria-based accessibility verification and confirming the ungrounded workaround instruction |
| **Primary risk if used without review** | Excluding users with limited literacy or less familiarity with formal register; vague action label leaves the user uncertain what "Proceed" does | Including an instruction whose practical accessibility has not been verified; this risk is harder to detect because the language looks plain |
| **Expertise required for review** | Knowledge of accessible language criteria is required to confirm that the revised output meets the standard, in addition to general content judgment to identify the initial gaps | Knowledge of the accessible language criteria is required to confirm the stated communication style requirements are met; assessing the workaround instruction requires knowledge of the target audience and the product |

**Key observation:** Accessible language guidance changes the nature of the reviewer's intervention. With Output A, the reviewer must identify and revise language that does not meet the specified criteria. With Output B, the reviewer can focus more on verifying alignment with those criteria and assessing whether the instructions are grounded and appropriate. In both cases, the reviewer must know the criteria the content is expected to meet — accessibility verification is not a general content quality check, and confirmation of linguistic accessibility does not substitute for assessment of whether the instructions are grounded and appropriate for the audience.

---

## 7. Evaluation

### What the experiment demonstrates

The comparison illustrates how two constructed outputs can differ when one incorporates explicit accessible language guidance and the other does not: Output B is shorter, uses plainer vocabulary, uses active constructions, and labels the submission action specifically. Voice alignment showed clear improvement — specifically, alignment with the communication style requirements specified in the accessible language guidance. Audience fit showed partial improvement: linguistic accessibility improved, but the ungrounded workaround instruction cannot be confirmed as appropriate for the described audience. Task completion showed partial improvement: the sequence is clearer and more direct, but the workaround instruction is not verified, so the task path is not fully confirmed. Accuracy is mixed. Concision improved modestly, with both outputs being reasonably brief.

### What accessible language guidance does not cover

The experiment illustrates a boundary of accessible language guidance: it shapes how content is expressed, not whether the instructions the content contains are grounded or practically accessible to the target audience. Output B introduced an instruction ("try saving it as a PDF") that is linguistically plain but whose practical accessibility cannot be established from the language specification alone. It assumes that users have access to a suitable file-conversion method and know how to use it — an assumption that is not supported by the shared task context or the audience description.

This boundary has an implication for how accessible language guidance is applied. Where content instructs users to take specific actions, the reviewer must confirm not only that the language is accessible but that the instructions themselves are grounded, appropriate, and within the capability of the target audience. These are different evaluations requiring different knowledge.

### The nature of accessibility review

The comparison makes visible that accessibility review requires the reviewer to hold knowledge of the specific criteria the content must meet. Identifying that Output A's language is formal and passive requires general content judgment. Confirming that Output B's sentence structure and vocabulary are consistent with the accessible language specification requires the reviewer to know what that specification requires and how to evaluate against it. Assessing whether "try saving it as a PDF" is a grounded and appropriate instruction requires knowledge of the target audience and the product.

This has a practical implication for how output evaluation is scoped. When working with accessible language guidance, the evaluation checklist should include an explicit step: confirm that the specific accessibility criteria used in the brief are referenced during review — and that the review covers both how content reads and whether the instructions it contains are grounded and appropriate for the audience. Where the team's current capabilities do not cover this, specialist input should be arranged.

### Rubric dimension most visibly differentiating the two constructed outputs

The rubric dimension that most visibly differentiates the two constructed outputs in this experiment is **voice alignment** — specifically, whether the content uses plain and direct constructions appropriate for a broad public audience. This is the dimension where the difference between the two constructed outputs is most immediately apparent, because it manifests across every sentence and every action label rather than in isolated terms or specific claims.

---

## 8. Limitations

**Illustrative outputs**

Both outputs were constructed to demonstrate specific characteristics. This experiment cannot establish what AI systems would produce under equivalent conditions with these prompts, or how consistently accessible language guidance improves output quality. The comparison is an illustration of two output types and the evaluation method applied to them.

**Linguistic accessibility as one dimension of accessible content**

This experiment addresses linguistic accessibility — reading level, sentence structure, vocabulary, and action labelling. Accessible content design encompasses additional considerations not examined here, including cognitive load, task sequencing, instructions for users with specific disabilities, and content adaptations for screen reader use. The improvements illustrated in Output B are specific to linguistic form; broader accessibility evaluation would require additional criteria.

**Reading level as an approximation**

Reading-level targets, such as the Grade 8 target specified in this experiment, are practical guides rather than comprehensive accessibility measures. A short sentence can still use an unfamiliar word; a text at the right reading level can still be poorly sequenced or instruct a task the user cannot complete. Human judgment is required to evaluate accessibility holistically, beyond what a readability metric captures.

**Specification without product grounding**

The accessible language specification in Condition B did not include product-grounding elements: the product's own terminology for the submission action, or the platform's recommended workaround for oversized files. Where accessible language and product-appropriate language must align, both must be supplied. This experiment isolates the accessible language dimension; the interaction between accessible language guidance and product grounding is not examined here.

**Single content task**

This experiment uses a single document submission scenario. The relationship between accessible language guidance and output characteristics may differ for other content types — particularly those with less clear task structures, such as campaign copy, editorial content, or promotional writing.

---

## 9. Recommendations

### 1. Include an accessible language specification in content briefs for broad-audience content

Where content will reach a broad public audience — or any audience that may include lower-literacy users, non-native speakers, or users with cognitive disabilities — the content brief should include an explicit accessible language specification: a reading level target, sentence length guidance, vocabulary principles, and action label guidance. This makes accessibility criteria an input to the AI-assisted drafting step, rather than a requirement applied only in review.

*Toolkit implication:* The content brief template already includes an audience section. Adding an "accessibility criteria" field for public-facing content types would make accessible language specification a standard brief activity. The field could reference `02-ux-writing-standards/readability-standards.md` for the applicable criteria.

### 2. Ensure accessibility criteria are present and visible during the output evaluation pass

Evaluating whether AI-assisted content meets accessible language criteria requires the reviewer to hold knowledge of those criteria. This is not equivalent to a general clarity or quality review. The evaluation checklist should specify the applicable accessibility criteria explicitly enough that any reviewer can apply them, and where the team's current capabilities do not cover a required standard, specialist input should be arranged for that review.

*Toolkit implication:* The five human oversight checkpoints in Phase 5 include a quality review and a final approval stage. For content types with explicit accessibility requirements, the quality review checkpoint should note the applicable accessibility criteria, so the reviewer knows what standard they are evaluating against, not only that accessibility is a consideration.

### 3. Extend accessibility review to cover whether instructions are grounded and appropriate, not only linguistically plain

Where content instructs users to take specific actions, the accessibility review should confirm that those instructions are grounded in the provided information and appropriate for the target audience — not only that the language describing them is plain. An instruction can be linguistically simple and still introduce an unverified assumption about what users can do or what tools they have available.

*Toolkit implication:* The inclusive language guide and readability standards provide criteria for evaluating linguistic accessibility. A note in the output evaluation rubric about verifying instructional content — particularly for broad audiences where task assumptions may not hold — would make this dimension of review explicit alongside the language criteria.

### 4. Consider an accessible language worked example as a future toolkit enhancement

The worked examples in `03-ai-content-creation/worked-examples.md` are the primary practical reference for output evaluation. An accessible language example — showing a before-and-after revision with the specific criteria applied, and including assessment of both linguistic and task accessibility — would make the evaluation method visible and replicable for practitioners who have not previously applied accessible language standards.

*Toolkit implication:* This is a possible future enhancement to the worked examples rather than a change to any currently completed phase. It could be considered when consolidating Phase 6 findings into the toolkit's reference materials.
