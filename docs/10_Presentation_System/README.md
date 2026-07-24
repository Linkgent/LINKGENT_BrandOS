# Presentation System

> Version: 1.0.0  
> Status: Active  
> Owner: LINKGENT Brand OS  
> Last Updated: 2026-07-24

---

## Purpose

The LINKGENT Presentation System defines how structured thinking becomes communication that people can understand, discuss, and act upon.

A LINKGENT presentation is not a collection of visually polished slides.

It is **Communication Design for decision-making**:

```text
Logical thinking
  ↓
Information architecture
  ↓
Story
  ↓
Visual communication
  ↓
Shared understanding
  ↓
Decision and action
```

The system applies across:

- PowerPoint
- Google Slides
- Keynote
- Canva
- Figma Slides
- Gamma
- AI presentation tools
- Future presentation environments

The same visual output is not required in every tool. The same intent, hierarchy, meaning, accessibility, and quality standard are required.

---

## Definition

At LINKGENT, a presentation is:

> A structured communication system that transforms complex information into shared understanding and enables an audience to make a decision, align around meaning, or take action.

A presentation is not defined by its file format, slide software, template, animation, or visual style.

It is defined by the quality of the decisions that precede visual production.

---

## Inheritance

This is an Applied System within LINKGENT Brand OS.

It inherits and applies the following canonical sources:

1. [`../../CONSTITUTION.md`](../../CONSTITUTION.md)
2. [`../01_Brand_Core.md`](../01_Brand_Core.md)
3. [`../03_Color_System.md`](../03_Color_System.md)
4. [`../04_Typography.md`](../04_Typography.md)
5. `../05_Design_Tokens.md` when defined
6. `../06_Iconography.md` when defined
7. `../09_Layout_System.md` when defined
8. `../13_AI_Generation_Rules.md` when defined

This system applies those foundations to presentation communication. It does not redefine their canonical meanings.

When a rule conflicts with an upper-level source, the upper-level source takes precedence.

---

## Brand Core Principles in Presentation

### Structure First

Visual design must reveal the logic, priority, relationship, and sequence of information.

A polished layout must never compensate for weak thinking.

### UX Before UI

The audience experience comes before the appearance of the slide.

The system must consider:

- What the audience already knows
- What they need to understand
- What may confuse or concern them
- What decision or action is expected
- How the presentation will be viewed and used

### Beauty Through Purpose

Beauty is not removed from presentation design.

Beauty emerges when logic, message, typography, spacing, color, imagery, and composition support the same purpose.

### Human × AI Collaboration

Humans provide context, judgment, responsibility, ethics, and final direction.

AI may accelerate research, structuring, story development, drafting, layout exploration, production, and review.

AI must not begin with visual generation before understanding the audience, purpose, message, and information structure.

---

## Presentation Design Priority

LINKGENT presentations use the following decision order:

```text
Audience
  ↓
Purpose
  ↓
Message
  ↓
Information Architecture
  ↓
Story
  ↓
Layout
  ↓
Typography
  ↓
Color
  ↓
Decoration
```

Higher layers govern lower layers.

When a lower-layer choice conflicts with a higher-layer need, the higher layer wins.

Examples:

- Readability takes precedence over a visually dramatic composition.
- Message clarity takes precedence over fitting all content onto one slide.
- Information structure takes precedence over template symmetry.
- Audience needs take precedence over the presenter's preferred style.
- Accessibility takes precedence over visual subtlety.

---

## Presentation Pyramid

Presentation quality is determined primarily by the upper layers of the system.

```text
Brand
  ↓
Information Architecture
  ↓
Story
  ↓
Layout
  ↓
Typography
  ↓
Color
  ↓
Decoration
```

### Interpretation

- **Brand** determines how LINKGENT thinks, communicates, and earns trust.
- **Information Architecture** determines what belongs, what matters, and how information relates.
- **Story** determines the order in which understanding develops.
- **Layout** makes the structure visible.
- **Typography** reveals hierarchy and reading order.
- **Color** communicates meaning, state, grouping, and focus.
- **Decoration** may refine expression only after every upper layer is resolved.

A weak presentation cannot be repaired at the bottom of the pyramid.

Changing colors, fonts, icons, shadows, or templates does not solve an unclear purpose, weak argument, or disorganized story.

---

## Brand Personality

Every LINKGENT presentation should feel:

- Structured
- Intelligent
- Reliable
- Beautiful
- Minimal
- Sophisticated
- Human-centered
- Future-ready

It should not feel:

- Decorative without meaning
- Visually loud without purpose
- Trend-driven
- Template-dependent
- Artificially futuristic
- Dense because editing was avoided
- Minimal at the expense of understanding
- Confident without evidence

---

## System Architecture

```text
10_Presentation_System/
├── README.md
├── Thinking.md
├── Layout.md
├── Components.md
├── Templates.md
├── AI_Generation.md
└── Checklist.md
```

### File Responsibilities

| File | Canonical Responsibility |
|---|---|
| [`README.md`](./README.md) | Definition, scope, inheritance, philosophy, system structure |
| [`Thinking.md`](./Thinking.md) | Audience, purpose, message, information architecture, story, density, reasoning |
| [`Layout.md`](./Layout.md) | Safe area, grid, whitespace, alignment, rhythm, balance, density application |
| [`Components.md`](./Components.md) | Reusable semantic presentation components and composition rules |
| [`Templates.md`](./Templates.md) | Reusable communication patterns for common presentation purposes |
| [`AI_Generation.md`](./AI_Generation.md) | Presentation-specific AI reasoning, generation, adaptation, and review rules |
| [`Checklist.md`](./Checklist.md) | Final quality gates and review criteria |

---

## Required Reading Order

Before creating or reviewing a LINKGENT presentation:

```text
Brand Core
  ↓
Color System
  ↓
Typography System
  ↓
Presentation System / Thinking
  ↓
Presentation System / Layout
  ↓
Presentation System / Components
  ↓
Presentation System / Templates
  ↓
Presentation System / AI Generation, when AI is used
  ↓
Presentation System / Checklist
```

Do not begin with `Templates.md`.

A template is an implementation pattern, not a substitute for thinking.

---

## Platform Independence

The Presentation System defines semantic intent before tool implementation.

Preferred definition:

```text
Use a Comparison pattern with one focal difference,
a shared evaluation axis, and direct labels.
```

Avoid tool-bound definition:

```text
Use SmartArt style 3 with a blue gradient.
```

Platform implementations may differ in:

- Canvas size
- Master and theme capabilities
- Font availability
- Grid controls
- Component systems
- Animation support
- Export behavior
- AI generation behavior

They must preserve:

- Audience intent
- Message hierarchy
- Reading order
- Information relationships
- Semantic component roles
- Typography hierarchy
- Color meaning
- Accessibility
- Editability

---

## Presentation Types

This system supports, but is not limited to:

- Executive decision decks
- Strategy presentations
- Proposals
- Sales presentations
- Product and service explanations
- Research reports
- UX findings
- Project kickoffs
- Operating reviews
- Training materials
- Conference presentations
- Internal alignment decks
- AI-generated first drafts
- Read-ahead documents

Different presentation types may use different density, pacing, and evidence levels. They must still follow the same thinking hierarchy.

---

## Presentation Modes

A presentation must identify its primary mode.

| Mode | Primary Use | Design Implication |
|---|---|---|
| Live | Spoken presentation with visual support | Low-to-medium density, strong pacing, rapid comprehension |
| Read-ahead | Independent reading before or after a meeting | Higher evidence density, explicit context, complete labels |
| Decision | Enable approval, prioritization, or choice | Clear options, criteria, trade-offs, recommendation, next action |
| Workshop | Facilitate discussion and participation | Flexible structures, prompts, working areas, visible decisions |
| Reference | Preserve detailed information for later use | Dense but highly structured, searchable, source-rich, often appendix-led |

Do not mix modes unintentionally.

A live slide should not become a compressed report page. A read-ahead document should not depend on spoken explanation to make sense.

---

## Canonical Presentation Principle

```text
Do not design slides.
Design understanding.
```

The slide is a temporary container.

The system exists to make thinking visible, reduce cognitive burden, support trust, and move people toward meaningful decisions and action.
