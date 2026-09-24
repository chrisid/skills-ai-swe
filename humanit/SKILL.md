---
name: humanit
description: Rewrite AI-sounding text so it reads naturally without changing what it says.
license: MIT
metadata:
  version: "4.0.0"
---

# Humanizer

Rewrite AI-sounding text so it reads like the writer, not a chatbot.

Keep the meaning, facts, names, numbers, dates, quotes, citations, and intent unchanged. Do not invent information.

## Core principles

A model tends to choose writing patterns that work broadly across many readers and topics. Human writing is usually more specific, uneven, and intentional.

Look especially for these patterns:

- **Staging.** Sentences announce, frame, or inflate a point instead of stating it directly.
- **Rhythm by rule.** Triads, repeated sentence structures, fragments, and dashes are used by habit rather than because the meaning calls for them.
- **Inflation.** Ordinary facts are made to sound pivotal, profound, authoritative, or more important than the source supports.
- **Formatting by rule.** Bold labels, headings, lists, and other formatting are applied consistently whether or not they improve the text.
- **Leftovers.** Chatbot phrases, drafting notes, disclaimers, and other text remain even though they were never meant for the reader.

Every sentence should add information, meaning, tone, or useful emphasis. Remove language that exists only to make the writing sound important.

## How to work

1. Read the full text before editing.
2. Identify AI writing patterns, starting with the strongest ones.
3. Rewrite naturally while preserving every supported claim.
4. Read the result again and check for anything that still sounds formulaic or AI-generated.
5. Verify that no fact, name, number, date, quote, citation, ranking, or conclusion was added or accidentally removed.

You may shorten repetitive sections, merge or split sentences, reorder material for clarity, and simplify wording.

Do not add missing details. If a sentence requires information the source does not provide, simplify it or state that the information is unavailable when necessary.

## Voice

If the user provides a writing sample, match its sentence length, vocabulary, punctuation, rhythm, openings, transitions, and level of formality.

The sample takes priority over the rules below when a stylistic choice is clearly intentional.

Without a sample:

- Technical, legal, factual, and reference writing should stay neutral and direct.
- Personal, opinion, essay, or creative writing should preserve the writer's uncertainty, humour, reactions, mixed feelings, and individual voice.

The goal is not only to remove AI patterns. The result should still sound like a specific person writing for a specific reader.

## Patterns to remove

### 1. Staged contrasts

Avoid formulas such as:

- "It's not X, it's Y"
- "Not just X, but Y"
- "Not only X, but Y"
- "This doesn't mean X. It means Y."

**Why:** The negative half often adds emphasis without adding information.

**Instead:** State the actual point directly.

Keep the contrast only when both sides carry real information or correct a genuine misunderstanding.

### 2. One-line closers and dramatic fragments

Watch for:

- "That is the real win."
- "Read that again."
- "Let that sink in."
- repeated one-sentence conclusions
- rows of fragments such as "No compromise. No guessing. No noise."

**Why:** These often repeat the previous point while asking the reader to treat it as important.

**Instead:** Cut repeated closers or merge fragments into a natural sentence.

### 3. Artificial profundity

Watch for:

- "The real question is"
- "At its core"
- "What really matters"
- "Fundamentally"
- "The deeper issue"
- "The heart of the matter"
- metaphors such as "the language of", "the currency of", or "the architecture of"

**Why:** They make an ordinary point sound like a hidden truth without adding substance.

**Instead:** State the specific claim.

### 4. Staged openings

Remove unnecessary openings such as:

- "Let's dive in"
- "Let's explore"
- "Here's what you need to know"
- "Quick note"
- "Honestly?"
- "Look"
- "Here's the thing"
- "Let's be honest"
- "Real talk"

**Why:** They announce the point instead of making it.

**Instead:** Begin with the point itself.

### 5. Arguing with no one

Watch for:

- "I'm not saying..."
- "To be clear..."
- "Don't get me wrong..."
- "This isn't about..."
- "You might think..."
- "A tempting approach would be..."

**Why:** The text may be answering an objection nobody raised.

**Instead:** Remove the defence and state the useful claim directly.

Keep genuine objections when they are relevant to the argument.

## Rhythm

### 6. Forced triads

Watch for ideas repeatedly appearing in groups of three.

**Why:** Models often use three parallel items because the structure sounds complete, even when the meaning does not naturally have three parts.

**Instead:** Keep all three only when each adds something distinct. Otherwise merge, cut, or vary the structure.

### 7. Repeated sentence openings

Watch for several sentences beginning the same way.

**Why:** Repetition can make the prose feel mechanically generated.

**Instead:** Merge sentences, change the subject, or vary the structure when it improves the rhythm.

Intentional repetition is fine.

### 8. Dashes as the default connector

Avoid em dashes and en dashes unless the writer's sample regularly uses them.

**Why:** Models often use dashes instead of deciding how two clauses actually relate.

**Instead:** Use a comma, colon, period, parentheses, or rewrite the sentence.

Do not change dashes or hyphens inside code, commands, paths, URLs, or other literal text.

### 9. Stacked qualifiers

Watch for combinations such as:

- "could potentially"
- "might arguably"
- "in some cases it may"
- multiple hedges in the same claim

**Why:** Repeated qualification makes simple claims vague and hesitant.

**Instead:** Keep the minimum qualifier required for accuracy.

### 10. Passive or subjectless writing

Prefer active voice when it makes the actor and action clearer.

**Why:** AI writing often hides who is doing something or produces sentence fragments without a clear subject.

**Instead:** Name the actor where the source supports it.

## Inflation

### 11. AI-heavy vocabulary

Be cautious with words such as:

- additionally
- crucial
- pivotal
- robust
- intricate
- enduring
- enhance
- fostering
- landscape
- meticulous
- showcase
- tapestry
- underscore
- vibrant

**Why:** These words are often used automatically to make plain writing sound more polished or important.

**Instead:** Prefer simpler, more specific language when the stronger word adds nothing.

Do not remove a word only because it appears on this list. Keep it when it is natural and accurate.

### 12. Inflated significance

Watch for:

- "a pivotal moment"
- "plays a key role"
- "stands as a testament"
- "marks a major shift"
- "reflects a broader..."
- "sets the stage for..."
- "the future looks bright"
- "exciting times ahead"

**Why:** Ordinary facts are being given significance the source may not support.

**Instead:** Keep the concrete fact and remove the interpretation unless the source explicitly supports it.

### 13. Vague relationships

Watch for phrases such as:

- "associated with"
- "connected to"
- "linked to"
- "tied to"

**Why:** They hide the actual relationship.

**Instead:** Name the relationship when the source provides it. If it does not, do not invent one.

### 14. Shallow "-ing" phrases

Watch for endings such as:

- highlighting
- underscoring
- emphasizing
- ensuring
- reflecting
- symbolizing
- showcasing
- fostering

**Why:** These phrases are often attached to a fact to make it sound more meaningful.

**Instead:** Keep them only when they add a supported claim.

### 15. Sales language

Watch for:

- renowned
- breathtaking
- stunning
- groundbreaking
- rich heritage
- diverse array
- must-visit
- commitment to
- nestled in the heart of

**Why:** Neutral information starts sounding like marketing copy.

**Instead:** State what the thing is or does.

Keep promotional language when promotional writing is actually the task.

### 16. Borrowed authority

Watch for:

- "experts argue"
- "observers say"
- "industry reports"
- "some critics"
- lists of prestigious publications used only to imply credibility

**Why:** An unnamed source or impressive name is standing in for evidence.

**Instead:** Name the actual source and what it says when available. Never invent authority.

### 17. Avoiding simple verbs

Watch for unnecessary substitutes for "is", "are", and "has":

- serves as
- stands as
- functions as
- operates as
- represents
- boasts
- features

**Why:** Simple statements become longer without becoming clearer.

**Instead:** Use the simpler verb when it says the same thing.

## Formatting

### 18. Bold as decoration

Avoid bolding every label or important-looking phrase.

**Why:** Mechanical formatting makes prose feel templated.

**Instead:** Use bold only when it genuinely helps the reader navigate the text.

### 19. Decorative headings

Avoid unnecessary title case, emojis, arrows, repeated separators, or headings that restate the sentence below them.

**Why:** The document starts looking generated from a template rather than structured around the content.

**Instead:** Use simple sentence-case headings only where they improve navigation.

### 20. Repeated heading content

If the first sentence under a heading simply repeats the heading, remove it.

## Leftovers

### 21. Chatbot residue

Remove phrases such as:

- "Of course!"
- "Certainly!"
- "Great question!"
- "I hope this helps"
- "Let me know if..."
- "Would you like me to..."
- "Want me to continue?"
- "Here is a..."

**Why:** These belong to the assistant conversation, not the finished writing.

### 22. Knowledge disclaimers and guesses

Watch for:

- "based on available information"
- "up to my last training update"
- "not widely documented"
- "it appears that"
- "likely..."
- "it is believed that..."

**Why:** The text may acknowledge missing information and then quietly replace it with a guess.

**Instead:** State only what the source supports. If the information is unknown and relevant, say so directly.

### 23. Writing about the previous draft

Avoid explaining what the current text, function, design, or approach replaced unless the document is specifically about that change.

**Why:** Finished writing should usually describe the current state.

## Final check

Before returning the rewrite, look specifically for:

- unsupported additions
- missing facts
- staged "not X but Y" contrasts
- one-line closers
- forced triads
- repeated sentence openings
- unnecessary dashes
- stacked qualifiers
- inflated vocabulary
- sales language
- decorative bold
- chatbot phrases
- unsupported guesses

If any remain without a clear reason, rewrite them.

## Output

### Pasted text

Return:

1. A short list of the main patterns found.
2. The final rewritten text.

### File mode

When editing a named file:

- Run the full process.
- Change prose only.
- Preserve code blocks, inline code, commands, paths, YAML metadata, structured data, and link targets exactly.
- Write only the final rewritten text to the file.
- Give the user a brief summary of what changed.

### Embedded mode

When used inside another task, such as a pull request, document workflow, or commit message, return only the final rewritten text.

This keeps the original prompt's main reasoning, especially the distinction between staging, rhythm, inflation, formatting, and leftovers, while removing a lot of repetition between individual rules. :chatgpt-content-reference{index="0"}
