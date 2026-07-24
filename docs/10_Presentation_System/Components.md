# Presentation Components

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

Presentation Components define reusable semantic parts used inside slides.

Components are not templates and are not complete slide narratives.

Namespace:

```text
Presentation/Component/{Name}
```

Examples:

```text
Presentation/Component/Metric
Presentation/Component/Comparison
Presentation/Component/Chart
```

Component selection follows `PRES-PROCESS-001` after Representation / Pattern is resolved.

---

## Component Contract

Every component definition must include:

```yaml
name:
namespace:
purpose:
status: draft | candidate | stable | deprecated
owner:
maintainer:
introduced_in:
anatomy:
variants:
content_rules:
typography_dependencies:
color_dependencies:
accessibility_requirements:
platform_support:
tested_in:
accessibility_status:
examples:
known_limitations:
prohibited_use:
replaced_by:
```

### Status

| Status | Meaning |
|---|---|
| `draft` | Incomplete or exploratory |
| `candidate` | Documented and usable in controlled work; validation incomplete |
| `stable` | Implemented, tested, accessible, documented, and approved |
| `deprecated` | Retained for migration; do not use in new work |

### Accessibility Status

```text
not-reviewed
partial
verified
exception
```

### Platform Support

Use:

```text
not-planned
planned
prototype
implemented
validated
limited
```

A component must not be called stable without test evidence.

---

## Version 0.9 Registry

All components are `candidate` until Golden Deck and platform validation are complete.

| Component | Namespace | Status | Accessibility | Known Limitation |
|---|---|---|---|---|
| Title | `Presentation/Component/Title` | candidate | partial | Cross-platform text metrics not fully validated |
| Section | `Presentation/Component/Section` | candidate | partial | Motion and dark-surface behavior not fully validated |
| Card | `Presentation/Component/Card` | candidate | partial | Overuse risk |
| Callout | `Presentation/Component/Callout` | candidate | partial | Semantic color mapping depends on context |
| Table | `Presentation/Component/Table` | candidate | partial | Reading order differs by platform |
| Chart | `Presentation/Component/Chart` | candidate | partial | Alt-text and export validation incomplete |
| Timeline | `Presentation/Component/Timeline` | candidate | partial | Dense timelines may fail small-screen use |
| Roadmap | `Presentation/Component/Roadmap` | candidate | partial | Status and certainty labeling need validation |
| Flow | `Presentation/Component/Flow` | candidate | partial | Connector routing can drift in conversion |
| Process | `Presentation/Component/Process` | candidate | partial | Long sequences require adaptation |
| Comparison | `Presentation/Component/Comparison` | candidate | partial | Unequal content may create false equivalence |
| Metric | `Presentation/Component/Metric` | candidate | partial | Context omission risk |
| Quote | `Presentation/Component/Quote` | candidate | partial | Source and permission workflow not automated |
| Image | `Presentation/Component/Image` | candidate | partial | Alt-text metadata portability varies |
| Icon | `Presentation/Component/Icon` | candidate | partial | Canonical Iconography System not yet active |

---

## Composition Rules

Use:

```text
One primary component
+ supporting components only when necessary
```

A component must have a semantic job.

Valid jobs include:

- State a conclusion
- Provide evidence
- Expose comparison
- Show sequence
- Show dependency
- Show hierarchy
- Show progress
- Preserve a source
- Enable action

Do not add components only to create visual variety.

---

## Title

### Namespace

```text
Presentation/Component/Title
```

### Purpose

Communicate the primary message or navigation role.

### Anatomy

- Optional eyebrow or section label
- Primary title
- Optional subtitle
- Optional metadata

### Variants

- Message-led
- Topic
- Question
- Cover
- Chapter

### Rules

Apply [`Content.md`](./Content.md).

Message-led is the default for analytical and decision slides. Topic titles are reserved for navigation and neutral framing.

### Prohibited Use

- A topic label that hides the actual conclusion
- Multiple competing titles
- Decorative line breaks that change meaning
- Title styling unsupported by semantic hierarchy

---

## Section

### Namespace

```text
Presentation/Component/Section
```

### Purpose

Create a meaningful narrative boundary.

### Anatomy

- Section number or label
- Chapter message
- Optional transition statement

### Rules

A Section must advance the Narrative Architecture. It must not exist only to separate equal-sized groups.

---

## Card

### Namespace

```text
Presentation/Component/Card
```

### Purpose

Group an independent but related information unit.

### Anatomy

- Optional label
- Heading
- Content
- Optional icon, metric, status, or action

### Variants

- Informational
- Comparative
- Metric
- Status
- Action

### Rules

Cards require shared anatomy and meaningful boundaries.

### Prohibited Use

- One card per paragraph
- Colored cards used instead of hierarchy
- Unequal concepts forced into equal cards
- More cards than can be scanned

---

## Callout

### Namespace

```text
Presentation/Component/Callout
```

### Purpose

Surface an implication, warning, recommendation, decision, or exception.

### Anatomy

- Label
- Message
- Optional supporting statement
- Optional icon

### Rules

Callout semantics must match the content state. Semantic colors may be used only for their canonical meaning.

---

## Table

### Namespace

```text
Presentation/Component/Table
```

### Purpose

Support precise lookup or multi-variable comparison.

### Anatomy

- Title or message
- Column headers
- Row labels
- Data cells
- Notes
- Source

### Rules

- Use meaningful sort order.
- Align numbers consistently.
- Keep units visible.
- Use spacing and borders before multiple fills.
- Highlight only what supports the governing message.
- Provide a summary for complex tables.

### Accessibility

- Define reading order.
- Avoid color-only meaning.
- Preserve headers in exported formats where supported.
- Add a text summary for key findings.

---

## Chart

### Namespace

```text
Presentation/Component/Chart
```

### Purpose

Reveal a quantitative relationship, pattern, distribution, composition, or change.

### Anatomy

- Message-led title
- Plot
- Direct labels or legend
- Annotation
- Unit
- Source
- Alt text or summary

### Rules

- Select chart type from analytical purpose.
- Normalize scales and periods.
- Use one focal data role when appropriate.
- Keep comparison series subordinate.
- Avoid decorative 3D, gradients, and chart effects.
- State material limitations.

### Accessibility

Apply canonical Color rules and [`Accessibility.md`](./Accessibility.md). Provide a text summary of the main finding.

---

## Timeline

### Namespace

```text
Presentation/Component/Timeline
```

### Purpose

Communicate chronology.

### Rules

- Preserve time scale or state clearly when spacing is symbolic.
- Distinguish past, present, and future.
- Label uncertainty.
- Do not use a timeline for non-temporal sequence.

---

## Roadmap

### Namespace

```text
Presentation/Component/Roadmap
```

### Purpose

Communicate planned progression, dependencies, milestones, and ownership.

### Rules

A Roadmap should identify:

- Time horizon
- Workstreams
- Milestones
- Owners
- Dependencies
- Decision points
- Confidence or status

A Roadmap is not a decorative timeline.

---

## Flow

### Namespace

```text
Presentation/Component/Flow
```

### Purpose

Show movement, transfer, dependency, or cause and effect.

### Rules

- Use explicit direction.
- Label connectors when meaning is not obvious.
- Minimize crossings.
- Keep start and end states clear.
- Preserve meaning without animation.

---

## Process

### Namespace

```text
Presentation/Component/Process
```

### Purpose

Show ordered actions or stages.

### Rules

- Use numbered stages when order matters.
- Distinguish actor, action, input, and output when relevant.
- Show iteration and feedback accurately.
- Do not force cyclical work into a linear process.

---

## Comparison

### Namespace

```text
Presentation/Component/Comparison
```

### Purpose

Expose meaningful differences using shared criteria.

### Anatomy

- Compared entities
- Shared criteria
- Evidence
- Focal difference
- Implication

### Rules

- Normalize units and periods.
- Use comparable content.
- Make trade-offs visible.
- Avoid false equivalence created by equal boxes.
- State the recommendation separately when required.

---

## Metric

### Namespace

```text
Presentation/Component/Metric
```

### Purpose

Surface a value with context and implication.

### Anatomy

- Label
- Value
- Unit
- Time period
- Comparator or target
- Interpretation
- Source

### Rules

A large number without context is not a Metric component.

Do not use visual size to imply importance unsupported by the decision context.

---

## Quote

### Namespace

```text
Presentation/Component/Quote
```

### Purpose

Present verified human evidence or a relevant authoritative statement.

Apply quote rules from [`Content.md`](./Content.md).

Do not use invented, reconstructed, or AI-generated wording as a quotation.

---

## Image

### Namespace

```text
Presentation/Component/Image
```

### Purpose

Provide evidence, demonstration, context, human story, or conceptual framing.

### Rules

- Identify role.
- Preserve source and rights.
- Avoid misleading crops.
- Add alt text.
- Do not present generated imagery as documentary evidence.
- Do not use generic imagery only to fill space.

---

## Icon

### Namespace

```text
Presentation/Component/Icon
```

### Provisional Family

Until `06_Iconography.md` is active:

```text
Material Symbols Outlined
```

This is a presentation-level provisional application, not a Brand OS-wide canonical redefinition.

### Rules

- Use one family.
- Use icons only when recognition improves.
- Pair unfamiliar icons with labels.
- Do not use icons as decorative bullets.
- Do not use an icon as the sole carrier of essential meaning.

---

## Implementation Evidence

Each platform implementation should record:

```yaml
component:
platform:
implementation_status:
version:
tested_on:
tested_by:
accessibility_status:
conversion_test:
known_limitations:
example:
```

Platforms include:

- PowerPoint
- Google Slides
- Keynote
- Canva
- Figma Slides
- AI generation
- PDF export

---

## Contribution and Change

A new component or variant requires:

1. A recurring communication need
2. A semantic difference from existing components
3. A complete Component Contract
4. Accessibility review
5. At least one example
6. Platform implementation plan
7. Known limitations
8. Brand Director approval before stable status

Visual variation alone is not a new component.

---

## Deprecation

A deprecated component must identify:

- Reason
- Replacement
- Migration guidance
- Last supported version
- Removal or archive plan

Do not silently delete a component used by templates or generated artifacts.
