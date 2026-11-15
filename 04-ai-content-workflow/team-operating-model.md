# Team Operating Model

How to apply the AI Content Workflow when multiple people are working on a task, or when different contributors carry out different stages.

## Contents

- [1. What this document covers](#1-what-this-document-covers)
- [2. Role distribution across the lifecycle](#2-role-distribution-across-the-lifecycle)
- [3. Checkpoint authority in a team context](#3-checkpoint-authority-in-a-team-context)
- [4. Handoffs between contributors](#4-handoffs-between-contributors)
- [5. Brief ownership and change management](#5-brief-ownership-and-change-management)
- [6. Glossary and terminology management](#6-glossary-and-terminology-management)
- [7. When one person holds multiple roles](#7-when-one-person-holds-multiple-roles)
- [8. References](#8-references)

---

## 1. What this document covers

This document is for teams where multiple people contribute to a task — different practitioners working on different stages, or a lead practitioner working alongside reviewers, approvers, and subject-matter experts. It describes how to distribute responsibilities, structure handoffs, and maintain checkpoint independence across contributors.

It does not replace the stage documents. Each stage document remains the authority on what must be done at that stage, by whom, and to what standard. This document describes how to apply those requirements across a team.

---

## 2. Role distribution across the lifecycle

The framework describes the following types of human involvement across the lifecycle:

| Role | Function | Stage |
|---|---|---|
| Task lead | Responsible for the overall task: owns the brief, coordinates stages, maintains the decision log | Stages 01–06 |
| Practitioner | Creates and iterates on the content | Stages 02–04 (primarily) |
| Direction approver | Confirms the brief and approach | Before AI-assisted work begins |
| Alignment reviewer | Reviews content alignment with brief requirements | Before AI-assisted intermediate outputs advance |
| Quality reviewer | Conducts the Quality checkpoint | Stage 04 |
| Locale reviewer | Conducts Locale approval for each target locale | Stage 05 |
| Final approver | Authorises the content for use | Stage 06 |

These are functional roles, not necessarily separate people. How they are distributed depends on team size, task complexity, and content risk.

**Task lead responsibilities:**
- Create and maintain the content brief
- Confirm approval authority for all checkpoints before AI-assisted work begins
- Maintain the decision and iteration log
- Coordinate handoffs between contributors
- Ensure that checkpoint records are complete and that findings are acted on

---

## 3. Checkpoint authority in a team context

In a team context, checkpoint independence is typically easier to maintain than in solo work, because different people naturally take different roles. However, role distribution alone does not guarantee checkpoint quality.

**Quality review should be independent of content creation wherever practicable.** Where the practitioner must also carry out Quality review, this is permitted only with sufficient time separation and a genuine assessment against the requirements established in the brief. The reviewer must assess the content against those requirements, not against their recollection of creating it. For high-stakes or compliance-sensitive content, an independent reviewer should be arranged wherever possible.

**The same applies to Locale approval.** The locale reviewer who translates the content cannot assess their own translation at the Locale approval checkpoint. Where the reviewer is also the translator, a separate qualified practitioner must carry out Steps 5–7 of the localisation workflow. See [`localisation-workflow.md`](localisation-workflow.md).

**Final approval is a distinct decision from Quality review.** Final approval is not a re-confirmation of the Quality review. It is an independent authorisation that the content is ready for use — taking into account all prior reviews, any outstanding non-blocking issues, and the content's current state. Final approval requires the authority to authorise the deliverable, not only the expertise to assess its quality.

**Checkpoint records must be completed by the person who carried out the checkpoint**, not by the task lead retrospectively. The record is a governance document that reflects the checkpoint as it was actually carried out.

---

## 4. Handoffs between contributors

When one contributor passes work to the next, the handoff is a governance event. Its purpose is to transfer not only the content but the context — the decisions made, the requirements in force, and the outstanding issues the next contributor needs to be aware of.

Use [`templates/handoff-template.md`](templates/handoff-template.md) as the basis for every stage-to-stage handoff where different people carry out different stages. For multilingual tasks, the handoff from Quality review (Stage 04) to localisation (Stage 05) is particularly important — the locale reviewer needs to understand what the Quality review found and what source content changes, if any, occurred after the review.

**Before a handoff:**
- Confirm that the checkpoint for the outgoing stage has been completed and recorded
- Complete the handoff template before the recipient starts work — not as a summary after they have already begun
- Identify any outstanding issues and ensure they are documented in both the handoff and the decision log

**After a handoff:**
- The recipient confirms they have received all materials listed in the handoff
- If the recipient identifies a gap — missing materials, an unresolved question that blocks their work — they raise it before proceeding rather than after completing their stage

A handoff template completed after the recipient has already started work does not serve its governance function. The purpose of the handoff is to establish a clean transfer of responsibility, not to document what was already done.

---

## 5. Brief ownership and change management

The content brief is the governing document for the full workflow. Changes to the brief after Stage 03 begins affect all contributors and all subsequent stages.

**Brief ownership:**
- The task lead owns the brief and is responsible for keeping it current
- Changes to the brief must be communicated to all contributors who may be affected
- Changes made after Stage 03 begins must be recorded in the decision and iteration log, with the rationale and the stages or contributors affected

**What constitutes a change to the brief:**
- Changes to audience definition, objectives, or scope
- Changes to mandatory requirements or AI use constraints
- Changes to approval authority
- Changes to the glossary that affect content already created

**Implications of brief changes for active work:**
- If the change affects content already created or reviewed, that content must be assessed for whether it still meets the revised requirements
- If the change affects the standard that a checkpoint assessed against, the checkpoint record should note the change
- If the change is substantive, returning to the affected stage may be required — assess using the revision-routing table in [`stages/06-delivery-and-maintenance.md`](stages/06-delivery-and-maintenance.md)

---

## 6. Glossary and terminology management

For team tasks, the glossary established in the content brief is the shared reference for all contributors. Inconsistent terminology across a team is a common source of Quality review findings and localisation errors.

**Glossary discipline for teams:**
- The glossary owner (typically the task lead) maintains the approved terminology and approved translations
- Practitioners refer to the glossary before making terminology decisions during Stage 03
- When a practitioner encounters a term not in the glossary and makes a decision, they record it in the decision log and flag it for the glossary owner to approve
- The glossary must be complete and accurate before localisation begins — Stage 05 depends on it

**For multilingual tasks:**
- Approved translations must be established for key terms before translation begins
- Where a locale reviewer proposes a different translation from the approved one, the change must be recorded in the decision log and confirmed with the glossary owner before it is applied consistently
- Terminology consistency across locales is a Quality review and Locale approval finding — it is not resolved by each locale working independently

---

## 7. When one person holds multiple roles

Team structure does not always map cleanly onto the framework's role types. In practice, the same person may hold more than one role for a given task.

**Permitted consolidations:**
- Task lead and practitioner — common in smaller teams; the lead takes responsibility for creation and coordination
- Direction approver and Alignment reviewer — the same person may carry out both checkpoints
- Quality reviewer and Final approver — permitted, but requires explicit separation between the two decisions; the Final approver must make an independent authorisation decision, not simply re-confirm the Quality review

**Consolidations that require care:**
- Practitioner and Quality reviewer — permitted if sufficient time separation is built in; the reviewer must assess the content against the brief requirements, not against their recollection of creating it
- Task lead and Final approver — permitted; the task lead who also gives Final approval must make a genuine independent decision, not a formality

**Consolidations that are not permitted:**
- Translator and Locale approver for the same locale — the person who translates the content cannot assess their own translation at the Locale approval checkpoint; a separate qualified practitioner must carry out Steps 5–7
- AI and any checkpoint role — no checkpoint can be passed by AI assessment alone; each requires a qualified human decision

Where one person holds multiple checkpoint roles, document this in the content brief. It does not change the requirements for each checkpoint, but makes the authority structure explicit for anyone reviewing the content's approval history.

---

## 8. References

| Document | Purpose |
|---|---|
| [`master-workflow.md`](master-workflow.md) | Full lifecycle overview |
| [`human-checkpoints.md`](human-checkpoints.md) | The five checkpoints — scope, authority, and decision criteria |
| [`implementation-guide.md`](implementation-guide.md) | Setup and first-task guidance |
| [`localisation-workflow.md`](localisation-workflow.md) | Localisation guidance, including locale reviewer separation requirements |
| [`templates/handoff-template.md`](templates/handoff-template.md) | Handoff template for stage-to-stage transfers |
| [`templates/content-brief-template.md`](templates/content-brief-template.md) | Content brief template |
| [`templates/decision-and-iteration-log.md`](templates/decision-and-iteration-log.md) | Decision log template |
