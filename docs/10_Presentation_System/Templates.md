# Presentation Templates

> Version: 1.0.0  
> Status: Active  
> Owner: LINKGENT Brand OS  
> Last Updated: 2026-07-24

---

## Purpose

Presentation Templates define reusable communication patterns for recurring presentation purposes.

A template is not a fixed visual composition.

It is a structured relationship among:

- Audience need
- Communication purpose
- Required information
- Message logic
- Appropriate components
- Density
- Review criteria

Templates accelerate execution after thinking is complete. They must never replace audience definition, purpose definition, information architecture, or story design.

---

## Inheritance

Every template must inherit:

- Brand principles from [`../01_Brand_Core.md`](../01_Brand_Core.md)
- Color semantics from [`../03_Color_System.md`](../03_Color_System.md)
- Typography roles from [`../04_Typography.md`](../04_Typography.md)
- Presentation reasoning from [`Thinking.md`](./Thinking.md)
- Layout rules from [`Layout.md`](./Layout.md)
- Component definitions from [`Components.md`](./Components.md)

A template may implement upper-level rules. It must not redefine them.

---

## Template Philosophy

### Pattern, Not Page

A template describes the communication job a slide must perform.

Preferred:

```text
Problem pattern:
Establish the current condition, affected audience,
evidence, impact, and reason action is required.
```

Avoid:

```text
Put three red cards under a large warning icon.
```

### Content Determines Form

Use a template only when the information relationship matches the pattern.

Do not force content into a familiar layout merely because it is available.

### Stable Logic, Flexible Expression

The same template may appear differently across tools, aspect ratios, and presentation modes.

It must preserve:

- Purpose
- Required information roles
- Message hierarchy
- Reading order
- Component semantics
- Accessibility

### Templates Are Starting Constraints

Templates should reduce arbitrary decisions while leaving enough flexibility to express the actual content.

Do not create slide variety by rotating through unrelated templates.

---

## Template Contract

Each template defines:

| Property | Meaning |
|---|---|
| Purpose | Communication outcome |
| Required content | Information necessary for the pattern to work |
| Message logic | Reasoning relationship among the content |
| Preferred components | Recommended semantic structures |
| Density | Typical information density mode |
| Variants | Meaningful adaptations |
| Avoid | Common failure modes |

Recommended naming:

```text
Presentation/Template/Pattern
```

Example:

```text
Presentation/Template/Comparison
```

---

## Cover

### Purpose

Establish what the presentation is about, why it matters, and who or what context it belongs to.

### Required Content

- Presentation title
- Optional thesis or framing statement
- Organization, project, or context
- Date or version when relevant
- Presenter or owner when relevant

### Message Logic

```text
Identity
  + subject
  + relevance
```

### Preferred Components

- Title
- Image, only when essential
- Minimal metadata

### Density

Statement

### Variants

- Title-led
- Thesis-led
- Image-led
- Event or session cover

### Avoid

- Generic decorative imagery
- Long subtitles
- Excessive logos
- Several competing brand colors
- A cover that does not establish the subject clearly

---

## Agenda

### Purpose

Orient the audience to the structure, decision path, or working sequence.

### Required Content

- Major sections
- Meaningful order
- Optional current position
- Optional decision or workshop stages

### Message Logic

```text
Where we are going
  + how the parts connect
```

### Preferred Components

- Process
- Timeline
- Structured list
- Section navigation

### Density

Standard

### Variants

- Narrative agenda
- Decision path
- Workshop flow
- Read-ahead contents

### Avoid

- Listing every slide
- Using vague chapter labels
- Presenting an agenda when the story is short and self-evident
- Different visual treatment for every item

---

## Chapter

### Purpose

Mark a major transition in the presentation story.

### Required Content

- Chapter title
- Optional chapter message
- Optional chapter number or navigation context

### Message Logic

```text
Previous understanding
  → new question or phase
```

### Preferred Components

- Section
- Title
- Optional minimal image or diagram fragment

### Density

Statement

### Variants

- Numbered chapter
- Message-led transition
- Question-led transition

### Avoid

- Chapter slides for minor topic changes
- Long explanatory content
- Decorative visual interruption
- Color changes without structural meaning

---

## Problem

### Purpose

Establish a meaningful current-state issue that requires attention or action.

### Required Content

- Current condition
- Affected audience or system
- Evidence
- Impact
- Scope or boundary
- Reason action is required now

### Message Logic

```text
Observed condition
  → consequence
  → urgency or significance
```

### Preferred Components

- Chart
- Metric
- Flow
- Image evidence
- Callout
- Comparison

### Density

Standard or Analytical

### Variants

- User problem
- Business problem
- System problem
- Risk or failure condition
- Opportunity gap

### Avoid

- Stating only a symptom
- Exaggerating urgency without evidence
- Using warning colors as decoration
- Mixing several unrelated problems
- Presenting the solution before the problem is understood

---

## Insight

### Purpose

Reveal a meaningful interpretation that changes understanding.

### Required Content

- Observation or evidence
- Pattern or relationship
- Interpretation
- Implication
- Confidence or limitation when relevant

### Message Logic

```text
Evidence
  → pattern
  → meaning
  → implication
```

### Preferred Components

- Chart
- Comparison
- Quote
- Image evidence
- Callout
- Diagram

### Density

Analytical

### Variants

- Research insight
- Data insight
- Behavioral insight
- Strategic insight
- Market insight

### Avoid

- Calling a fact an insight
- Repeating the chart title without interpretation
- Presenting opinion as evidence
- Hiding uncertainty
- Using a visually dramatic statement without support

---

## Solution

### Purpose

Explain the proposed response and why it addresses the defined problem or opportunity.

### Required Content

- Solution definition
- Target problem or opportunity
- Mechanism of value
- Audience benefit
- Scope
- Evidence or rationale
- Constraints or dependencies

### Message Logic

```text
Need
  → response
  → mechanism
  → value
```

### Preferred Components

- Flow
- Process
- System diagram
- Card group
- Comparison
- Metric
- Image or prototype evidence

### Density

Standard or Analytical

### Variants

- Product solution
- Service solution
- Operating model
- Policy or process response
- Design recommendation

### Avoid

- Feature lists without value logic
- Claims that do not connect to the problem
- Hiding implementation constraints
- Using conceptual imagery instead of explaining how the solution works

---

## Before After

### Purpose

Make a change in state, experience, performance, or structure visible.

### Required Content

- Stable baseline
- Before state
- After or target state
- Shared comparison dimensions
- Meaningful difference
- Mechanism or reason for change

### Message Logic

```text
Current state
  → intervention
  → changed state
  → implication
```

### Preferred Components

- Comparison
- Image pair
- Process pair
- Metric pair
- Table

### Density

Standard or Analytical

### Variants

- Current and target
- Existing and proposed
- Without and with
- Baseline and outcome

### Avoid

- Different scales or crops
- Comparing unrelated conditions
- Showing improvement without a stable baseline
- Over-simplifying trade-offs
- Using color alone to label before and after

---

## Comparison

### Purpose

Support evaluation, prioritization, or choice among alternatives.

### Required Content

- Compared items
- Shared criteria
- Evidence
- Trade-offs
- Decision relevance
- Recommendation when appropriate

### Message Logic

```text
Decision
  → criteria
  → differences
  → trade-offs
  → implication
```

### Preferred Components

- Comparison
- Table
- Chart
- Card group
- Callout

### Density

Analytical

### Variants

- Two-option comparison
- Multi-option matrix
- Feature comparison
- Strategic alternatives
- Pros and trade-offs

### Avoid

- Different criteria for each option
- Biased language replacing evidence
- Checkmark grids without degree or quality
- Highlighting the preferred option before explaining criteria
- Decorative visual differences unrelated to the decision

---

## Process

### Purpose

Explain an ordered method, sequence of actions, or transformation.

### Required Content

- Start condition
- Ordered stages
- Stage purpose
- Inputs and outputs when relevant
- Owners or decisions when relevant
- End condition

### Message Logic

```text
Input
  → stages
  → output
```

### Preferred Components

- Process
- Flow
- Timeline
- Callout

### Density

Standard

### Variants

- Linear process
- Cyclical process
- Branching process
- Human and AI workflow
- Current and proposed process

### Avoid

- Forcing a non-linear system into a line
- Too many stages
- Vague verb labels
- Decorative chevrons without meaningful transformation
- Hiding decision points or ownership

---

## Timeline

### Purpose

Communicate what happened or will happen in chronological order.

### Required Content

- Time range
- Key events or periods
- Current position when relevant
- Meaningful milestones
- Optional status

### Message Logic

```text
Past
  → present
  → future
```

### Preferred Components

- Timeline
- Metric
- Callout

### Density

Standard or Reference

### Variants

- Historical timeline
- Delivery schedule
- Event sequence
- Decision chronology

### Avoid

- Equal spacing that implies false duration
- Too many minor events
- Mixing historical facts and future commitments without distinction
- Decorative time axes

---

## Roadmap

### Purpose

Communicate intended progression, priorities, outcomes, and dependencies across time or phases.

### Required Content

- Strategic horizon or phases
- Outcomes or capabilities
- Workstreams
- Dependencies
- Decision gates
- Confidence or commitment level
- Current phase

### Message Logic

```text
Current capability
  → phased change
  → future outcome
```

### Preferred Components

- Roadmap
- Timeline
- Process
- Callout
- Metric

### Density

Analytical or Reference

### Variants

- Outcome roadmap
- Capability roadmap
- Product roadmap
- Transformation roadmap
- Now / Next / Later

### Avoid

- Treating every task as a roadmap item
- False date precision
- Mixing outcomes and tasks at the same level
- Hiding dependencies
- Using the roadmap as a project plan substitute

---

## KPI

### Purpose

Communicate performance against a goal and enable interpretation or action.

### Required Content

- KPI definition
- Current value
- Unit
- Time period
- Target or baseline
- Trend or variance
- Interpretation
- Action or risk when relevant

### Message Logic

```text
Goal
  → actual
  → variance
  → reason
  → action
```

### Preferred Components

- Metric
- Chart
- Table
- Callout

### Density

Analytical

### Variants

- Single focal KPI
- KPI scorecard
- Trend and target
- Variance review

### Avoid

- Metrics without targets or context
- Large numbers with no interpretation
- Coloring all positive values green without defined meaning
- Too many KPIs on one live slide
- Decorative gauges

---

## Pricing

### Purpose

Explain pricing structure, included value, comparison, and decision implications.

### Required Content

- Offer or plan names
- Price and billing unit
- Included scope
- Important differences
- Conditions or exclusions
- Recommended option when appropriate
- Next action

### Message Logic

```text
Need or segment
  → offer
  → value
  → price
  → choice
```

### Preferred Components

- Comparison
- Card group
- Table
- Metric
- Callout

### Density

Analytical

### Variants

- Tier comparison
- Cost breakdown
- Current and proposed pricing
- Investment and return

### Avoid

- Hiding conditions in unreadable captions
- Making the recommended option visually dominant without rationale
- Comparing prices without equivalent units
- Using decorative badges as the only recommendation signal
- Presenting price without value context

---

## Organization

### Purpose

Explain roles, relationships, ownership, governance, or team structure.

### Required Content

- Organizational scope
- Roles or units
- Reporting, collaboration, or decision relationships
- Ownership
- Boundaries
- Optional vacancies or future state

### Message Logic

```text
Purpose
  → roles
  → relationships
  → accountability
```

### Preferred Components

- Hierarchy diagram
- Flow
- Card group
- Table
- Callout

### Density

Standard or Reference

### Variants

- Formal organization chart
- Project team
- Governance model
- Responsibility map
- Current and future organization

### Avoid

- Showing hierarchy when the relationship is collaborative
- Using boxes and lines without explaining ownership
- Fitting every individual onto one live slide
- Mixing role, person, and department levels without distinction
- Decorative portraits that reduce clarity

---

## Summary

### Purpose

Reinforce the essential understanding and prepare the audience for decision or action.

### Required Content

- Deck thesis
- Two to four essential conclusions
- Decision, recommendation, or implication
- Optional risk or condition
- Next step

### Message Logic

```text
What we learned
  → what it means
  → what should happen
```

### Preferred Components

- Title
- Callout
- Metric
- Structured list
- Comparison

### Density

Standard

### Variants

- Executive summary
- Key takeaways
- Recommendation summary
- Decision summary

### Avoid

- Repeating slide titles without synthesis
- Introducing new evidence
- Listing too many takeaways
- Ending without a clear implication
- Replacing the conclusion with a generic thank-you message

---

## Closing

### Purpose

Create a clear final state for the audience: decision, action, reflection, contact, or transition to discussion.

### Required Content

One of the following:

- Decision required
- Next action
- Commitment
- Discussion question
- Contact or follow-up path
- Final thesis

### Message Logic

```text
Understanding
  → decision or action
```

### Preferred Components

- Title
- Callout
- Metric
- Minimal contact information

### Density

Statement

### Variants

- Decision request
- Call to action
- Final message
- Discussion prompt
- Contact close

### Avoid

- A generic “Thank you” as the only message
- New complex information
- Several competing calls to action
- Decorative imagery unrelated to the conclusion
- Ending without ownership or next timing when action is required

---

## Deck Assembly Patterns

Templates may be combined into a story. The following are reference patterns, not mandatory sequences.

### Decision Deck

```text
Cover
  → Decision Required
  → Context
  → Problem or Opportunity
  → Criteria
  → Comparison
  → Recommendation
  → Risks and Dependencies
  → Roadmap
  → Decision and Next Action
```

### Proposal Deck

```text
Cover
  → Audience Need
  → Problem
  → Insight
  → Solution
  → Value
  → Process
  → Roadmap
  → Pricing or Investment
  → Summary
  → Closing
```

### Research or UX Findings Deck

```text
Cover
  → Purpose and Scope
  → Method
  → Context
  → Findings
  → Insight
  → Impact
  → Recommendation
  → Priority
  → Next Validation
```

### Operating Review

```text
Cover
  → Goal
  → KPI
  → Progress
  → Variance
  → Root Cause
  → Risk
  → Priority
  → Next Action
```

### Training Deck

```text
Cover
  → Learning Goal
  → Context
  → Concept
  → Example
  → Process
  → Practice
  → Review
  → Application
```

---

## Template Selection Process

AI and humans should select templates using this sequence:

```text
Slide purpose
  ↓
Information relationship
  ↓
Required evidence
  ↓
Density mode
  ↓
Template pattern
  ↓
Component composition
  ↓
Visual implementation
```

Do not select a template from a visual gallery before the slide purpose is defined.

---

## Template Governance

Create a new template only when:

- A recurring communication purpose is not represented
- The required information relationship differs materially
- Existing templates repeatedly require the same documented exception
- The pattern can be explained semantically across tools
- The pattern improves consistency and comprehension

Do not create a new template only because:

- A new visual style is desired
- A single project used a unique layout
- A tool introduced a new feature
- A trend makes the current templates feel less novel

Every new template must document:

- Purpose
- Required content
- Message logic
- Preferred components
- Density
- Variants
- Failure modes

---

## Final Principle

```text
A template should accelerate correct thinking,
not accelerate decoration.
```
