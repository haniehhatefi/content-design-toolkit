# AI Content Workflow

A structured framework for AI-assisted content work: six lifecycle stages, human oversight requirements, and supporting guidance for individual practitioners and small teams.

## Contents

- [About this module](#about-this-module)
- [The six lifecycle stages](#the-six-lifecycle-stages)
- [Human oversight checkpoints](#human-oversight-checkpoints)
- [Operating modes](#operating-modes)
- [Documents in this directory](#documents-in-this-directory)

---

## About this module

This module provides a repeatable process for AI-assisted content work. It organises the work into six connected lifecycle stages, defines where human oversight is required, and provides supporting guidance for working independently or as part of a small team.

**Start with [`master-workflow.md`](master-workflow.md).** It describes the complete process, explains how the stages connect, and links to all detailed stage documents and supporting resources.

---

## The six lifecycle stages

| Stage | Purpose |
|---|---|
| [01. Research and discovery](stages/01-research-and-discovery.md) | Examine existing content, synthesise supplied research, and identify potential gaps |
| [02. Ideation and planning](stages/02-ideation-and-planning.md) | Explore ideas, establish requirements, and plan the content approach |
| [03. Content creation](stages/03-content-creation.md) | Draft, restructure, and adapt content |
| [04. Review and refinement](stages/04-review-and-refinement.md) | Evaluate content against requirements, voice guidelines, and content standards |
| [05. Localisation and adaptation](stages/05-localisation-and-adaptation.md) | Translate, adapt, and validate content for other languages and cultural contexts |
| [06. Delivery and maintenance](stages/06-delivery-and-maintenance.md) | Coordinate handoffs, approve deliverables, and manage future updates |

Stage 05 is conditional. Tasks that do not involve multiple languages or cultural contexts move directly from stage 04 to stage 06.

The stages provide a shared structure rather than a fixed production sequence. Work may return to an earlier stage when review findings, new requirements, or changing circumstances call for revision. Return paths and triggers are described in `master-workflow.md`.

Detailed instructions for each stage are in the [`stages/`](stages/) directory.

---

## Human oversight checkpoints

Five checkpoints define where human review and decision-making are required. No stage advances without the responsible practitioner confirming that exit conditions are met.

| Checkpoint | When it applies | Purpose |
|---|---|---|
| **Direction** | Stages 01–02 | Confirm that research questions, objectives, and constraints are established before AI-assisted work begins |
| **Alignment** | Before AI-assisted intermediate outputs advance; at least once per task | Confirm that AI-generated approaches or draft content follow the established brief and direction before proceeding |
| **Quality** | Stage 04 | Structured review of content against requirements, voice guidelines, and content standards |
| **Localisation** | Stage 05 | Validate language accuracy, terminology, meaning, and cultural suitability for each locale |
| **Final approval** | Stage 06 | Final human review and approval before any deliverable is treated as complete |

Mandatory and conditional checkpoint requirements are defined in [`human-checkpoints.md`](human-checkpoints.md).

---

## Operating modes

**Individual operating mode** — for practitioners working independently. One person holds all responsibilities: defining the brief, guiding AI assistance, reviewing outputs, making decisions, and approving the final deliverable. The six-stage structure applies in full; the depth of each stage should be proportionate to the task.

**Collaborative team operating mode** — for small teams. The framework coordinates responsibilities, handoffs, and approval authority across contributors. Functional responsibilities include content lead, reviewer, localisation reviewer, and approver. Roles may be combined when team size requires it, but accountability must remain clear.

Both modes are introduced in [`master-workflow.md`](master-workflow.md). Detailed operating guidance is in [`individual-operating-model.md`](individual-operating-model.md) and [`team-operating-model.md`](team-operating-model.md).

---

## Documents in this directory

### Central reference

| Document | Purpose |
|---|---|
| [`master-workflow.md`](master-workflow.md) | The complete workflow: six stages, operating modes, stage transitions, and links to all supporting resources |

### Stage documents

Detailed instructions, activity-level guidance, checklists, and checkpoint references for each lifecycle stage.

| Stage | Document |
|---|---|
| 01. Research and discovery | [`stages/01-research-and-discovery.md`](stages/01-research-and-discovery.md) |
| 02. Ideation and planning | [`stages/02-ideation-and-planning.md`](stages/02-ideation-and-planning.md) |
| 03. Content creation | [`stages/03-content-creation.md`](stages/03-content-creation.md) |
| 04. Review and refinement | [`stages/04-review-and-refinement.md`](stages/04-review-and-refinement.md) |
| 05. Localisation and adaptation | [`stages/05-localisation-and-adaptation.md`](stages/05-localisation-and-adaptation.md) |
| 06. Delivery and maintenance | [`stages/06-delivery-and-maintenance.md`](stages/06-delivery-and-maintenance.md) |

See [`stages/README.md`](stages/README.md) for a directory overview.

### Operating guidance

| Document | Purpose |
|---|---|
| [`human-checkpoints.md`](human-checkpoints.md) | Mandatory and conditional checkpoints, decision criteria, and responsibility matrix |
| [`individual-operating-model.md`](individual-operating-model.md) | Detailed guidance for applying the workflow independently |
| [`team-operating-model.md`](team-operating-model.md) | Detailed guidance for applying the workflow in a small team |
| [`localisation-workflow.md`](localisation-workflow.md) | Operational process for AI-assisted multilingual content |
| [`implementation-guide.md`](implementation-guide.md) | Guidance for introducing and adapting the framework |
| [`retrospective-guide.md`](retrospective-guide.md) | Structured questions for evaluating and improving the workflow |

### Templates

Reusable templates for common workflow activities.

| Template | Purpose |
|---|---|
| [`templates/content-brief-template.md`](templates/content-brief-template.md) | Define objectives, audience, context, requirements, and constraints |
| [`templates/handoff-template.md`](templates/handoff-template.md) | Transfer work and context between contributors |
| [`templates/decision-and-iteration-log.md`](templates/decision-and-iteration-log.md) | Record AI outputs, decisions, changes, and rationale |
| [`templates/final-approval-checklist.md`](templates/final-approval-checklist.md) | Confirm that a deliverable is ready for use |

See [`templates/README.md`](templates/README.md) for guidance on when to use each template.
