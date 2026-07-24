# Presentation Patterns

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

Presentation Patterns define reusable communication arrangements for recurring presentation problems.

Patterns are not tool templates.

Namespace:

```text
Presentation/Pattern/{Name}
```

Example:

```text
Presentation/Pattern/Comparison
```

Implemented deck assets belong under:

```text
templates/presentation/
```

Example:

```text
Presentation/Template/ExecutiveDecisionDeck
```

---

## Pattern Contract

Every Pattern must include:

```yaml
name:
namespace:
purpose:
status: draft | candidate | stable | deprecated
owner:
maintainer:
introduced_in:
audience_need:
narrative_role:
required_inputs:
recommended_components:
density:
content_rules:
accessibility_requirements:
platform_support:
tested_in:
accessibility_status:
examples:
known_limitations:
prohibited_use:
replaced_by:
```

All version `0.9.0` Patterns are `candidate`.

---

## Pattern Selection

Select a Pattern after:

- Audience
- Purpose and Expected Outcome
- Governing Message
- Content Architecture
- Narrative Architecture
- Slide Architecture

Do not start from a Pattern library.

A Pattern is appropriate when it solves a recurring communication relationship. It should not be selected only to make adjacent slides look different.

---

## Cover

### Namespace

```text
Presentation/Pattern/Cover
```

### Purpose

Establish identity, subject, context, and ownership.

### Required Content

- Presentation title
- Organization or project
- Date or version
- Owner or presenter when relevant
- Confidentiality when required

### Recommended Components

- Title
- Image when meaningful
- Metadata

### Prohibited Use

- Generic technology decoration
- Long executive summary
- Unsupported claim as a slogan

---

## Agenda

### Namespace

```text
Presentation/Pattern/Agenda
```

### Purpose

Explain the reasoning path or session structure.

An Agenda should communicate sequence and purpose, not merely list chapter names.

For workshops and decisions, include interaction or decision points.

---

## Chapter

### Namespace

```text
Presentation/Pattern/Chapter
```

### Purpose

Create a meaningful transition in Narrative Architecture.

Use a chapter message, not only a category label, when the transition advances an argument.

---

## Problem

### Namespace

```text
Presentation/Pattern/Problem
```

### Purpose

Explain a material gap, barrier, risk, or unmet need.

### Required Logic

```text
Current state
  ↓
Evidence
  ↓
Impact
  ↓
Why action is required
```

### Recommended Components

- Metric
- Flow
- Comparison
- Callout
- Chart

### Prohibited Use

- Emotional exaggeration without evidence
- Problem statements without impact
- Blaming people when the issue is systemic

---

## Insight

### Namespace

```text
Presentation/Pattern/Insight
```

### Purpose

Reveal a non-obvious conclusion derived from evidence.

### Required Logic

```text
Observation
  ↓
Interpretation
  ↓
Implication
```

An Insight is not a restated data point.

---

## Solution

### Namespace

```text
Presentation/Pattern/Solution
```

### Purpose

Explain how a proposed response addresses the defined problem.

### Required Logic

```text
Problem requirement
  ↓
Solution mechanism
  ↓
Expected outcome
  ↓
Evidence or feasibility
```

A solution must not appear before the audience understands the problem and evaluation criteria.

---

## Before and After

### Namespace

```text
Presentation/Pattern/BeforeAfter
```

### Purpose

Show a meaningful transformation.

Requirements:

- Same comparison axis
- Same scope
- Same unit or basis
- Clear change mechanism
- Honest limitations

Do not use Before / After when the two states are not comparable.

---

## Comparison

### Namespace

```text
Presentation/Pattern/Comparison
```

### Purpose

Enable evaluation, choice, or understanding of difference.

### Required Content

- Compared entities
- Shared criteria
- Evidence
- Trade-offs
- Focal difference
- Implication or recommendation

### Recommended Components

- Comparison
- Table
- Chart
- Metric
- Callout

A Pattern may use a Component with the same conceptual name. Namespaces keep the levels distinct.

---

## Decision

### Namespace

```text
Presentation/Pattern/Decision
```

### Purpose

Enable a decision owner to approve, reject, prioritize, or choose.

### Required Content

- Decision required
- Decision owner
- Deadline
- Options
- Criteria
- Recommendation
- Trade-offs
- Risks
- Consequence of delay
- Next action

### Recommended Components

- Comparison
- Callout
- Metric
- Table
- Roadmap

Do not hide the ask in a Summary or Closing slide.

---

## Process

### Namespace

```text
Presentation/Pattern/Process
```

### Purpose

Explain how work is performed.

### Required Logic

- Trigger
- Inputs
- Stages
- Actors
- Outputs
- Feedback
- Exception path when material

Do not force iterative work into a false linear sequence.

---

## Timeline

### Namespace

```text
Presentation/Pattern/Timeline
```

### Purpose

Explain chronological development or event sequence.

Use for factual or planned time relationships. Label uncertainty and symbolic spacing.

---

## Roadmap

### Namespace

```text
Presentation/Pattern/Roadmap
```

### Purpose

Explain how an intended future state will be achieved.

Required content:

- Horizon
- Workstreams
- Milestones
- Owners
- Dependencies
- Decision points
- Risks
- Confidence

A Roadmap is a governance artifact, not a decorative arrow.

---

## KPI

### Namespace

```text
Presentation/Pattern/KPI
```

### Purpose

Explain performance against a target or expectation.

Required content:

- Metric definition
- Current value
- Comparator or target
- Time period
- Trend
- Interpretation
- Owner
- Action when off track

A collection of large numbers is not a KPI Pattern.

---

## Pricing

### Namespace

```text
Presentation/Pattern/Pricing
```

### Purpose

Explain price, value, scope, conditions, and trade-offs.

Required content:

- Offer
- Included scope
- Price and unit
- Billing period
- Conditions
- Exclusions
- Comparison basis
- Recommended option when appropriate

Do not use visual emphasis to hide conditions.

---

## Organization

### Namespace

```text
Presentation/Pattern/Organization
```

### Purpose

Explain roles, accountability, interfaces, or governance.

Use the relationship that matters:

- Reporting
- Decision rights
- Collaboration
- Escalation
- Ownership
- Capability

Do not use an organization chart when the real question is decision ownership.

---

## Summary

### Namespace

```text
Presentation/Pattern/Summary
```

### Purpose

Reinforce the Governing Message and material implications.

A Summary should not merely repeat chapter titles.

It should state:

- What is now understood
- What matters
- What is decided or proposed
- What happens next

---

## Closing

### Namespace

```text
Presentation/Pattern/Closing
```

### Purpose

Complete the communication and make the expected next action visible.

Possible content:

- Decision request
- Commitment
- Next step
- Contact
- Final principle

Avoid decorative “Thank you” slides when an action remains unclear.

---

## Pattern Composition

A slide Pattern may use:

```text
One primary component
+ supporting components
```

A deck Pattern may contain several slide Patterns in a coherent Narrative Architecture.

Patterns must not prescribe raw colors, font sizes, or tool effects. They reference canonical systems.

---

## Platform Support

Each implementation must record:

```yaml
pattern:
platform:
status:
tested_on:
conversion_test:
accessibility_status:
example:
known_limitations:
```

Pattern implementation is distinct from Pattern definition.

---

## Template Boundary

A Template is an implemented asset that may include:

- Tool theme or master
- Layouts
- Text styles
- Color mappings
- Components
- Pattern examples
- Placeholder behavior
- Export settings
- Accessibility guidance

Templates must:

- Reference the Pattern and Component namespaces they implement
- Record platform and version
- Preserve editability
- Avoid creating new canonical rules
- Remain subordinate to Brand OS

Future location:

```text
templates/presentation/
├── powerpoint/
├── google-slides/
├── keynote/
├── canva/
├── figma-slides/
└── ai/
```

---

## Contribution

A new Pattern requires:

1. A recurring audience or communication need
2. A defined narrative role
3. Required inputs
4. Pattern Contract
5. Component mapping
6. Content guidance
7. Accessibility requirements
8. Example
9. Platform validation plan
10. Brand Director approval before stable status

Visual arrangement alone is not a Pattern.
