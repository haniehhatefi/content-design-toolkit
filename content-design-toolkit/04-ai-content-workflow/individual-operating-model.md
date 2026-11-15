# Individual Operating Model

How to apply the AI Content Workflow when you are working alone on a task, or when you are the primary practitioner responsible for most stages.

## Contents

- [1. What this document covers](#1-what-this-document-covers)
- [2. Role consolidation in solo work](#2-role-consolidation-in-solo-work)
- [3. Maintaining checkpoint independence](#3-maintaining-checkpoint-independence)
- [4. Documentation approach for solo tasks](#4-documentation-approach-for-solo-tasks)
- [5. When to bring in external input](#5-when-to-bring-in-external-input)
- [6. Adapting the framework for lower-risk tasks](#6-adapting-the-framework-for-lower-risk-tasks)
- [7. References](#7-references)

---

## 1. What this document covers

This document is for practitioners working alone on a task — carrying out both the AI-assisted activities and the human responsibilities described in each stage document. It describes how to structure solo use of the framework, how to maintain the checkpoint disciplines when no other person is involved, and how to calibrate documentation effort for lower-risk tasks.

It does not replace the stage documents. Each stage document remains the authority on what must be done at that stage, by whom, and to what standard. This document describes how to apply those requirements in a solo context.

---

## 2. Role consolidation in solo work

The framework describes five types of human decision-making across the lifecycle:

| Role | Function |
|---|---|
| Practitioner | Creates and iterates on the content |
| Direction approver | Confirms the brief and approach before AI-assisted work begins |
| Alignment reviewer | Reviews content alignment with brief requirements before AI-assisted intermediate outputs advance |
| Quality reviewer | Conducts the Quality checkpoint at Stage 04 |
| Final approver | Authorises the content for use at Stage 06 |

For multilingual tasks, Locale approval (Stage 05) requires a qualified locale reviewer for each target locale. This role cannot be consolidated with the practitioner role when the practitioner is also producing the translation — see [Section 5](#5-when-to-bring-in-external-input) and [`localisation-workflow.md`](localisation-workflow.md).

For non-localisation roles, a single practitioner may hold all five in a solo task. This is a practical concession to context, not a weakening of the checkpoint structure. When one person holds all roles, checkpoint quality depends on the discipline the practitioner applies to each one.

---

## 3. Maintaining checkpoint independence

Checkpoints lose their governance value if the person who created the content reviews it immediately as the same person. The purpose of a checkpoint is to assess the content against requirements — not to approve work already done.

**Build in time separation.** Complete the content, then step away from it before reviewing it at a checkpoint. As a practical measure, reviewing content after a break of at least several hours — the following morning, if feasible — tends to produce a more independent assessment than reviewing it immediately after finishing.

**Review against the brief, not against the content.** At each checkpoint, start with the requirements established in the content brief, not with the content you just produced. Ask whether the content meets the requirements — not whether the requirements match what you wrote.

**Complete the checkpoint record before continuing.** Document your findings and decision before moving to the next stage. A checkpoint record completed retrospectively, after subsequent work has been done, is less reliable than one completed at the time.

**Keep the checkpoint record separate from working notes.** The decision and iteration log is a governance record. Notes made while creating the content are working notes. Keep them separate.

**Apply the same standard regardless of time pressure.** The discipline of a checkpoint is most important when you are under time pressure — that is precisely when errors are most likely to occur and most likely to go undetected.

---

## 4. Documentation approach for solo tasks

Documentation level should reflect the risk and complexity of the task. The table below describes appropriate documentation for three task types. These are starting points, not requirements — apply judgement.

| Task type | Content brief | Decision log | Checkpoint records |
|---|---|---|---|
| **Straightforward, lower-risk** (e.g. short UI copy, internal notes) | Condensed — audience, objective, approval authority, and AI use constraints | Minimal — record decisions with implications for review or localisation | Brief — confirm checkpoint passed, note any findings that affect the next stage |
| **Moderate complexity** (e.g. onboarding flows, feature announcements) | Full brief — all relevant fields | Active — record decisions, checkpoint outcomes, and any revision routing | Full — findings, outcome, and rationale for any decisions at each checkpoint |
| **High-stakes, compliance-sensitive, or broad audience** (e.g. safety content, legal-adjacent copy, public-facing communications) | Full brief, with particular attention to requirements and AI use constraints | Detailed — full audit trail including decisions at every stage | Thorough — mandatory requirements listed, findings documented, rationale for any carried-forward issues |

For all task types, the following are not adaptable to task complexity:

- All applicable checkpoint types must occur and must be carried out by a qualified person
- Mandatory requirements established in the brief must be met before Quality review passes
- Phase 4 AI use exclusions apply regardless of task risk level
- Only Final approval may explicitly accept outstanding non-blocking issues as exceptions

---

## 5. When to bring in external input

Solo work does not mean operating in isolation. The following situations warrant bringing in a second person even when you are the primary practitioner.

**High-stakes or compliance-sensitive content.** Where the content has legal, regulatory, clinical, or safety implications, a second reviewer for the Quality checkpoint is strongly recommended. Subject-matter expert input may also be required.

**Broad audience or public-facing content.** Content that will reach a large or diverse audience is more likely to contain assumptions about the audience that the practitioner cannot reliably assess from their own perspective alone.

**Unfamiliar content domain.** If you are creating content in a domain where your knowledge is limited — a technical product, a regulated industry, an unfamiliar cultural context — input from a qualified reviewer at Quality review is valuable.

**Localisation.** When the task requires localisation and you will also produce the translation, you must arrange a separate qualified practitioner to carry out Steps 5–7 of the localisation workflow: reviewing and adapting the draft, conducting the substantive locale assessment, and making the Locale approval decision. The person who produced the translation cannot assess their own work at the Locale approval checkpoint. Confirm this arrangement before localisation begins. See [`localisation-workflow.md`](localisation-workflow.md).

**When you are uncertain.** A persistent doubt about the content that cannot be resolved through the brief requirements and your own assessment is a signal that a second perspective would be valuable.

---

## 6. Adapting the framework for lower-risk tasks

The framework is designed to scale. Not every content task warrants the same documentation effort or the same checkpoint rigour.

**What you can adapt:**
- The length and depth of the content brief — a short, low-risk task may need only a condensed brief
- The level of documentation in the decision log — lower-risk tasks can use lighter records
- The format of checkpoint records — a brief checkpoint note is sufficient where the full structured format would be disproportionate to the task

**What you must not adapt:**
- Whether checkpoints occur — all checkpoint types must occur for tasks where they apply
- Who carries out checkpoints — the same person cannot both create content and immediately pass it without a genuine assessment
- The exception acceptance rules — only Final approval may accept outstanding non-blocking issues
- The Phase 4 AI use exclusions — these apply to all tasks regardless of risk level

A simple test for calibrating documentation effort: match it to the reversibility of the content. Content that is difficult to revise after delivery — legal, public-facing, safety-critical — warrants more thorough records than content that can be corrected quickly if an error is found.

---

## 7. References

| Document | Purpose |
|---|---|
| [`master-workflow.md`](master-workflow.md) | Full lifecycle overview |
| [`human-checkpoints.md`](human-checkpoints.md) | The five checkpoints — scope, authority, and decision criteria |
| [`implementation-guide.md`](implementation-guide.md) | Setup and first-task guidance |
| [`localisation-workflow.md`](localisation-workflow.md) | Localisation guidance, including solo-task locale reviewer requirements |
| [`templates/content-brief-template.md`](templates/content-brief-template.md) | Content brief template |
| [`templates/decision-and-iteration-log.md`](templates/decision-and-iteration-log.md) | Decision log template |
