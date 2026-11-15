# Content principles

Content principles are broader than voice. Where voice describes *how content sounds*, content principles describe *how content is designed* — the structural and strategic decisions that make content work for the people who need it.

These six principles apply across any digital product, regardless of brand, industry, or format.

---

## 1. Start with what the reader needs to do

Design content around the reader's task, not the organisation's structure or the system's logic.

Before writing, ask: *What is the reader trying to accomplish? What do they need to know to do it?* Everything else — explanations, context, caveats — comes after the core task is served.

**In practice:**
- Put the most important information first, before any context or qualification
- Structure help documentation around tasks, not features
- Write error messages from the reader's perspective (*you*), not the system's perspective

**Illustrative example** *(Demonstrates the principle. Replace bracketed placeholders with your own context.)*

| Perspective | Example |
|---|---|
| Organisation's structure | *"The [product name] system supports a range of file formats including PDF, DOCX, and XLSX."* |
| Reader's task | *"You can upload PDF, Word, and Excel files."* |

**Real-world example:** GOV.UK's design principles lead with "Start with user needs." Their guidance notes: "If you don't know what the user needs, you won't build the right thing. Do research, analyse data, talk to users." *(Source: [GOV.UK Design Principles](https://www.gov.uk/guidance/government-design-principles), accessed 2024)*

---

## 2. Write less

Every additional word raises the cost of reading. Remove anything that does not serve the reader's task or change their understanding.

This is not about being terse — it is about being precise. A long, well-written explanation can be leaner than a short, vague one.

**In practice:**
- Cut throat-clearing: opening sentences that restate what the reader already knows
- Remove softeners that add no meaning: *simply*, *just*, *easily*, *please note that*
- One idea per sentence, one purpose per paragraph
- If you can say it in one sentence, do not use two

**Common targets for removal:**

| Type | Before | After |
|---|---|---|
| Throat-clearing | *"Before proceeding, please take a moment to review the following information."* | *(Remove entirely; show the information directly)* |
| Redundant softener | *"You can simply click the button to continue."* | *"Select Continue."* |
| Nominalisation | *"The process of deletion"* | *"Deleting"* |
| Weak passive | *"Your file has been saved by the system."* | *"Your file has been saved."* |

---

## 3. Use the reader's language

Write using the words the reader uses to describe their own situation. Avoid internal jargon, technical terminology, and business language that the reader would not use themselves.

**In practice:**
- Use the words the reader would use to describe their task in a support ticket
- When technical terms are necessary, define them once where they first appear
- Run vocabulary decisions past people outside the team — the word that is obvious internally may be opaque externally

**Testing vocabulary:** Ask someone outside the team: *"What would you call this action?"* or *"What would you do if you saw this word in an error message?"* Where they are uncertain or give a different answer, the vocabulary needs attention.

**Illustrative examples** *(Demonstrates the principle.)*

| Internal term | Reader's term |
|---|---|
| *"Authenticate your credentials"* | *"Sign in"* |
| *"Your session token has expired"* | *"You were logged out"* |
| *"Initiate the submission workflow"* | *"Send your [item]"* |

---

## 4. Be consistent, then improve

Consistency takes priority over local optimisation. A mediocre but consistent term is more usable than a mixture of technically superior alternatives.

If a term is already in use across a product, the bar for changing it is high — the disruption of inconsistency often outweighs the benefit of a better word.

**In practice:**
- Establish a shared glossary before writing at scale (a simple document listing preferred terms, variants to retire, and decision rationale)
- Change terms deliberately, with a migration plan, not incrementally across individual screens
- When in doubt, use the term that is already in the most user-facing context (the most prominent button, the most-visited screen)

**When a product is new:** If terms haven't solidified yet, the corollary applies — *decide terms early, before they proliferate*. Retrofitting consistency is costly. Start a terminology glossary from the beginning — it is much harder to retrofit consistency after terms have proliferated.

---

## 5. Make every state readable

A product that works perfectly is easy to write for. Write for every state: the empty state, the error state, the loading state, the edge case, the timeout, and the first use.

These states are often written last and given least attention, but they appear at moments of highest user uncertainty and therefore carry the most weight.

**States that commonly go unwritten (or are written as afterthoughts):**
- Empty states: first use, cleared, filtered to zero
- Error states: form validation, server error, connection failure, file type or size error, rate limit
- Loading and waiting states
- Session expiry, timeout, permission denied, insufficient privileges
- Completion states for significant milestones
- Offline or low-connectivity states

**A practical check:** Before completing a content design pass on any flow, list every state the user could encounter. Mark each as *written*, *draft*, or *missing*. Write the missing ones before the pass is complete.

---

## 6. Test your content, not just your design

Content assumptions are design assumptions. The words on a button, the instructions in a form, the labels in a navigation — these are hypotheses about what the reader will understand and act on. Test them.

**Lightweight testing methods:**

| Method | How it works | What it reveals |
|---|---|---|
| **5-second test** | Show a screen for 5 seconds. Ask: *"What is this for? What can you do here?"* | Whether key content is landing |
| **Cloze test** | Remove key words from a text. Ask readers to fill them in. | Vocabulary gaps between writer and reader |
| **Think-aloud test** | Ask someone to complete a task while narrating their thoughts. | Where content causes pauses, re-reads, or questions |
| **Preference test** | Show two versions side by side. Ask which feels more [attribute]. | Which version matches your intended voice |

**What to do with findings:** Document them. A content change made because *it tested better* is more persuasive to stakeholders than a change made because *it sounds better*. Keep records of tests, findings, and resulting changes alongside your content — a simple before and after record noting the original wording, the revision, and the reason is sufficient.

---

## 7. Write inclusively

Language that excludes people undermines everything else in this module. Write in a way that includes the full range of people who might use your product, regardless of gender, age, cultural background, ability, or technical experience.

This principle establishes the foundation. Practical guidance — specific patterns, checks, and examples — is in [Module 2: Inclusive language guide](../02-ux-writing-standards/inclusive-language-guide.md).

**In practice:**
- Use gender-neutral language by default: *they/them* as singular pronouns, *the user* not *he* or *she*
- Avoid idioms, metaphors, and colloquialisms that do not translate across languages or cultures
- Do not assume physical or cognitive ability: avoid *simply click*, *you can see*, *just tap*
- Write for a range of reading levels — aim for clarity at plain language standard (see [readability standards](../02-ux-writing-standards/readability-standards.md)), while not dumbing down content for expert users
- Avoid cultural defaults: dates, formats, units, and examples that only make sense in one context

**A practical check:** Before publishing content, ask: *Does this make sense to someone who is not like me?* The answer requires testing, not assumption — but asking the question is the starting point.

---

## Related documents

- [Voice principles](voice-principles.md) — The attributes that define how content sounds
- [Tone spectrum](tone-spectrum.md) — How principles express differently across contexts
- [Module 2 — UX Writing Standards](../02-ux-writing-standards/README.md) — These principles applied to specific patterns
