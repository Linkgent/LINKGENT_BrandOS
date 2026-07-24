# Presentation Content

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

Presentation Content applies LINKGENT Tone & Voice to slide-based communication.

The canonical Tone & Voice remains [`../01_Brand_Core.md`](../01_Brand_Core.md). This file defines how that voice is used in presentations.

Content is part of Information Architecture. It is not text added after design.

---

## Content Principles

### Write for Understanding

Prefer concrete, direct, complete language.

Avoid:

- Buzzwords
- Marketing clichés
- Unexplained abbreviations
- Ambiguous claims
- Decorative wording
- Excessive adjectives
- Confidence unsupported by evidence

### Message Before Copy

Write the slide message before writing supporting copy.

### Evidence Before Emphasis

A strong visual emphasis does not strengthen a weak claim.

### Concision Without Loss

Remove unnecessary language while preserving context, conditions, ownership, and meaning.

### Human-centered Language

Write with respect, clarity, and accessibility. Avoid language that excludes, stereotypes, blames, or obscures responsibility.

---

## Title System

### Message-led Title

Use a message-led title for analytical, persuasive, explanatory, and decision slides.

A message-led title states the conclusion or implication.

Preferred:

```text
The current workflow cannot scale without a shared production system
```

Avoid:

```text
Current Workflow
```

### Topic Title

Topic titles are appropriate for:

- Cover
- Agenda
- Chapter divider
- Reference section
- Appendix
- Neutral navigation

Topic titles must not replace conclusions on slides that contain an argument.

### Question Title

Use a question when the slide genuinely frames inquiry, discussion, or decision.

The body must answer, structure, or advance the question.

Avoid rhetorical questions used only for drama.

### Title Quality Test

A title should:

- Represent the whole slide
- Be understandable without reading every element
- Use the audience's vocabulary
- Avoid unsupported certainty
- Avoid ending with a vague noun
- Avoid duplicating a visible section label

---

## Slide Copy

### Primary Message

Each slide has one primary message owned by [`Thinking.md`](./Thinking.md).

### Supporting Copy

Supporting copy should:

- Explain the message
- Provide evidence
- Clarify scope
- State implication
- Define action

Supporting copy should not introduce a second independent conclusion.

### Paragraphs

Use paragraphs only when continuous reasoning is necessary.

Prefer:

- Short complete sentences
- Clear paragraph boundaries
- Visible relationship to the title
- Limited dependence on spoken explanation for self-guided artifacts

Do not compress a report paragraph into a slide without restructuring it.

---

## Bullet Lists

Use bullets for parallel items.

All items in one list should share:

- Grammatical structure
- Conceptual level
- Time frame
- Voice
- Punctuation logic

Preferred:

```text
- Reduce duplicated work
- Standardize quality checks
- Preserve decision history
```

Avoid mixing:

```text
- Cost reduction
- We should improve quality
- Faster
```

Use numbered lists when order, sequence, priority, or count matters.

Do not use icons as decorative bullets.

---

## Labels

Labels should be:

- Short
- Consistent
- Mutually distinguishable
- Semantically stable across the deck
- Placed close to the object they describe

Use the same term for the same concept.

Do not alternate between synonyms merely for visual variety.

Define abbreviations on first use unless the audience is known to understand them.

---

## Numbers

Use numerals when precision or comparison matters.

Rules:

- Use consistent decimal precision.
- Use consistent thousands separators.
- Preserve signs and units.
- State whether values are actual, forecast, target, indexed, rounded, or estimated.
- Use the same scale across comparisons.
- Do not hide meaningful differences through rounding.
- Do not add precision unsupported by the source.

Examples:

```text
12.4%
¥1.2B
FY2026 forecast
Index: 2025 = 100
```

---

## Dates and Time

Use unambiguous dates.

Preferred:

```text
2026-07-24
July 24, 2026
2026年7月24日
```

Avoid ambiguous forms such as:

```text
7/8
```

Use consistent fiscal-year notation and define it when necessary.

State the time zone when timing affects interpretation.

---

## Units

A unit must be visible where the audience needs it.

Use:

- Consistent unit systems
- Consistent scale
- Direct labels
- Clear definitions for derived measures

Do not mix `%`, percentage points, index values, and raw counts without explanation.

---

## Claims and Evidence

Every material claim should be classifiable as:

- Fact
- Interpretation
- Assumption
- Proposal
- Unknown

Do not write proposals as facts.

Use qualifiers when evidence is limited.

Preferred:

```text
The current evidence suggests...
```

Avoid:

```text
This proves...
```

unless the evidence supports that level of certainty.

---

## Sources and Footnotes

Sources must be:

- Traceable
- Specific
- Attached to the relevant claim, chart, table, quote, or image
- Readable in the intended delivery context
- Preserved in exported formats

A source entry should include, when available:

- Author or organization
- Title
- Date
- URL or document identifier
- Access date for changing online sources
- Relevant page, section, or dataset

Do not use “Source: Internet.”

Source formatting may be compact, but it must not become invisible.

Apply `TYPE-PRESENTATION-MIN-CAPTION`.

---

## Quotes

Quotes require:

- Exact wording
- Speaker or author
- Role or relevant context
- Date or source
- Permission when required
- Clear distinction between verified and reconstructed wording

Do not fabricate quotes or present AI-generated text as a human quotation.

Use ellipses and edits responsibly without changing meaning.

---

## Executive Summary

An executive summary should communicate:

1. Context
2. Governing Message
3. Key evidence
4. Recommendation or decision
5. Principal trade-off or risk
6. Required next action

It is not a miniature table of contents.

It should allow a decision owner to understand the central case without reading the complete deck while preserving material caveats.

---

## Decision Content

A decision slide or section should state:

- Decision required
- Decision owner
- Deadline
- Options
- Evaluation criteria
- Recommendation
- Trade-offs
- Risks
- Consequence of delay
- Next action

Do not hide the decision request in closing copy.

---

## Calls to Action

A call to action must identify:

- Actor
- Action
- Timing
- Output or success condition

Preferred:

```text
Brand Director approves the Release Candidate by 2026-08-07.
```

Avoid:

```text
Move forward.
```

---

## Japanese and English

Use the language most appropriate to the audience.

When Japanese and English are mixed:

- Preserve terminology consistently.
- Avoid switching languages for visual novelty.
- Define specialized English terms where necessary.
- Keep capitalization consistent.
- Do not manually alternate fonts in ways that create unstable layout.
- Apply canonical typography guidance.

Do not translate proper nouns, product names, or technical terms inconsistently.

---

## Translation and Localization

Translation must preserve:

- Meaning
- Evidence
- Tone
- Hierarchy
- Reading order
- Units and dates
- Legal or compliance meaning
- Cultural appropriateness

Localization is not word replacement.

Re-check layout after translation because text expansion, line breaks, and reading direction may change.

Do not use machine translation without review for executive, legal, medical, financial, or public-facing content.

---

## Inclusive Language

Use language that:

- Centers people rather than labels
- Avoids unnecessary gender assumptions
- Avoids ableist metaphors
- Avoids cultural stereotypes
- Uses requested names and pronouns
- Makes responsibility explicit without blame
- Remains understandable across expertise levels

Accessibility language should describe barriers and support needs, not define people by limitations.

---

## Speaker Notes

Speaker notes may contain:

- Context not required on the slide
- Delivery guidance
- Transition language
- Source detail
- Anticipated questions
- Facilitation instructions
- Accessibility cues
- Timing

Speaker notes must not contain essential meaning that a self-guided artifact requires.

Confidential notes must not be included in distributed exports unintentionally.

---

## Alt Text

Alt text should communicate the purpose and meaning of an image, chart, or diagram.

It should not merely describe appearance.

For a chart, include:

- Chart purpose
- Main trend
- Material comparison
- Important exception
- Relevant limitation

For decorative imagery, mark it decorative when the platform supports that state.

Alt text is further governed by [`Accessibility.md`](./Accessibility.md).

---

## Content Metadata

Each deliverable should record:

```yaml
title:
version:
status:
owner:
maintainer:
audience:
purpose:
consumption_mode:
session_mode:
artifact_role:
language:
confidentiality:
source_owner:
last_updated:
```

Metadata may live in the file, notes, document properties, or delivery record, but it must be recoverable.

---

## Content Review Rules

Before release:

- The Governing Message is explicit.
- Titles represent slide conclusions.
- Terminology is consistent.
- Facts, proposals, assumptions, and unknowns are distinguishable.
- Units and dates are unambiguous.
- Sources are traceable.
- Quotes are verified.
- Calls to action identify actor and timing.
- Self-guided content does not depend on hidden narration.
- Speaker notes do not leak confidential content.
- Alt text is meaningful.
- Localization has been reviewed.
- Inclusive language has been checked.

Use [`Release_Gates.md`](./Release_Gates.md) for mandatory release decisions.
