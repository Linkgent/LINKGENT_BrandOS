# Presentation Thinking

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

Presentation Thinking defines how LINKGENT transforms information into understanding before visual production begins.

This file is the canonical owner of the Presentation generation and design process.

No other Presentation System file may redefine the process order.

---

## Canonical Process

### `PRES-PROCESS-001`

```text
Audience
  ↓
Purpose and Expected Outcome
  ↓
Governing Message
  ↓
Content Architecture
  ↓
Narrative Architecture
  ↓
Slide Architecture
  ↓
Representation / Pattern
  ↓
Component Composition
  ↓
Layout
  ↓
Typography
  ↓
Color
  ↓
Imagery and Motion
  ↓
Validation
  ↓
Delivery
```

Higher stages govern lower stages.

When a lower-stage decision conflicts with a higher-stage need, the higher stage wins.

Examples:

- Understanding wins over visual drama.
- Evidence wins over narrative convenience.
- Message clarity wins over fitting content onto one slide.
- Accessibility wins over visual subtlety.
- Audience needs win over the presenter's preferred style.
- Delivery conditions win over tool-specific effects.

---

## Why Three Architectures Exist

“Information Architecture” is not one operation in presentation work.

LINKGENT separates it into three levels.

### Content Architecture

Content Architecture determines what information exists and whether it is trustworthy, relevant, and usable.

It includes:

- Source inventory
- Fact extraction
- Terminology normalization
- Duplicate removal
- Unit and time-period reconciliation
- Evidence quality assessment
- Fact, interpretation, assumption, proposal, and unknown classification
- Essential, supporting, reference, and remove classification
- Evidence gap identification

Output:

```text
Content Inventory
Evidence Map
Terminology Map
Content Priority Map
Unknowns and Gaps
```

### Narrative Architecture

Narrative Architecture determines how understanding develops across the complete presentation.

It includes:

- Entry point
- Context
- Question, tension, risk, or opportunity
- Insight
- Response
- Evidence
- Trade-off
- Decision
- Action
- Transition logic

Output:

```text
Governing Message
Story Spine
Chapter Sequence
Claim–Evidence–Implication–Action Map
Transition Logic
```

### Slide Architecture

Slide Architecture determines the meaning, information relationships, and reading order within each slide.

It includes:

- Slide purpose
- One primary message
- Evidence role
- Relationship type
- Reading order
- Density
- Representation
- Primary component
- Supporting components
- Source placement
- Interaction with speaker notes

Output:

```text
Slide Specification
Reading Order
Density Assignment
Source Requirement
```

These architectures are connected but not interchangeable.

A strong Content Architecture cannot compensate for a weak Narrative Architecture. A strong story cannot compensate for a confusing Slide Architecture.

---

## Stage 1: Audience First

The primary audience must be explicit.

Define:

- Primary audience
- Decision owner
- Secondary stakeholders
- Existing knowledge
- Motivations
- Concerns and objections
- Vocabulary and expertise level
- Cultural and language context
- Accessibility needs
- Viewing conditions
- Time available
- Expected participation

A presentation for “everyone” is not an audience definition.

When several audiences have conflicting needs:

1. Identify the primary audience.
2. Protect the decision path for that audience.
3. Support secondary audiences through notes, appendix, or follow-up artifacts.
4. Do not overload the main story to satisfy every possible reader.

---

## Stage 2: Purpose and Expected Outcome

Purpose is defined as an audience outcome, not a creator activity.

Preferred:

```text
Enable [audience]
to [understand / decide / align / learn / act]
about [subject]
within [context].
```

Define:

- Purpose
- Expected outcome
- Required decision or action
- Success condition
- Non-goals

Avoid:

- “Create a professional deck.”
- “Explain the project.”
- “Make the content look good.”

A presentation may have several supporting outcomes, but it must have one governing purpose.

---

## Stage 3: Governing Message

The Governing Message is the most important conclusion the audience should retain.

It is not the topic.

Topic:

```text
AI-enabled production
```

Governing Message:

```text
AI production should be introduced through a governed design system before it is scaled across teams.
```

A valid Governing Message is:

- Specific
- Relevant to the audience
- Supported by available evidence
- Connected to the expected outcome
- Strong enough to govern inclusion and exclusion
- Clear enough to test every slide against

Every chapter and slide must support, qualify, evidence, operationalize, or responsibly challenge the Governing Message.

---

## Stage 4: Content Architecture

Use `PRES-CONTENT-ARCH-001`.

### Content States

| State | Meaning |
|---|---|
| Defined | Approved or verified information |
| Derived | Logically inferred from defined information |
| Proposed | A recommendation or draft decision |
| Unknown | Missing, contradictory, or unverifiable |

Polished visual treatment must not make Proposed or Unknown information appear Defined.

### Content Priority

Classify each item:

- Essential
- Supporting
- Reference
- Remove

Essential content belongs in the primary reasoning path. Supporting content clarifies or substantiates it. Reference content belongs in the appendix or linked source. Remove content does not create audience value.

### Evidence Discipline

For every material claim, identify:

- Source
- Date
- Owner
- Scope
- Method
- Confidence
- Limitations

Do not create a chart, metric, quote, or customer statement without a traceable source.

---

## Stage 5: Narrative Architecture

Use `PRES-NARRATIVE-ARCH-001`.

A narrative is a reasoning sequence, not theatrical storytelling.

Common transition relationships include:

- Because
- Therefore
- However
- Compared with
- For example
- As a result
- To decide this
- Next

A transition must explain why the audience should move from one idea to the next.

### Story Spine

A default reasoning spine may include:

```text
Context
  ↓
Question / Tension / Opportunity
  ↓
Insight
  ↓
Response
  ↓
Evidence and Feasibility
  ↓
Trade-off
  ↓
Decision
  ↓
Action
```

This is not a mandatory template. The correct sequence depends on audience and purpose.

### Chapter Test

Each chapter must have:

- A chapter message
- A role in the overall argument
- A clear transition from the previous chapter
- Evidence appropriate to its claim
- A reason to exist

Remove chapters that only categorize content without advancing understanding.

---

## Stage 6: Slide Architecture

Use `PRES-SLIDE-ARCH-001`.

### One Slide, One Message

Every slide should communicate one primary conclusion, question, decision, or instruction.

“One slide, one message” does not mean one data point or one object. Multiple elements may appear when they collectively support one message.

Split a slide when:

- It contains independent conclusions.
- It requires two unrelated reading paths.
- It uses unrelated evidence sets.
- The title cannot accurately summarize the complete slide.
- The audience must make more than one decision.

### Slide Specification

```yaml
slide_id: S01
story_role: establish-decision-context
purpose: explain-why-action-is-required-now
message: The current operating model cannot support the next growth phase.
message_type: claim
content_state: proposed
evidence:
  - source_id: SRC-01
    role: primary
implication: A structural change is required before expansion.
information_relationship: cause-effect
density: analytical
pattern: Presentation/Pattern/Problem
primary_component: Presentation/Component/Flow
supporting_components:
  - Presentation/Component/Metric
reading_order:
  - message
  - evidence
  - implication
source_requirement: visible
```

Rendering begins only after the semantic specification is coherent.

---

## Stage 7: Representation / Pattern

Choose representation from the information relationship.

| Information Relationship | Preferred Representation |
|---|---|
| Single conclusion | Statement, Metric, or Callout |
| Precise lookup | Table |
| Quantitative pattern | Chart |
| Chronology | Timeline |
| Planned progression | Roadmap |
| Movement or dependency | Flow |
| Ordered action | Process |
| Difference or choice | Comparison |
| Hierarchy | Hierarchy diagram |
| Human evidence | Quote |
| Visual evidence or context | Image |

Use [`Patterns.md`](./Patterns.md) for recurring communication arrangements.

Do not select a pattern because it creates visual variety.

---

## Stage 8: Component Composition

Use one primary component whenever practical.

Supporting components may be added only when they:

- Provide evidence
- Clarify meaning
- Enable comparison
- Expose a decision
- Provide necessary context

Avoid collections of cards that merely divide paragraphs into boxes.

A component is justified by information structure, not by available space.

---

## Stage 9: Layout

Layout makes Slide Architecture visible.

Apply [`Layout.md`](./Layout.md).

Layout must establish:

- Reading order
- Grouping
- Hierarchy
- Alignment
- Rhythm
- Focus
- Balance
- Density
- Source attachment

Layout must not invent meaning that does not exist in the content.

---

## Stage 10: Typography

Typography reveals semantic hierarchy.

Apply:

- `TYPE-PRESENTATION-HIERARCHY`
- `TYPE-PRESENTATION-MIN-BODY`
- `TYPE-PRESENTATION-MIN-CAPTION`

Canonical values are owned by [`../04_Typography.md`](../04_Typography.md).

Do not copy numeric values into this file.

Restructure content before reducing typography.

---

## Stage 11: Color

Color supports structure, focus, state, and data meaning.

Apply:

- `COLOR-CONTRAST-NORMAL`
- `COLOR-CONTRAST-LARGE`
- `COLOR-ACCENT-INVERSE-PROHIBITED`
- `COLOR-FOCAL-AREA-GUIDANCE`
- `COLOR-NOT-SOLE-CARRIER`

Canonical values and roles are owned by [`../03_Color_System.md`](../03_Color_System.md).

Color must not compensate for unclear hierarchy or weak comparison.

---

## Stage 12: Imagery and Motion

Imagery must have a communication role:

- Evidence
- Demonstration
- Context
- Human story
- Conceptual framing

AI-generated imagery must not be presented as factual evidence.

Motion must:

- Reveal sequence
- Preserve orientation
- Clarify transformation
- Support facilitation

Motion must not exist only to make the deck feel dynamic.

---

## Stage 13: Validation

Validation is part of design, not a final cosmetic check.

Apply:

1. [`Release_Gates.md`](./Release_Gates.md)
2. [`Audit_Checklist.md`](./Audit_Checklist.md) when risk requires it
3. [`Accessibility.md`](./Accessibility.md)
4. Platform conversion testing when the artifact will move between tools

Validation must cover:

- Logic
- Evidence
- Content
- Accessibility
- Platform behavior
- Editability
- Sources
- Delivery conditions

---

## Stage 14: Delivery

Delivery includes more than exporting a file.

Define:

- Delivery platform
- Presenter
- Audience access
- Distribution channel
- Version and approval state
- Speaker notes
- Source visibility
- Accessibility accommodations
- Editability expectation
- Archive location
- Follow-up action

A deck is complete when the intended audience can use it as intended.

---

## Information Density

Assign each slide one density mode.

| Density | Purpose |
|---|---|
| Statement | One primary idea with minimal support |
| Standard | One message with essential explanation or evidence |
| Analytical | A message supported by structured evidence |
| Reference | Detailed information intended for lookup |

Density is not quality. The correct density depends on the classification axes defined in [`README.md`](./README.md).

A complex visual requires simpler surrounding content. A dense table requires restrained annotation. Reference detail should not interrupt the primary narrative.

---

## Diagram First

Use a diagram when relationships are the content.

A diagram is appropriate when it clarifies:

- Sequence
- Dependency
- Hierarchy
- Flow
- Feedback
- Comparison
- System boundaries
- Cause and effect

Do not turn a paragraph into a diagram if the relationships are not meaningful.

---

## Comparison Before Decoration

When the audience must choose, evaluate, prioritize, or understand difference:

1. Define the shared comparison axis.
2. Normalize units and time periods.
3. Identify the focal difference.
4. Make trade-offs visible.
5. State the implication.
6. Add visual refinement only after comparability is established.

Decorative contrast must not replace analytical comparability.

---

## Visual Hierarchy

Hierarchy should make the reading order understandable before detailed reading.

Use, in priority order:

1. Position
2. Grouping
3. Whitespace
4. Scale
5. Weight
6. Contrast
7. Color
8. Decoration

No slide should contain several elements competing for primary attention.

---

## Design Balance

Balance is the controlled distribution of visual and informational weight.

Evaluate:

- Content weight
- Visual weight
- Empty space
- Direction
- Alignment
- Contrast
- Density
- Focal point
- Stability
- Tension appropriate to the message

Balance is not mandatory symmetry.

---

## AI Thinking Requirement

AI must execute `PRES-PROCESS-001` and preserve stage outputs.

AI must not:

- Start from layout
- Start from a template
- Copy source-document headings automatically
- Create evidence
- Hide uncertainty
- Use visual polish to imply approval
- Skip validation because an artifact is editable

AI stage outputs are defined in [`AI_Generation.md`](./AI_Generation.md).

---

## Canonical Principle

```text
Structure creates understanding.
Understanding creates trust.
Trust enables decisions and action.
```
