# Templates

Operational templates for the AI Content Workflow.

## Overview

These templates support specific activities in the AI Content Workflow. They are starting points, not requirements. Each template should be adapted for the task at hand — adding fields that are relevant, removing fields that are not, and adjusting the structure for the content type, team size, and risk level.

A template that is used unchanged, regardless of whether its fields are relevant, creates documentation that practitioners work around rather than with. The purpose of a template is to prompt the right questions and record the right decisions — not to be completed in full for its own sake.

---

## Templates in this directory

| Template | Used at | Purpose |
|---|---|---|
| [`content-brief-template.md`](content-brief-template.md) | Stage 02 | The governing document for the full workflow. Establishes audience, objective, scope, requirements, and approval authority. |
| [`handoff-template.md`](handoff-template.md) | Stages 04, 05, 06 | Transfers content and context between stages or contributors. Used when one person passes work to another. |
| [`decision-and-iteration-log.md`](decision-and-iteration-log.md) | All stages | Records decisions, iterations, checkpoint outcomes, and outstanding issues throughout the workflow. |
| [`final-approval-checklist.md`](final-approval-checklist.md) | Stage 06 | Structured record of the Final approval decision: completeness of review, outstanding issues, approval authority, and accepted exceptions. |

---

## Which template to use when

**At the start of a task (Stage 02)**

Create the content brief from [`content-brief-template.md`](content-brief-template.md). Establish audience, objectives, scope, approval authority, and the approved glossary. The brief governs every subsequent stage.

Open the decision and iteration log from [`decision-and-iteration-log.md`](decision-and-iteration-log.md) for the task. It will be maintained throughout.

**When passing work between stages or contributors (Stages 04, 05, 06)**

Use [`handoff-template.md`](handoff-template.md) to record what has been completed, what checkpoint has been passed, any outstanding issues, and what the recipient needs to do next. This is particularly important when different people carry out different stages. At Stage 06, the template records the delivery handoff to the recipient — confirming what has been approved, what the recipient needs to know, and that all required reviews are complete.

**At Final approval (Stage 06)**

Use [`final-approval-checklist.md`](final-approval-checklist.md) to record the Final approval decision, the accountable approver's review of outstanding non-blocking issues, and the basis on which the content was authorised.

---

## Adapting templates for your context

**Lower-risk or shorter tasks** — The content brief can be condensed for a short, low-risk task. Focus on audience, objective, and approval authority; not every section needs to be completed in full.

**Team tasks** — The handoff template is most valuable when different contributors carry out different stages. For solo tasks, the decision log may serve as a sufficient handoff record.

**Multilingual tasks** — The content brief template includes sections for locale-specific requirements and glossary entries in target languages. Extend these sections for each locale in scope.

**Recurring content types** — For teams running the same content type repeatedly (onboarding flows, error messages, release notes), create a task-specific version of the brief template that pre-fills the fields that do not change between tasks. This reduces the setup burden while preserving the brief's governing function.

---

## Relationship to stage documents

Each stage document references the templates it uses. The stage document is the authority on when and how to use a template within the workflow; this README provides navigation and context.

| Stage document | Templates referenced |
|---|---|
| [`stages/02-ideation-and-planning.md`](../stages/02-ideation-and-planning.md) | `content-brief-template.md` |
| [`stages/03-content-creation.md`](../stages/03-content-creation.md) | `decision-and-iteration-log.md` |
| [`stages/04-review-and-refinement.md`](../stages/04-review-and-refinement.md) | `decision-and-iteration-log.md`, `handoff-template.md` |
| [`stages/05-localisation-and-adaptation.md`](../stages/05-localisation-and-adaptation.md) | `decision-and-iteration-log.md`, `handoff-template.md` |
| [`stages/06-delivery-and-maintenance.md`](../stages/06-delivery-and-maintenance.md) | `final-approval-checklist.md`, `handoff-template.md` |
