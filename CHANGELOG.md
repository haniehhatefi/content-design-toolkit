# Changelog

All notable changes to this repository are documented here.

The toolkit is organised into six modules, each corresponding to one of the six content
directories. This changelog records the completion of each module and any subsequent
corrections made during quality review.

---

## [1.0.0] — 2026-11-14

Initial release. All six modules completed, reviewed, and approved.

### Added

**Module 1 — Foundations** (`01-foundations/`)
- Voice principles: three core voice attributes (Clear, Human, Helpful) and two
  cross-cutting writing standards (Direct, Consistent), with a tone spectrum and
  worked examples
- Content design principles: seven principles covering clarity, structure, consistency,
  and inclusivity
- Brand voice audit template: a structured template for scoring existing content against
  the voice framework

**Module 2 — UX Writing Standards** (`02-ux-writing-standards/`)
- Microcopy pattern standards for error messages, button labels, empty states,
  confirmations, notifications, and helper text
- Interface component standards for modals, tooltips, inline validation, and onboarding
- Readability standards with a three-tier guidance level framework (Rule, Recommendation,
  Contextual)
- Inclusive language guide covering disability, gender, age, cultural background, and
  technical experience

**Module 3 — AI-Assisted Content Creation** (`03-ai-content-creation/`)
- AI content principles and responsible-use boundaries
- Grounding guide for structuring toolkit standards as LLM context
- Prompt template library: microcopy generation, voice alignment review, and plain
  language rewriting
- Output evaluation rubric with five dimensions and red-flag criteria
- Failure modes documentation with annotated illustrative examples
- Worked examples: three end-to-end annotated cases covering generation, review,
  and rewriting

**Module 4 — AI Content Workflow** (`04-ai-content-workflow/`)
- Six-stage AI content workflow (research and discovery, ideation and planning, content
  creation, review and refinement, localisation and adaptation, delivery and maintenance)
- Five human oversight checkpoints framework (Direction, Alignment, Quality,
  Localisation, Final approval)
- Individual and team operating models
- Localisation workflow with locale-specific review guidance
- Stage documents, templates, and retrospective guide

**Module 5 — Practical Experiments** (`05-practical-experiments/`)
- Five structured experiments applying toolkit methods to constructed content scenarios:
  voice consistency across a content set, grounding comparison, accessibility and
  inclusive language review, localisation readiness, and human-in-the-loop oversight
- Findings and recommendations synthesising cross-cutting observations across all five
  experiments

**Module 6 — Content Quality Evaluation** (`06-content-quality-evaluation/`)
- Quality dimensions framework with thirteen dimensions organised by assessment context
- Evaluation methodology: a step-by-step process for scoping and conducting a quality
  evaluation
- Content audit framework for applying quality criteria to existing content collections
- Quality issue classification taxonomy with identification signals, evidence requirements,
  resolution paths, and checkpoint routing

**Supporting documentation**
- Root README with toolkit overview, structure, navigation, and conventions
- `04-ai-content-workflow/README.md` with module overview and checkpoint summary table
- `LICENSE` (CC BY 4.0, content scope)
- `CONTRIBUTING.md` (portfolio project framing)
- `.gitignore`

### Fixed (Phase 8 audit corrections)

Applied during cross-document consistency review prior to initial release:

- Corrected four broken internal links pointing to an obsolete directory name
  (`04-quality-evaluation` → `06-content-quality-evaluation`)
- Removed six broken links to a non-existent `05-process-templates/` directory;
  rewrote references as plain-text guidance
- Corrected five incorrect relative paths in `localisation-workflow.md`
- Corrected two filename references to `experiment-04-localisation-readiness.md`
- Corrected three broken heading anchors in AI content documents
- Corrected phase number references throughout Phase 6 and Phase 7 documents
  (output evaluation rubric: Phase 3 → Phase 4; human oversight checkpoints:
  Phase 4 → Phase 5)
- Removed stale `Status: Draft` declarations from all nine affected files across
  Phase 6 and Phase 7
- Corrected voice framework terminology in three documents (five voice principles /
  attributes → three voice attributes and two cross-cutting writing standards)
- Broadened workflow role descriptions in two operating-model documents to reflect
  the approved checkpoint scope
- Updated localisation checkpoint terminology in retrospective guide
