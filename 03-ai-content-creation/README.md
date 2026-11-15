# AI-assisted content creation

This module provides reusable resources, prompt templates, and evaluation exercises for content designers who want to integrate AI tools into their content work responsibly. It is not merely a prompt directory, an app, or a guide to building AI-powered products. It is a practical framework for using AI as a drafting and evaluation aid — with the content designer as decision-maker, editor, and accountable reviewer throughout.

## What AI-assisted content design means in practice

AI tools can support content design work in a number of specific, bounded ways: generating candidate copy from structured constraints, flagging readability issues, reformatting structured content to match a pattern, or applying a consistent style across a large set of items. These are tasks where AI can accelerate first-draft work and surface options for the content designer to evaluate.

They are not tasks where AI can replace content design judgment. AI tools do not understand your product, your users, or the full context in which your content will be read. They can produce confident-sounding copy that is factually inaccurate, inaccessible, inconsistent with established product language, or subtly off-voice. The content designer's role is to apply the standards in this toolkit to the AI's output — not to treat that output as complete.

This module assumes familiarity with Modules 1 and 2. The voice principles, content principles, and UX writing standards established there are what you will use to constrain, ground, and evaluate AI outputs here.

---

## The five workflow stages

This module is organised around five stages of a responsible AI-assisted content workflow. Each stage corresponds to one or more files.

| Stage | What happens | Files in this module |
|---|---|---|
| **1. Define constraints and responsible-use boundaries** | Determine what AI is and isn't appropriate for in this task; set privacy, accuracy, and review requirements before writing a single prompt | `ai-content-principles.md` |
| **2. Prepare grounding context** | Structure the toolkit's standards as LLM grounding material; decide what goes into reusable instructions, reference context, and the task-specific request | `grounding-guide.md` |
| **3. Generate, review, or rewrite through prompts** | Use a template to write a prompt for your specific task: generating microcopy, evaluating content, or rewriting for plain language and voice alignment | `prompt-templates/README.md`, `prompt-templates/microcopy-prompts.md`, `prompt-templates/review-prompts.md`, `prompt-templates/rewriting-prompts.md` |
| **4. Evaluate outputs and identify failure modes** | Apply the evaluation rubric to the AI's output; check for known failure patterns before proceeding to revision | `output-evaluation-rubric.md`, `failure-modes.md` |
| **5. Apply human review, revise, and document decisions** | Make the final content decisions yourself; record what changed and why; keep the edited output traceable to the toolkit's standards | `worked-examples.md` |

---

## How to use this module

**If you are new to AI-assisted content work,** read the files in order — principles, grounding, prompts, evaluation, failure modes — before attempting any task. The worked examples in `worked-examples.md` show the full five-stage sequence end to end.

**If you are writing a prompt for a specific task,** go directly to the relevant file in `prompt-templates/`. Read `grounding-guide.md` first if you have not yet structured grounding context for your AI tool.

**If you are evaluating an AI-generated output,** use `output-evaluation-rubric.md` as a checklist. If the output raises concerns, `failure-modes.md` documents the failure patterns covered in this module and how to identify them.

**If you are reviewing the module for portfolio or team use,** `worked-examples.md` is the most complete demonstration of the workflow. Each example preserves the AI's output and documents the human decisions that produced the final version.

---

## Prerequisites

This module builds on the foundations established in Modules 1 and 2. Before using the prompt templates or evaluation rubric, you should be familiar with:

- The three core voice attributes (Clear, Human, Helpful) and two cross-cutting writing standards (Direct, Consistent): [Module 1 — Voice principles](../01-foundations/voice-principles.md)
- The seven content principles, including the distinction between accessibility requirements and inclusive-writing recommendations: [Module 1 — Content principles](../01-foundations/content-principles.md)
- The guidance level framework (Rule, Recommendation, Contextual): [Module 2 README](../02-ux-writing-standards/README.md)
- The specific UX writing patterns you plan to reference as grounding material: [Module 2 — UX writing standards](../02-ux-writing-standards/)

If you are using this module to evaluate existing content, the [brand voice audit template](../01-foundations/brand-voice-audit-template.md) provides a complementary manual evaluation approach.

---

## Files in this module

| File | Covers |
|---|---|
| `ai-content-principles.md` | Principles and responsible-use boundaries for AI in content design work; what AI does and doesn't do well; constraints to define before writing any prompt |
| `grounding-guide.md` | How to use this toolkit's standards as LLM grounding; the distinction between reusable instructions, reference context, and task-specific requests; platform differences |
| `prompt-templates/README.md` | How to read and adapt the prompt library; template anatomy; constraints to include by default |
| `prompt-templates/microcopy-prompts.md` | Templates for generating error messages, button labels, empty states, and notifications |
| `prompt-templates/review-prompts.md` | Templates for evaluating content against the toolkit's voice and accessibility standards |
| `prompt-templates/rewriting-prompts.md` | Templates for plain language revision, readability improvement, and voice alignment |
| `output-evaluation-rubric.md` | Framework for evaluating AI outputs against the toolkit's standards; a lightweight scoring approach; red flags that require human intervention |
| `failure-modes.md` | Documented failure patterns in AI-generated content design, with annotated illustrative examples |
| `worked-examples.md` | Three fully annotated end-to-end examples — generation, review, and rewriting — with preserved AI output, structured evaluation, and documented human review decisions |
