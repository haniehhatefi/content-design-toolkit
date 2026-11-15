# Voice principles

Your product's voice is the consistent personality expressed through its words. Unlike tone, which changes with context, voice stays stable — it is recognisable in a button label, an error message, an empty state, and a confirmation email.

This document defines three core voice attributes and two cross-cutting writing standards that support them.

---

## How to use this document

**If you are establishing voice principles for a new product:** Use these attributes as a starting point and adapt them to your context. Each attribute includes prompts to help you define what it means for your product specifically.

**If you are auditing existing content:** Use the descriptions and examples to identify where your content is on-voice and where it drifts. The [brand voice audit template](brand-voice-audit-template.md) gives you a structured process for this.

**If you are writing new content:** Return to these attributes before drafting. Ask: does this feel [attribute]? Then apply each of the three in turn.

---

## Three core voice attributes

### 1. Clear

**Definition:** Content that prioritises understanding over cleverness. It says the most important thing first, uses familiar words, and removes anything that makes the reader work harder than the task requires.

**What it means in practice:**
- Use the word a reader would use, not the word an engineer or marketer would use
- Front-load information: the most important point first, qualification after
- One idea per sentence where possible
- Avoid nominalisations: *submit* not *submission*, *confirm* not *confirmation*

**What it does not mean:**
- Simple to the point of being condescending
- Always short — some content requires detail; clear detail is still clear
- Avoiding technical terms when the reader knows them and expects them

**Illustrative examples** *(These examples demonstrate the principle. Replace bracketed placeholders with your own context.)*

| Situation | Unclear | Clear |
|---|---|---|
| Form submission error | "An error has occurred during the processing of your submission." | "Something went wrong. Check your connection and try again." |
| Button confirming deletion | "Execute deletion protocol" | "Delete [item]" |
| Search with no results | "Your query returned no results at this time." | "No results for '[search term]'. Try a different word or phrase." |

---

### 2. Human

**Definition:** Content that sounds like a person wrote it for a person. It acknowledges the reader's situation, uses natural language, and avoids the mechanical patterns that make digital products feel impersonal.

**What it means in practice:**
- Write in second person: *you*, *your*
- Use contractions where they sound natural: *you're* not *you are*, *we'll* not *we will*
- Acknowledge effort or difficulty when it is real, without being performative
- Avoid passive voice where possible: *we sent your receipt* not *your receipt has been sent*

**What it does not mean:**
- Informal to the point of inconsistency
- Forced friendliness that doesn't match the seriousness of the situation
- Overusing the reader's name or personal details

**Illustrative examples** *(These examples demonstrate the principle. Replace bracketed placeholders with your own context.)*

| Situation | Mechanical | Human |
|---|---|---|
| Account created | "Account creation process has been completed successfully." | "You're in. We've set up your account." |
| Waiting for a process | "Processing request. Please stand by." | "Hang on — this usually takes about 30 seconds." |
| Session expired | "Authentication token has expired. Re-authentication required." | "You were away for a while. Sign in again to continue." |

**Real-world example:** GOV.UK writes in second person and uses contractions throughout its guidance. For example, its guidance on renewing a driving licence uses "You need to renew your licence" rather than "Licence renewal is required." *(Source: [GOV.UK, Renew your driving licence](https://www.gov.uk/renew-driving-licence), accessed 2024)*

---

### 3. Helpful

**Definition:** Content that anticipates the reader's next question and answers it, or points them to where they can answer it themselves. Helpful content reduces friction — it does not just describe it.

**What it means in practice:**
- Error messages say what went wrong *and* what to do next
- Confirmations say what happens next, not only what has happened
- Warnings include the consequence, not just the warning
- Empty states offer a path forward

**What it does not mean:**
- Piling on information the reader did not ask for
- Over-explaining steps a confident user does not need
- Treating the reader as if they cannot understand context

**Illustrative examples** *(These examples demonstrate the principle. Replace bracketed placeholders with your own context.)*

| Situation | Unhelpful | Helpful |
|---|---|---|
| Password requirements not met | "Password does not meet requirements." | "Your password needs at least 8 characters and one number." |
| File upload failed | "Upload failed." | "That file is too large. The maximum size is [size]." |
| Task completed | "[Action] complete." | "[Action] complete. Your [item] is now available in [location]." |
| Destructive action warning | "Are you sure you want to delete?" | "This will permanently delete [item]. You can't undo this." |

---

## Cross-cutting writing standards

These two standards apply across all three voice attributes. They are quality requirements, not attributes in themselves — they describe how to execute voice consistently.

### Direct

Directness is an expression of clarity. Direct content makes a clear point without hedging, over-apologising, or using filler words.

**Apply this standard by:**
- Using imperative verbs for instructions: *Save*, *Continue*, *Choose* — not *You may want to save*
- Removing unnecessary softeners: *simply*, *just*, *easily*, *quickly*
- Acknowledging problems clearly rather than burying them in caveats
- Getting to the point without a preamble sentence

**Directness is compatible with warmth.** Being direct does not mean being cold — it means respecting the reader's time. When a situation genuinely calls for empathy (delivering difficult news, acknowledging significant data loss), use direct language that is also considerate in tone.

### Consistent

Consistency is a quality-control requirement. Content that uses the same words for the same things builds trust and reduces cognitive load.

**Apply this standard by:**
- Establishing one term per concept and using it across all touchpoints: UI copy, notifications, emails, and documentation
- Applying a single capitalisation convention: sentence case for UI copy unless a proper noun
- Applying consistent punctuation: headings without full stops, button labels without punctuation
- Maintaining a glossary so decisions do not have to be remade

Consistency takes priority over local optimisation. If a term is already in use across a product, the bar for changing it is high — the disruption of inconsistency often outweighs the benefit of a better word.

---

## Adapting these attributes

These attributes are a starting point, not a fixed prescription.

1. **Keep what fits.** Most products benefit from clear, human, and helpful voice.
2. **Replace what doesn't.** If your product's brand calls for a quality not represented here — playful, authoritative, reassuring — define it in the same format: definition, what it means in practice, what it doesn't mean, examples.
3. **Add constraints.** If your product operates in a regulated industry, add a constraint under the relevant attribute. For example: *Clear — in a regulated context: avoid language that implies certainty about outcomes.*
4. **Rank them.** If two attributes come into tension in a specific context, have a conversation about which takes precedence and document the decision.

---

## Related documents

- [Tone spectrum](tone-spectrum.md) — How these attributes express differently across contexts
- [Brand voice audit template](brand-voice-audit-template.md) — How to assess existing content against these attributes
- [Module 2 — UX Writing Standards](../02-ux-writing-standards/README.md) — How to apply these attributes to specific interface patterns
