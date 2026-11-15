# Practical Experiments

Structured experiments applying the Content Design Toolkit's methods to constructed content-design scenarios.

## Contents

- [1. Purpose](#1-purpose)
- [2. Relationship to earlier phases](#2-relationship-to-earlier-phases)
- [3. Methodology and conventions](#3-methodology-and-conventions)
- [4. What these experiments can and cannot claim](#4-what-these-experiments-can-and-cannot-claim)
- [5. Experiment selection](#5-experiment-selection)
- [6. How experiments are structured](#6-how-experiments-are-structured)
- [7. Scenarios](#7-scenarios)
- [8. File index](#8-file-index)

---

## 1. Purpose

Phases 2–5 of this toolkit establish principles, standards, AI content practices, and a workflow framework. Phase 6 puts those elements into practice through documented experiments.

The purpose is not to showcase polished AI outputs. It is to show how the toolkit's methods are applied, what they reveal when applied to constructed content problems, and where human judgement is required. Each experiment is designed to demonstrate the method in action — including cases where AI output requires significant revision, fails to meet a standard, or cannot be evaluated without domain-specific expertise.

These experiments are intended to be read alongside the toolkit phases they draw on, not as standalone demonstrations.

---

## 2. Relationship to earlier phases

Each experiment applies methods from one or more earlier phases. The relevant phase documents should be read before the experiment that depends on them.

| Phase | Coverage | Relevant to |
|---|---|---|
| Phase 2 | Voice and tone principles | Experiments 01, 02 |
| Phase 3 | UX writing standards, accessibility, and inclusive language | Experiments 01, 03 |
| Phase 4 | AI content creation: prompting, grounding, and output evaluation | Experiments 01, 02 |
| Phase 5 | AI content workflow: lifecycle stages, checkpoints, and localisation | Experiments 04, 05 |

Phase 4's `worked-examples.md` demonstrates individual AI-assisted tasks — generating microcopy, reviewing voice alignment, revising content to address a quality finding. These experiments apply the same methods under more demanding or complex conditions: across a content set, under different grounding conditions, through the full workflow lifecycle, and against accessibility and localisation standards that require human expertise.

---

## 3. Methodology and conventions

**Illustrative outputs**

The AI outputs shown in these experiments are illustrative. They are constructed to demonstrate specific aspects of a method — how a grounding gap produces unsupported assumptions, how an accessibility issue presents in AI-generated content, how a checkpoint finding changes the direction of a task. They are not actual outputs captured from recorded model runs.

This convention is stated explicitly in each experiment. Where an output has been constructed to include a deliberate weakness — to make a specific evaluation challenge visible — this is noted at the point it appears.

**Why illustrative rather than empirical**

Using actual AI outputs would introduce variability across model versions, prompts, and run conditions. This portfolio-based demonstration format does not attempt to control or measure those variables. Constructed illustrative examples therefore provide a more appropriate way to demonstrate the application of the toolkit's methods without implying empirical findings.

This convention is consistent with Phase 4's established approach.

**Labelling**

Illustrative outputs are labelled: *Illustrative output — constructed to demonstrate [specific aspect].* Where a deliberate weakness has been introduced, the label states this. Evaluation commentary follows the output and applies the toolkit's methods to it in full.

---

## 4. What these experiments can and cannot claim

**What they can demonstrate:**

- How to apply a specific toolkit method to a content problem
- What a method identifies when applied to content with known characteristics
- Where human judgement, expertise, or accountability remains necessary beyond AI-assisted analysis and recommendations
- How a revision or intervention changes the content in relation to a specific standard
- What decisions a practitioner needs to make at each stage

**What they cannot claim:**

- That an AI system would actually produce a given output under equivalent conditions
- That grounding, revision, or human review *caused* a measurable improvement in AI output quality
- That findings generalise to other models, contexts, or content types
- That content meeting the toolkit's standards is free of all errors or risks

Where an experiment describes a comparison — grounded versus underspecified generation, before and after revision, source versus locale-adapted content — the comparison documents the method's application to two illustrative cases. It does not constitute experimental evidence of the method's effectiveness.

---

## 5. Experiment selection

Five experiments were selected on the basis that each applies a toolkit capability to conditions Phase 4's worked examples do not already cover.

| Experiment | Research question | Phase(s) drawn on |
|---|---|---|
| [01 — Voice consistency](experiment-01-voice-consistency.md) | How does voice consistency break down across a content set, and what changes in alignment are observable following human-guided revision? | 2, 3, 4 |
| [02 — Grounding comparison](experiment-02-grounding-comparison.md) | How do outputs differ between equivalent tasks with different levels of grounding specification? | 4 |
| [03 — Accessibility and inclusive language](experiment-03-accessibility-and-inclusion.md) | Does AI-generated content meet Phase 3 accessibility and inclusion standards without human intervention? | 3 |
| [04 — Localisation readiness and adaptation](experiment-04-localisation-readiness.md) | How well does structured source content and localisation guidance support adaptation across languages and cultural contexts? | 5 |
| [05 — Human-in-the-loop workflow](experiment-05-human-in-the-loop.md) | What decisions, interventions, and revisions occur when a content task is developed through the six lifecycle stages and five human oversight checkpoints? | 5 |

Experiments 01–03 apply individual content capabilities to more demanding conditions than Phase 4's worked examples cover. Experiments 04 and 05 apply Phase 5's operational framework — the localisation workflow and the full six-stage lifecycle — to a realistic content scenario.

---

## 6. How experiments are structured

Each experiment follows a consistent format, though the methodology within each section reflects the specific scenario being examined.

| Section | Content |
|---|---|
| **Research question** | What the experiment is trying to find out |
| **Hypothesis** | What is expected to happen and why |
| **Test scenario** | The content task being used as the basis for the experiment |
| **Materials** | Which toolkit documents, templates, and evaluation criteria are applied |
| **Procedure** | How the illustrative case is constructed, examined, and evaluated, step by step |
| **Observations** | What the application of the method identifies, including deliberate weaknesses, evaluation findings, and human intervention points |
| **Evaluation** | How the observations are assessed against the applicable criteria, and what conclusions can be drawn within the stated limitations |
| **Limitations** | What cannot be concluded from this experiment |
| **Recommendations** | Implications for the toolkit |

The experiment format is designed to make each one legible as a self-contained record. A reader who has not followed the full toolkit development should be able to read an experiment, understand what was being examined, follow the procedure, and evaluate the findings.

---

## 7. Scenarios

Each experiment uses a distinct, generic illustrative scenario. No fictional brand, product, or user journey is used across the full experiment set.

Scenarios are introduced with only the context needed to make the experiment meaningful. Where placeholder content is used, it is clearly marked: `[action]`, `[item]`, `[next step]`, `[product category]`. Where specific content is needed for evaluation purposes — to demonstrate a voice inconsistency, an accessibility issue, or a localisation challenge — the content is introduced at that point in the experiment and labelled as illustrative.

This keeps the experiments reusable as references and consistent with the toolkit's product-agnostic identity.

---

## 8. File index

| File | Purpose |
|---|---|
| `README.md` | This document — purpose, methodology, and conventions |
| [`experiment-01-voice-consistency.md`](experiment-01-voice-consistency.md) | Voice consistency across a content set, with human-guided revision |
| [`experiment-02-grounding-comparison.md`](experiment-02-grounding-comparison.md) | Grounded versus underspecified generation comparison |
| [`experiment-03-accessibility-and-inclusion.md`](experiment-03-accessibility-and-inclusion.md) | Accessibility and inclusive language review of AI-generated content |
| [`experiment-04-localisation-readiness.md`](experiment-04-localisation-readiness.md) | Localisation readiness and cultural adaptation |
| [`experiment-05-human-in-the-loop.md`](experiment-05-human-in-the-loop.md) | Full workflow lifecycle with five oversight checkpoints |
| [`findings-and-recommendations.md`](findings-and-recommendations.md) | Consolidated findings, limitations, and toolkit improvement recommendations |
