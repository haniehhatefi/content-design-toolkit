# AI content principles

Before writing a prompt, define the boundaries. Responsible AI use in content design is not primarily about prompt quality — it is about knowing what AI is appropriate for, what it is not, and what responsibilities remain with the content designer regardless of how good the output looks.

For guidance levels used in this document, see [Module 2 README](../02-ux-writing-standards/README.md). The same Rule / Recommendation / Contextual framework applies here: Rules are requirements without exceptions; Recommendations are strong defaults where exceptions are possible; Contextual decisions depend on the specific situation.

---

## What AI does well in content design work

AI tools are genuinely useful for a specific set of content design tasks where the goal is to generate options, apply a consistent pattern, or surface potential issues quickly:

- **Generating candidate copy** from a structured brief and grounding context — providing several options to evaluate rather than starting from a blank page
- **Applying a writing pattern consistently** across a large set of items — reformatting, restructuring, or matching a style at scale
- **Flagging readability issues** — identifying long sentences, nominalisations, passive constructions, or vocabulary likely to exceed a target reading level
- **Reformatting structured content** — converting a list to a table, restructuring a paragraph as numbered steps, or adapting copy from one content type to another
- **Producing first drafts for evaluation** — not final copy, but a starting point that is faster to edit than to generate from scratch

In all of these cases, the output requires evaluation before use. AI accelerates the generation of options; content design judgment determines which option is appropriate and what revision is needed.

---

## What AI does poorly in content design work

AI tools consistently struggle with the parts of content design that require understanding context beyond what is supplied in the prompt:

- **Understanding your product** — AI does not know what your product actually does, how users experience it, or what edge cases matter. It can produce confident copy about features or workflows it has invented.
- **Respecting brand nuance** — Even with grounding context, AI can drift from voice over longer outputs, produce copy that is on-pattern but off-voice, or revert to generic professional language when uncertain.
- **Applying judgment to ambiguity** — AI resolves ambiguous instructions by choosing a plausible interpretation and generating fluent output. It does not flag uncertainty the way a careful human reviewer would.
- **Generating accurate product-specific claims** — AI may generate specific-sounding numbers, timeframes, policy details, or feature descriptions with no basis in your product. These can be indistinguishable from accurate claims in the output itself.
- **Producing accessible content reliably** — AI tools trained on general content do not reliably apply ARIA requirements, device-neutral language conventions, or the specific accessibility standards in this toolkit without explicit and detailed grounding.

---

## Responsible use requirements

### Privacy

**`Rule`** Do not submit personal data, personally identifiable information (PII), or sensitive user data to an external AI tool without explicit organisational authorisation. This includes real user names, contact details, usage data, or any data that could identify an individual.

**`Rule`** Do not submit confidential product information — unpublished features, internal roadmaps, unreleased pricing, proprietary workflows — to an external AI tool without explicit authorisation.

In both cases, authorisation should cover the specific tool being used and the data being submitted, including any applicable organisational data-handling requirements.

**`Rec`** Use placeholder data in prompts wherever specific data is not required for the task. Illustrative examples labelled as such are almost always sufficient for content design tasks.

---

### Sensitive content areas

**`Rule`** Specialist review by a qualified expert is mandatory before use for any AI-generated copy that concerns health, legal, financial, or safety matters. This applies even where AI assistance is otherwise permitted for the content type. AI tools are not a substitute for domain expertise in regulated or high-stakes content areas.

Mandatory specialist review is a minimum safeguard, not a general permission to use AI. For some content types in these areas — legal disclaimers, clinical instructions, financial product terms, safety-critical instructions — AI-assisted generation is excluded entirely, regardless of the review process in place. See [When not to use AI](#when-not-to-use-ai-for-content) for the full exclusion list.

**`Rec`** For products operating in regulated industries, establish a team-level review process for AI-assisted content before adopting these templates. The existence of a toolkit does not constitute authorisation to use AI for regulated copy.

---

### Bias

**`Rec`** Review AI-generated content for stereotyping, exclusion, and cultural assumptions. AI tools trained on general-purpose data can produce copy that reflects patterns from that data: gendered language, culturally-specific references, or assumptions about ability, background, or technical experience. Apply the [inclusive language guide](../02-ux-writing-standards/inclusive-language-guide.md) to any AI output before use.

**`Rec`** Be particularly attentive when AI generates copy that describes users. Descriptions of "typical" users, default personas, or representative examples can embed assumptions about who the product is for.

---

### Accountability

**`Rule`** The content designer is responsible for every piece of content they publish or deliver. Using an AI tool does not transfer or reduce that responsibility. If the final copy could not be defended under review without reference to the tool, it is not ready.

**`C`** When AI assistance is used in a team or agency context, establish a shared understanding of what review is expected of content produced with AI assistance. A reviewer who does not know AI was used cannot apply appropriate scrutiny to the output.

---

### Factual and product-specific claims

**`Rule`** Verify factual and product-specific claims in AI outputs against authoritative sources, prioritising primary sources where available. AI tools may generate plausible-sounding but unsupported statements about product behaviour, policy, pricing, or technical specifications. These require verification against the product's own documentation — not against the AI's output.

**`Rule`** If a claim in an AI output cannot be verified against an authoritative source, remove it or rewrite it as a placeholder. Do not publish unverified product-specific claims.

**`Rec`** When a prompt is likely to produce product-specific claims — for example, an error message that references a recovery path, a notification that names a specific timeframe, or onboarding copy that describes a feature — include explicit grounding context for those claims in the prompt. See [grounding guide](grounding-guide.md).

---

## Pre-prompt constraint checklist

Before writing or sending any prompt, work through this checklist. It is not a comprehensive quality review — it is a pre-flight check for the most consequential decisions.

**Privacy and data**
- [ ] This prompt contains no PII or sensitive user data
- [ ] This prompt contains no confidential product information not authorised for external AI tools

**Accuracy requirements**
- [ ] I know which claims in the expected output will require verification against an authoritative source
- [ ] I have included the relevant product context in the prompt, or I will treat product-specific outputs as placeholders pending verification

**Content type and audience**
- [ ] This content type is appropriate for AI assistance (see [When not to use AI](#when-not-to-use-ai-for-content), below)
- [ ] I have identified the audience and can apply the [inclusive language guide](../02-ux-writing-standards/inclusive-language-guide.md) to the output

**Grounding**
- [ ] I have included the relevant voice and tone grounding from Module 1
- [ ] I have included the relevant Module 2 pattern reference for this content type
- [ ] I have specified a target reading level if the content type has one (see [readability standards](../02-ux-writing-standards/readability-standards.md))

**Review**
- [ ] I know who is responsible for reviewing and approving this output before use
- [ ] I know whether a specialist review is required for this content type

---

## When not to use AI for content

Some content types are not appropriate for AI-assisted generation regardless of how well the prompt is written or how good the output appears. In these cases, human authorship and specialist review are required:

- **Legal disclaimers, terms of service, or regulatory notices** — require legal review regardless of source; AI-generated legal language creates accountability risk even when it appears technically accurate
- **Safety-critical instructions** — content where an error could cause physical harm, data loss, or significant financial damage to a user
- **Health-related copy** — diagnoses, medication instructions, clinical guidance, mental health support content
- **Financial copy involving specific products, rates, or eligibility** — varies by jurisdiction; requires compliance review before use
- **Personalised content that includes or implies knowledge of a specific user's data** — even where the data is accurate, decisions about how to use it in copy require human judgment
- **Crisis or incident response content** — where accuracy and tone decisions are high-stakes, time-sensitive, and not appropriate to delegate to a first draft

For other content types, consider AI assistance on a task-by-task basis, applying the responsible-use requirements above and evaluating outputs against the [output evaluation rubric](output-evaluation-rubric.md) before use.

---

## Related documents

- [Grounding guide](grounding-guide.md) — How to structure the toolkit's standards as LLM grounding material
- [Output evaluation rubric](output-evaluation-rubric.md) — Framework for evaluating AI outputs before use
- [Failure modes](failure-modes.md) — Documented failure patterns, including hallucinated claims and fabricated functionality
- [Inclusive language guide](../02-ux-writing-standards/inclusive-language-guide.md) — Apply to AI output before use
- [Readability standards](../02-ux-writing-standards/readability-standards.md) — Target reading levels by content type
