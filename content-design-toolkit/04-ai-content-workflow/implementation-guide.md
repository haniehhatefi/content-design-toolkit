# Implementation Guide

How to set up and start using the AI Content Workflow framework.

## Contents

- [1. What this framework covers](#1-what-this-framework-covers)
- [2. Who this guide is for](#2-who-this-guide-is-for)
- [3. Reading order — before your first task](#3-reading-order--before-your-first-task)
- [4. What to set up before you start](#4-what-to-set-up-before-you-start)
- [5. Using the framework as an individual practitioner](#5-using-the-framework-as-an-individual-practitioner)
- [6. Using the framework as a team](#6-using-the-framework-as-a-team)
- [7. What you can adapt and what you should keep fixed](#7-what-you-can-adapt-and-what-you-should-keep-fixed)
- [8. Common mistakes when getting started](#8-common-mistakes-when-getting-started)
- [9. References](#9-references)

---

## 1. What this framework covers

This framework covers the AI-assisted content lifecycle from research and discovery through delivery and maintenance. It describes how to integrate AI tools into content work responsibly — where AI assistance is appropriate, where it is not, what human decisions are required at each stage, and how those decisions are documented.

The framework has six stages and five human oversight checkpoints. The stages describe the work; the checkpoints describe the decisions that must be made by qualified people before the work can proceed.

This guide does not explain the stages in detail — the stage documents do that. Its purpose is to help you read the framework, set up for your first task, and make the structural decisions that affect how you will use it.

---

## 2. Who this guide is for

This guide is for content designers, UX writers, and content practitioners who are:

- Using this framework for the first time and need to understand its structure before starting a task
- Setting up the framework for use by a team
- Adapting the framework for a specific content type, product context, or team structure

It assumes you have some familiarity with AI-assisted content work but does not assume you have used this framework before. It does not assume a specific tool set or platform.

---

## 3. Reading order — before your first task

Read in this order before running your first task.

**Start with the lifecycle overview**

[`master-workflow.md`](master-workflow.md) — Read this first. It describes the six stages, the five checkpoints, and how they connect. It gives you the full picture before you go into any stage in detail. Reading time: 15–20 minutes.

**Read the checkpoint definitions**

[`human-checkpoints.md`](human-checkpoints.md) — The five checkpoints are the most important structural element in the framework. Understanding what each checkpoint is, who carries it out, and what it decides will help you read the stage documents more usefully. Reading time: 10–15 minutes.

**Choose your operating model**

[`individual-operating-model.md`](individual-operating-model.md) — Read this if you are working alone on most or all of a task.

[`team-operating-model.md`](team-operating-model.md) — Read this if you are working as part of a team, or if different people will carry out different stages.

**Read the stage documents relevant to your first task**

You do not need to read all six stage documents before starting. Read Stage 02 ([`stages/02-ideation-and-planning.md`](stages/02-ideation-and-planning.md)) before creating the content brief for your first task, and read each subsequent stage document before beginning that stage.

**Read the localisation workflow if applicable**

[`localisation-workflow.md`](localisation-workflow.md) — Read this before starting Stage 05 if your task requires localisation. You do not need to read it for single-language tasks.

---

## 4. What to set up before you start

**Confirm approval authority**

Before creating the content brief for your first task, confirm who has the authority for each of the three approval checkpoints: Quality review (Stage 04), Locale approval (Stage 05, if applicable), and Final approval (Stage 06). These roles may be the same person or different people depending on your team structure and the nature of the content.

If approval authority is not confirmed before the task begins, you are likely to discover it only when a checkpoint is reached — at which point a delay is unavoidable.

**Establish the approved glossary**

An approved glossary of key terms for the content — and, for multilingual tasks, approved translations for each locale — should be in place before Stage 03 (Content creation). Terminology decisions made ad hoc during content creation are inconsistent and difficult to retroactively apply. Build the glossary during Stage 02 as part of the brief.

**Identify locale reviewers for multilingual tasks**

If the task requires localisation, identify and confirm a qualified locale reviewer for each target locale before Stage 05 begins. A qualified reviewer has appropriate proficiency in the target language, relevant domain knowledge, and familiarity with the target cultural context. Do not wait until Stage 05 to discover that a reviewer is not available.

**Prepare the content brief**

The content brief is the governing document for the full workflow. It is created at Stage 02 and referenced at every subsequent stage. Use [`templates/content-brief-template.md`](templates/content-brief-template.md) as a starting point. A brief that is complete and accurate at Stage 02 will reduce the need for redirection and rework at later stages.

**Review the AI use exclusions**

The AI Content Creation module establishes categories of content that must not be generated or translated using AI assistance, regardless of subsequent human review. These include legal disclaimers, clinical instructions, financial product terms, and safety-critical instructions. Review these exclusions before Stage 03 and ensure they are reflected in the brief.

---

## 5. Using the framework as an individual practitioner

When you are working alone on a task, you will carry out both the AI-assisted activities and the human responsibilities described in each stage document. The framework is designed to work for individual practitioners, not only teams.

The key discipline for individual use is maintaining the checkpoint structure even when no other person is involved. Some checkpoints — Quality review and Final approval in particular — benefit from a degree of separation between the person who produced the content and the person who assesses it. Where you are both practitioner and approver for a task, build in enough distance between finishing the content and reviewing it that you can assess it independently. As a practical measure, reviewing content after a break of at least several hours — the following morning, if feasible — tends to produce a more independent assessment than reviewing it immediately after finishing.

Where the content is high-stakes, complex, or will reach a broad audience, consider whether checkpoint responsibilities should be shared even if you are the primary practitioner. A subject-matter expert or second content designer can carry out the Quality checkpoint without being involved in content creation.

Refer to [`individual-operating-model.md`](individual-operating-model.md) for guidance on adapting the framework for solo use, including lighter documentation approaches suitable for lower-risk tasks.

---

## 6. Using the framework as a team

When multiple people are working on a task, the framework distributes responsibilities across roles. The stage documents describe both the AI-assisted activities and the human responsibilities for each stage; operating model documents describe how those responsibilities are structured for team use.

**Before the first team task, align on:**

- **Approval authority for each checkpoint.** Who carries out the Quality review, Locale approval (for multilingual tasks), and Final approval? These roles must be clearly assigned before work begins.
- **Brief ownership.** Who is responsible for creating and maintaining the content brief? Who has the authority to change it, and how are changes communicated?
- **Handoff process.** When one contributor passes work to the next, what does a handoff look like? Use [`templates/handoff-template.md`](templates/handoff-template.md) as the basis for your team's handoff process.
- **Decision log ownership.** Who maintains the decision and iteration log for the task? For team tasks, this is typically the lead practitioner.
- **Glossary ownership.** Who maintains the approved glossary? Who approves additions and changes?

Refer to [`team-operating-model.md`](team-operating-model.md) for guidance on role structures, task briefings, and coordination across stages.

---

## 7. What you can adapt and what you should keep fixed

The framework is designed to be adaptable. Practitioners are expected to apply it in context, not follow it mechanically regardless of task type, team size, or content risk.

**What you can adapt**

- The templates — they are starting points. Adapt them for your task type, team, and content context.
- The level of documentation — lower-risk tasks benefit from lighter documentation; high-stakes or compliance-sensitive content warrants more thorough records.
- The timing of checkpoints within a stage — when within a stage a checkpoint occurs may vary; what must not vary is that it occurs and that the right person carries it out.
- The format and depth of the content brief — a short task may need a shorter brief; the brief must still establish the governing requirements.
- Stage entry and exit conditions — follow the conditions established in the stage documents. You may adapt operational details where the framework permits, but must not weaken mandatory requirements, prerequisites, checkpoint criteria, or approval rules. Document any permitted contextual adjustments in the content brief.

**What you should keep fixed**

- **The five checkpoint types and their authority structure.** Direction, Alignment, Quality, Locale approval, and Final approval are distinct checkpoints with distinct roles. Merging them, omitting them, or delegating them to AI is not appropriate.
- **The exception acceptance rules.** Only Final approval (Stage 06) can explicitly accept outstanding non-blocking issues as exceptions, with recorded rationale. Quality review (Stage 04) and Locale approval (Stage 05) must meet their mandatory criteria before proceeding.
- **The requirement to quality-review before localising.** Localisation must not begin on content that has not passed Quality review at Stage 04.
- **The Phase 4 AI use exclusions.** Legal disclaimers, clinical instructions, financial product terms, and safety-critical instructions must not use AI assistance, regardless of subsequent review.
- **The human accountability at checkpoints.** No checkpoint can be passed by AI assessment alone. Each requires a qualified human decision.

---

## 8. Common mistakes when getting started

**Starting without a complete content brief**

The brief is the governing document. A vague or incomplete brief means that requirements, audience, scope, and approval authority are undefined — which creates misalignment at every stage that follows. Take the time to complete it before Stage 03.

**Treating AI output as a first draft rather than a starting point**

AI-generated content, including AI-generated translation, requires evaluation, not editing. The question is not "what needs to change in this draft" but "does this output accurately and appropriately meet the requirements." A draft that does not meet requirements should be regenerated with improved grounding, not patched.

**Skipping checkpoint documentation**

Checkpoints are only valuable if they are real decisions with recorded outcomes. A checkbox that records nothing — no findings, no rationale, no decision — provides no governance value and no reference point for future questions about the content's approval history.

**Discovering locale reviewer availability at Stage 05**

A locale reviewer who is unavailable at Stage 05 stalls the entire task. Identify and confirm locale reviewers during Stage 02, alongside the content brief.

**Treating the first revision as minor without assessing impact**

After delivery, a request to update content can appear straightforward but affect accuracy, compliance, or audience assumptions in ways that require a full workflow review. Assess the impact of every change before deciding whether it is a minor correction or a substantive revision.

**Using the framework templates unchanged**

The templates are starting points, not requirements. A content brief that uses every field without considering whether they are relevant for the task will produce documentation that practitioners work around rather than with. Adapt the templates for your context.

---

## 9. References

| Document | Purpose |
|---|---|
| [`master-workflow.md`](master-workflow.md) | Full lifecycle overview — read before anything else |
| [`human-checkpoints.md`](human-checkpoints.md) | The five checkpoints — their scope, authority, and decision criteria |
| [`individual-operating-model.md`](individual-operating-model.md) | How to apply the framework for solo work |
| [`team-operating-model.md`](team-operating-model.md) | How to apply the framework for team tasks |
| [`localisation-workflow.md`](localisation-workflow.md) | Operational guidance for multilingual tasks |
| [`retrospective-guide.md`](retrospective-guide.md) | How to reflect on and improve your use of the framework after a task |
| [`templates/README.md`](templates/README.md) | Index of available templates and when to use each |
| [`stages/02-ideation-and-planning.md`](stages/02-ideation-and-planning.md) | Where the content brief is created — start here for your first task |
