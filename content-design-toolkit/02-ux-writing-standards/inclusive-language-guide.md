# Inclusive language guide

Inclusive language ensures your content works for the full range of people who might use your product — regardless of gender, age, cultural background, ability, or technical experience. This guide provides practical guidance on the most common decisions content designers face.

**Two kinds of guidance appear in this document.** Some recommendations address accessibility — they help ensure content works across different input methods, assistive technologies, and interaction contexts. Others address inclusive writing — choices about language, terminology, and representation that affect whether users feel respected and accurately described. The two are related but distinct: an accessible interaction design does not substitute for inclusive language, and vice versa. Both are part of content quality.

This module establishes the foundational principle. The rationale is in [Module 1: Content principles](../01-foundations/content-principles.md), Principle 7.

For guidance levels used in this document, see [Module 2 README](../README.md).

---

## Gender-neutral language

**`Rule`** Use gender-neutral language by default. Do not assume the gender of users, customers, support staff, or any other person referenced in the product.

**`Rec`** Use "they/them" as the default singular pronoun when referring to a person whose gender is unknown or unspecified.

> ❌ "The user can view his dashboard."
> ✅ "The user can view their dashboard."
> ✅ "Users can view their dashboard." (restructuring to plural also works)

**`Rec`** Avoid gendered professional terms unless a specific individual has identified with them.

| Avoid | Use |
|---|---|
| "Salesman" | "Sales representative" / "Sales rep" |
| "Stewardess" | "Flight attendant" |
| "Chairman" | "Chair" / "Chairperson" |
| "Manpower" | "Workforce" / "People" / "Capacity" |

**`C`** For products where users can set a preferred pronoun in their profile, use that setting to personalise content. If the product does not support pronoun preferences, gender-neutral language is the correct default.

---

## Ability-neutral language

**`Rule`** Do not write copy that assumes physical or cognitive ability. Avoid instructions that require a specific sense or motor action to understand.

**A note on disability-related language:** Conventions around disability terminology vary between communities and individuals. Some people prefer identity-first language ("autistic person"); others prefer person-first language ("person with autism"). When writing for or about people with specific disabilities, follow the community's or individual's stated preference where known. Where it is not known, person-first language is a reasonable default for formal or professional content. The guidance in this section focuses on avoiding copy that makes unwarranted assumptions about how users interact with a product — not on prescribing identity or community terminology.

| Avoid | Use |
|---|---|
| "Click the button" | "Select the button" |
| "Simply drag the item" | "Move the item" (or describe the action specifically) |
| "You'll see a confirmation" | "A confirmation will appear" |
| "As you can see above" | "As shown above" |
| "Tap with two fingers" | "Use the [name] gesture" (and provide keyboard alternative) |

**`Rec`** Prefer device-neutral language for interactive instructions where multiple input methods are equally valid. "Select" works across mouse, keyboard, touchscreen, and voice navigation; "click" implies a mouse. When documenting a specific platform or interaction method (such as iOS documentation that deliberately uses "tap", or instructions for a keyboard shortcut), platform-specific language is appropriate. The goal is to avoid assuming a mouse where the instruction applies equally to all users — not to replace every instance of "click" regardless of context.

**`C`** When documenting keyboard shortcuts or specific interaction methods, describe the action generically first, then give the specific method as a supplement.

> ✅ "Open the menu. On a keyboard, press [shortcut]."

---

## Cultural and regional language

**`Rule`** Avoid idioms, metaphors, and colloquialisms that do not translate reliably across languages and cultures. These create friction for non-native speakers and translation systems.

| Avoid | Use |
|---|---|
| "Ballpark figure" | "Approximate figure" |
| "Hit the ground running" | "Get started quickly" |
| "Move the goalposts" | "Change the requirements" |
| "Boiling the ocean" | "Attempting something too large" |
| "Burning the midnight oil" | "Working late" |

**`Rec`** Use formats that are unambiguous across regions, or state the format explicitly.

| Ambiguous | Clear |
|---|---|
| "03/04/25" (date) | "3 April 2025" or "April 3, 2025" — write the month as text |
| "$1,000" (currency) | Include currency code for international products: "USD 1,000" or "£1,000" |
| "1.5" (decimal separator) | Note format when targeting audiences that use a comma as the decimal separator |

**`Rec`** Avoid examples that assume one cultural context (sports metaphors, local celebrity references, public holidays from one country).

---

## Age and experience

**`Rec`** Do not write content that assumes the user is young, tech-savvy, or familiar with digital conventions. Avoid references that date the product or assume a narrow cultural frame.

> ❌ "Hit the like button — it's as easy as social media!"
> ✅ "Select the [like/recommend] button."

**`Rec`** Avoid condescending language that implies the task is easy. Words like "simply", "just", "obviously", and "of course" can make a user feel inadequate if they find the task difficult.

> ❌ "Just click here to get started. It's that simple!"
> ✅ "Select here to get started."

---

## Plain language

Plain language is part of inclusive design. Content that is unnecessarily complex, jargon-heavy, or formally structured excludes users who are not specialists, non-native speakers, users with cognitive disabilities, and users under cognitive load (which is most people, most of the time).

**`Rec`** Write at the appropriate readability level for your audience. See [readability standards](readability-standards.md) for target grade levels and measurement tools.

**`Rec`** Define technical terms on first use. Do not assume all users know the vocabulary of your domain.

**`Rec`** Use short sentences and short paragraphs. Break up long explanations with headings, numbered steps, or bullet points when the content is sequential or comparative.

**`Rec`** Use the most common word when two words mean the same thing.

| Less common | More common |
|---|---|
| "Utilise" | "Use" |
| "Commence" | "Start" |
| "Endeavour" | "Try" |
| "Terminate" | "End" / "Stop" |
| "Prior to" | "Before" |
| "In order to" | "To" |

---

## A note on evolving language

Language norms around inclusion change over time. This guide reflects current widely accepted standards, but the right approach is to stay informed, listen to feedback from users, and update guidance when better practices emerge. Inclusive language is an ongoing practice, not a fixed checklist.

Resources for staying current:
- [Conscious Style Guide](https://consciousstyleguide.com) — Regularly updated resource on inclusive and thoughtful language choices
- [GOV.UK Style Guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style) — Plain language guidance used by UK government digital services
- [Apple Inclusive Design](https://developer.apple.com/design/human-interface-guidelines/inclusion) — Inclusive language in product and UI copy

---

## Review checklist

Before publishing, verify:

- [ ] Gender-neutral pronouns used throughout (they/them or restructured to plural)
- [ ] No gendered professional terms
- [ ] No instructions that assume a specific input method (mouse, touch, sight) where the instruction applies to all users
- [ ] Device-neutral language used for primary interactive actions where appropriate ("select" rather than "click" in general copy)
- [ ] No idioms or colloquialisms that do not translate reliably
- [ ] Dates, currencies, and numbers written in unambiguous formats
- [ ] No condescending language ("simply", "just", "obviously")
- [ ] Technical terms defined on first use
- [ ] Readability score at the appropriate level for the content type (see [readability standards](readability-standards.md))

---

## Related documents

- [Content principles](../01-foundations/content-principles.md) — Principle 7: Write inclusively
- [Readability standards](readability-standards.md) — Plain language targets and tools
- [Module 6 — Content Quality Evaluation](../06-content-quality-evaluation/README.md) — Inclusive language as a scored dimension in the quality rubric
