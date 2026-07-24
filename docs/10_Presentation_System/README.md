# Presentation System

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

The LINKGENT Presentation System defines how structured thinking becomes communication that people can understand, discuss, decide upon, and act upon.

A LINKGENT presentation is not a collection of visually polished slides. It is:

> **Communication Design for shared understanding and decision-making.**

This system is platform-independent and applies to:

- PowerPoint
- Google Slides
- Keynote
- Canva
- Figma Slides
- Gamma
- AI presentation systems
- Future presentation environments

The same visual output is not required in every tool. The same intent, meaning, hierarchy, accessibility, traceability, and quality standard are required.

---

## Definition

At LINKGENT, a presentation is:

> A structured communication system that transforms complex information into shared understanding and enables an audience to decide, align, learn, or act.

A presentation is not defined by software, file format, template, animation, or visual style. It is defined by the quality of the decisions that precede visual production.

```text
Do not design slides.
Design understanding.
```

---

## Inheritance

This directory is an Applied System within LINKGENT Brand OS.

It inherits:

1. [`../../CONSTITUTION.md`](../../CONSTITUTION.md)
2. [`../01_Brand_Core.md`](../01_Brand_Core.md)
3. [`../03_Color_System.md`](../03_Color_System.md)
4. [`../04_Typography.md`](../04_Typography.md)
5. `../05_Design_Tokens.md` when active
6. `../06_Iconography.md` when active
7. `../07_Photography.md` when active
8. `../08_Illustration.md` when active
9. `../09_Layout_System.md` when active
10. `../13_AI_Generation_Rules.md` when active

This system applies those foundations to presentation communication. It must not redefine canonical brand meanings owned by upstream files.

When rules conflict, the higher-level canonical source takes precedence.

---

## Brand Core Application

### Structure First

Visual design must reveal the logic, priority, relationship, and sequence of information. A polished layout must not compensate for weak thinking.

### UX Before UI

The audience experience comes before the appearance of the slide. Design must account for prior knowledge, decision context, viewing conditions, cognitive load, accessibility needs, and expected action.

### Beauty Through Purpose

Beauty emerges when message, evidence, typography, spacing, color, imagery, and composition support the same communication purpose.

### Human × AI Collaboration

Humans retain responsibility for intent, judgment, evidence, ethics, approval, and delivery. AI may accelerate analysis, structuring, specification, production, adaptation, and validation.

---

## Canonical Process

The only canonical presentation process is defined in [`Thinking.md`](./Thinking.md) as `PRES-PROCESS-001`.

All other files must reference that process. They must not create a competing sequence.

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

---

## System Architecture

```text
10_Presentation_System/
├── README.md
├── Thinking.md
├── Content.md
├── Layout.md
├── Components.md
├── Patterns.md
├── AI_Generation.md
├── Accessibility.md
├── Release_Gates.md
└── Audit_Checklist.md
```

### File Responsibilities

| File | Canonical Responsibility |
|---|---|
| [`README.md`](./README.md) | Scope, inheritance, architecture, governance, reading order |
| [`Thinking.md`](./Thinking.md) | Canonical process and presentation reasoning |
| [`Content.md`](./Content.md) | Presentation-specific writing, labeling, sourcing, notes, localization, alt text |
| [`Layout.md`](./Layout.md) | Safe area, grid, whitespace, alignment, rhythm, balance, density application |
| [`Components.md`](./Components.md) | Reusable semantic presentation parts and component maturity |
| [`Patterns.md`](./Patterns.md) | Reusable communication and slide patterns |
| [`AI_Generation.md`](./AI_Generation.md) | AI input contract, specification, generation, adaptation, traceability |
| [`Accessibility.md`](./Accessibility.md) | Presentation-specific accessibility application and validation |
| [`Release_Gates.md`](./Release_Gates.md) | Mandatory release gates for every deliverable |
| [`Audit_Checklist.md`](./Audit_Checklist.md) | Risk-based and full-system audit criteria |

---

## Concepts and Namespaces

The system separates three levels that may share similar names.

```text
Presentation/Component/Comparison
Presentation/Pattern/Comparison
Presentation/Template/ExecutiveDecisionDeck
```

### Component

A reusable part used inside a slide.

Example:

```text
Presentation/Component/Metric
```

### Pattern

A reusable communication arrangement that solves a recurring presentation problem.

Example:

```text
Presentation/Pattern/Problem
```

### Template

An implemented, editable asset for a specific tool, audience, or deck type.

Example:

```text
Presentation/Template/ExecutiveDecisionDeck
```

Templates belong under:

```text
templates/presentation/
```

This directory defines Components and Patterns. It does not contain tool implementation assets.

---

## Presentation Classification

Presentation context must be described through independent axes. The values are not mutually exclusive across axes.

### Consumption Mode

```yaml
consumption_mode:
  - live
  - self_guided
  - hybrid
```

| Value | Meaning |
|---|---|
| `live` | Meaning is delivered through a presenter and visual support |
| `self_guided` | The artifact must be understandable without spoken explanation |
| `hybrid` | The artifact must support both live delivery and independent reading |

### Session Mode

```yaml
session_mode:
  - presentation
  - decision
  - workshop
```

| Value | Meaning |
|---|---|
| `presentation` | Explain, inform, teach, persuade, or align |
| `decision` | Enable approval, prioritization, selection, or commitment |
| `workshop` | Facilitate participation, exploration, synthesis, or co-creation |

### Artifact Role

```yaml
artifact_role:
  - working
  - read_ahead
  - reference
  - archive
```

| Value | Meaning |
|---|---|
| `working` | A changeable artifact used during active development |
| `read_ahead` | A self-contained artifact reviewed before a session |
| `reference` | A durable source for later consultation |
| `archive` | A preserved record of a decision, event, or approved state |

Example:

```yaml
consumption_mode: live
session_mode: decision
artifact_role: read_ahead
```

---

## Canonical Rule References

Presentation files should reference canonical rules instead of copying raw values.

| Rule ID | Canonical Owner |
|---|---|
| `TYPE-PRESENTATION-MIN-BODY` | `04_Typography.md` → Accessibility → Minimum Size |
| `TYPE-PRESENTATION-MIN-CAPTION` | `04_Typography.md` → Accessibility → Minimum Size |
| `TYPE-PRESENTATION-HIERARCHY` | `04_Typography.md` → Hierarchy and Presentation Rule |
| `COLOR-CONTRAST-NORMAL` | `03_Color_System.md` → Contrast Rules |
| `COLOR-CONTRAST-LARGE` | `03_Color_System.md` → Contrast Rules |
| `COLOR-ACCENT-INVERSE-PROHIBITED` | `03_Color_System.md` → Required Pairing Decisions |
| `COLOR-FOCAL-AREA-GUIDANCE` | `03_Color_System.md` → Presentation Constraints |
| `COLOR-NOT-SOLE-CARRIER` | `03_Color_System.md` → Accessibility |
| `ICON-PRESENTATION-FAMILY` | `06_Iconography.md` when active; provisional application in `Components.md` |
| `CONTENT-TONE-VOICE` | `01_Brand_Core.md` → Tone & Voice |

These IDs are cross-reference aliases. The canonical values remain in their owner files.

---

## Lifecycle

Presentation System knowledge uses the Brand OS lifecycle:

```text
Draft
  ↓
In Review
  ↓
Release Candidate
  ↓
Active
  ↓
Deprecated
  ↓
Archived
```

| Status | Meaning |
|---|---|
| Draft | Incomplete and not ready for formal review |
| In Review | Under structured review; unresolved changes are expected |
| Release Candidate | Conceptually complete; implementation validation is still required |
| Active | Approved, implemented, validated, and safe for normal use |
| Deprecated | Retained temporarily but should not be used for new work |
| Archived | Historical record; not an operational source |

`Git Ready` is not a lifecycle state.

This version remains `Release Candidate` until Golden Deck validation is complete.

---

## Component and Pattern Maturity

Components and Patterns use:

```text
draft
candidate
stable
deprecated
```

`stable` requires:

- Documented purpose and contract
- At least one implementation
- Accessibility review
- Platform test evidence
- Known limitations
- Examples
- No unresolved P0 issue

No component or pattern in version `0.9.0` should be assumed stable solely because it is documented.

---

## Required Reading Order

```text
Brand Core
  ↓
Color System
  ↓
Typography System
  ↓
Presentation / README
  ↓
Presentation / Thinking
  ↓
Presentation / Content
  ↓
Presentation / Accessibility
  ↓
Presentation / Layout
  ↓
Presentation / Components
  ↓
Presentation / Patterns
  ↓
Presentation / AI Generation, when AI is used
  ↓
Presentation / Release Gates
  ↓
Presentation / Audit Checklist, when required
```

Do not begin with Patterns or tool templates. A pattern accelerates a resolved communication decision; it does not replace thinking.

---

## Platform Independence

Platform implementations may differ in canvas, grid controls, fonts, master systems, export behavior, animation support, and editability.

They must preserve:

- Audience intent
- Governing message
- Content integrity
- Narrative sequence
- Slide reading order
- Information relationships
- Semantic component roles
- Typography hierarchy
- Color meaning
- Accessibility
- Source traceability
- Editability appropriate to the intended workflow

---

## Review Strategy

Use three levels of review:

```text
Fast Gate
  ↓
Risk-based Audit
  ↓
Full Audit
```

- `Fast Gate`: required for every deliverable through [`Release_Gates.md`](./Release_Gates.md).
- `Risk-based Audit`: required when content, audience, platform, accessibility, or business risk is elevated.
- `Full Audit`: required for system templates, executive-critical work, regulated content, major public artifacts, and Golden Deck validation.

---

## Golden Deck Validation

Before version `1.0.0 / Active`, validate at least:

1. **Live Decision Deck**
   - Low-to-medium density
   - Live consumption
   - Decision session

2. **Read-ahead UX / Research Deck**
   - High evidence density
   - Self-guided consumption
   - Reference or read-ahead role

3. **Cross-platform Reference Deck**
   - PowerPoint → Google Slides → PDF
   - Typography, layout, source, accessibility, and editability checks

Each validation record must include:

- Release Gate result
- Audit score or findings
- Platform conversion issues
- Typography failures
- AI interpretation failures
- Accessibility exceptions
- Known limitations
- Improvement history

Documentation alone does not make the system Active. Implementation and validation do.

---

## Release Position

This version is suitable for controlled use and structured review.

It is not yet Active because:

- Design Tokens are not yet active
- Iconography is not yet fully canonical
- Golden Deck validation is incomplete
- Platform implementation evidence is incomplete
- Stable component and pattern status has not been earned

The target for `1.0.0 / Active` is a validated operating standard, not merely a completed document set.
