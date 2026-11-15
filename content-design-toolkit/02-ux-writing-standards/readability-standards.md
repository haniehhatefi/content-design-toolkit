# Readability standards

Readability describes how easy content is to read and understand. These standards help content designers make consistent decisions about sentence length, vocabulary, and structure — and give them a measurable baseline to track over time.

Readability is not the same as simplicity. The goal is not to remove all complexity from content, but to remove unnecessary complexity that makes content harder than it needs to be.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Readability scoring

The most widely used tool for measuring readability in English is the Flesch-Kincaid Grade Level formula, which calculates an approximate US school grade level based on average sentence length and average syllable count per word.

**How to interpret the score:**

| Flesch-Kincaid Grade Level | Approximate reading age | Appropriate for |
|---|---|---|
| Grade 5–6 | 10–11 years | Consumer-facing mobile apps, simple onboarding, mass-market products |
| Grade 7–8 | 12–13 years | General consumer web products, government services, most SaaS products |
| Grade 9–10 | 14–15 years | Professional tools, B2B products, technical documentation (non-specialist) |
| Grade 11–12 | 16–17 years | Specialist professional content, some regulated industries |
| Grade 13+ | University | Highly technical documentation, academic, legal |

**Recommended targets by content type:**

| Content type | Target grade level |
|---|---|
| Error messages | Grade 6–7 |
| Onboarding and welcome screens | Grade 6–7 |
| Form helper text | Grade 7–8 |
| In-product notifications | Grade 7–8 |
| In-product help documentation | Grade 8–9 |
| Technical documentation (developer or admin) | Grade 9–11 |

These are targets, not strict rules. Content that scores one or two grades above the target is not necessarily a problem. Content that consistently scores 3–4 grades above the target for its type warrants review.

---

## Tools for measuring readability

| Tool | Type | Access |
|---|---|---|
| Hemingway Editor | Web / desktop app | [hemingwayapp.com](https://hemingwayapp.com) |
| Readable | Web tool | [readable.com](https://readable.com) |
| Microsoft Word | Built-in (Flesch-Kincaid) | Review → Check Document |
| Grammarly | Integrated editor | Various integrations |
| Custom script (Python) | Automated | Use `textstat` library: `textstat.flesch_kincaid_grade(text)` |

For bulk content audits, automating readability scoring with a script is more efficient than measuring manually. See the [brand voice audit template](../01-foundations/brand-voice-audit-template.md) for how to integrate scores into an audit.

---

## Rules

**`Rule`** Error messages and microcopy in high-stress moments (account recovery, payment failure) must target Grade 6–7. This is not about dumbing down — it is about reducing cognitive load at the moments when users have the least capacity.

**`Rule`** Readability scores are a diagnostic tool, not a substitute for human judgement. A sentence can score Grade 6 and still be confusing; a sentence can score Grade 11 and still be the right choice for its expert audience. Use scores alongside manual review, not instead of it.

---

## Recommendations

**`Rec`** Aim for an average sentence length of 15–20 words for most product copy. Sentences over 25 words consistently increase reading difficulty.

**`Rec`** Use active voice by default. Passive constructions increase sentence complexity without adding meaning.

> ❌ "Your account has been successfully created by the system." (passive, 10 words, complex)
> ✅ "Your account is ready." (active, 4 words, clear)

**`Rec`** Prefer concrete verbs over abstract nouns (nominalisations).

| Nominalisation | Preferred |
|---|---|
| "Make a decision" | "Decide" |
| "Provide an explanation" | "Explain" |
| "Have a discussion" | "Discuss" |
| "Give consideration to" | "Consider" |

**`Rec`** Use a readability check as part of the content review process — not as the final gate, but as one signal alongside peer review and user testing.

---

## Contextual decisions

**`C`** The right readability target depends on the product's audience. A consumer fintech product serving a broad demographic should target Grade 6–7 for most copy. A developer API documentation site serving professional engineers can comfortably target Grade 10–11 for technical content. Know your audience before setting targets.

**`C`** Legal or regulatory content may need to maintain specific language for compliance reasons. In these cases, readability scores will be higher. Consider whether a plain-language summary can be offered alongside the required text.

**`C`** For products that support multiple languages, readability scoring should be applied to each language independently — Flesch-Kincaid is calibrated for English and will give unreliable results for other languages. Use language-specific tools for non-English content.

---

## Common readability problems

| Problem | Example | Revision |
|---|---|---|
| Sentence too long | "In order to successfully complete the registration process, please ensure that all required fields in the form below have been filled in with accurate and up-to-date information." | "Fill in all the required fields to register." |
| Nominalisation chain | "The utilisation of the available functionality will result in an improvement of outcomes." | "Using this feature improves your results." |
| Unnecessary passive | "Errors have been detected in your submission." | "We found some errors in your submission." |
| Jargon without definition | "Please authenticate using your SSO credentials." | "Sign in using your company email." |
| Double negatives | "This action cannot be undone unless you have not yet confirmed it." | "You can undo this until you confirm it." |

---

## Related documents

- [Brand voice audit template](../01-foundations/brand-voice-audit-template.md) — For integrating readability scores into a systematic content audit
- [Inclusive language guide](inclusive-language-guide.md) — For plain language as part of inclusive writing
- [Module 6 — Content Quality Evaluation](../06-content-quality-evaluation/README.md) — For using readability as one dimension of a content quality rubric
