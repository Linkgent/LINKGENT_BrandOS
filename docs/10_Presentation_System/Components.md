# Presentation Components

> Version: 1.0.0  
> Status: Active  
> Owner: LINKGENT Brand OS  
> Last Updated: 2026-07-24

---

## Purpose

Presentation Components define reusable semantic structures for expressing recurring information relationships.

A component is not a decorative shape.

It is a repeatable communication pattern with:

- A defined purpose
- A defined information role
- A predictable anatomy
- A clear hierarchy
- Usage conditions
- Constraints
- Accessible behavior

Components should help people and AI create presentations that are consistent, editable, explainable, and scalable across tools.

---

## Inheritance

Every component must inherit:

- Brand principles from [`../01_Brand_Core.md`](../01_Brand_Core.md)
- Semantic color roles from [`../03_Color_System.md`](../03_Color_System.md)
- Typography roles from [`../04_Typography.md`](../04_Typography.md)
- Thinking rules from [`Thinking.md`](./Thinking.md)
- Layout rules from [`Layout.md`](./Layout.md)

When `../05_Design_Tokens.md` and `../06_Iconography.md` are defined, component implementations must adopt their canonical tokens and icon rules.

---

## Component Philosophy

### Meaning Before Shape

Select a component from the information relationship, not from visual preference.

```text
Information role
  ↓
Relationship
  ↓
Component
  ↓
Variant
  ↓
Visual implementation
```

### Components, Not Containers

A rectangle around content does not automatically create a component.

A component exists only when the boundary communicates a meaningful group, state, comparison, or reusable behavior.

### Minimum Necessary System

Use the smallest number of component types needed to express the story.

Do not create a different card, callout, chart style, or title pattern for every slide.

### Editable by Default

Components should remain editable in the destination tool.

Prefer:

- Live text
- Native tables
- Native charts when reliable
- Editable vector shapes
- Structured groups
- Shared styles or components

Avoid rasterizing structured information unless required by the production environment.

---

## Component Contract

Every component implementation should define:

| Property | Definition |
|---|---|
| Name | Semantic component name |
| Purpose | Communication problem the component solves |
| Information role | Claim, evidence, context, action, navigation, status, or reference |
| Anatomy | Required and optional parts |
| Variants | Meaningful alternatives, not cosmetic permutations |
| Typography | Approved semantic typography roles |
| Color | Approved semantic color roles |
| Layout behavior | Grid span, alignment, spacing, and responsive adaptation |
| Accessibility | Contrast, reading order, labeling, and non-color cues |
| Prohibited use | Conditions where the component should not be used |

Recommended naming:

```text
Presentation/Component/Variant
```

Examples:

```text
Presentation/Card/Standard
Presentation/Comparison/TwoColumn
Presentation/Metric/Focal
Presentation/Callout/Warning
```

Do not name components by appearance alone.

Avoid:

```text
Blue Rounded Box
Big Number Block
Fancy Timeline
```

---

## Title

### Purpose

The Title component establishes the primary message and reading entry point of a slide.

### Anatomy

- Optional chapter or context label
- Primary message title
- Optional supporting subtitle
- Optional status, date, or scope metadata

### Rules

- Use a message-led title for analytical, persuasive, and decision slides.
- Use a topic title only for cover, chapter, agenda, or reference contexts.
- Keep one clear title anchor across the deck.
- Use `Typography/Heading/H1` or the appropriate semantic role.
- Keep supporting text visibly subordinate.
- Do not add a decorative line, icon, or label unless it improves orientation.

### Avoid

- Titles that only repeat the template name
- Titles that do not match the evidence
- Two competing titles
- Excessive all-caps labels
- Title bars that consume space without structural value

---

## Section

### Purpose

The Section component marks a major narrative transition and helps the audience understand where they are in the story.

### Anatomy

- Chapter number, optional
- Chapter title
- Short chapter message, optional
- Optional navigation context

### Rules

- Use for meaningful changes in topic, argument, phase, or decision stage.
- Keep density low.
- Use Primary or `background.inverse` only as a controlled structural context.
- Preserve strong contrast and generous safe area.
- Use consistent chapter naming throughout the deck.

### Avoid

- A section divider before every small topic
- Decorative chapter slides that interrupt momentum
- Different colors for every chapter without semantic meaning
- Long explanatory paragraphs

---

## Card

### Purpose

A Card groups information that belongs together and can be understood as one semantic unit.

### Anatomy

- Optional label or icon
- Card title
- Primary content
- Optional metric, status, or supporting text
- Optional action or source

### Variants

- Standard
- Metric
- Status
- Selected
- Comparison item
- Reference

Variants must represent different information roles, not minor visual differences.

### Rules

- Use cards only when boundaries improve grouping or comparison.
- Keep internal hierarchy consistent across repeated cards.
- Use neutral surfaces and subtle borders by default.
- Use equal card height only when items are semantically comparable.
- Align titles, values, and supporting text across a card group.
- Use Accent for one selected or focal card, not every card.

### Avoid

- Putting every bullet in a separate card
- Using cards only to make a slide look designed
- Filling all cards with different colors
- Mixing different information structures in visually equal cards
- Excessive radius, shadow, or elevation

---

## Callout

### Purpose

A Callout isolates information that requires attention, interpretation, action, or qualification.

### Anatomy

- Optional semantic icon
- Label, optional
- Callout message
- Optional supporting explanation or action

### Variants

- Insight
- Recommendation
- Information
- Success
- Warning
- Error
- Assumption

### Rules

- Use a semantic variant based on meaning.
- Use the relevant Color System role.
- Combine color with text, icon, label, or position.
- Keep the callout shorter than the content it interprets.
- Use one primary callout per composition unless multiple statuses are genuinely required.

### Avoid

- Using Accent callouts for general decoration
- Treating every sentence as important
- Using warning or error colors without semantic meaning
- Placing a callout far from the content it explains

---

## Table

### Purpose

A Table supports precise lookup, comparison, categorization, and structured reference.

### Anatomy

- Title or message context
- Column headers
- Row labels
- Data cells
- Optional units
- Optional highlights or annotations
- Source and time period

### Rules

- Use a real table structure where the tool supports it.
- Define the comparison dimension clearly.
- Keep units, time periods, and number formats consistent.
- Align text left and numeric values by their numerical logic.
- Use spacing, typography, and borders before multiple fills.
- Use one focal row, column, or cell treatment when necessary.
- Keep headers distinct but not visually dominant over the slide message.
- Use direct labels and explain symbols.

### Avoid

- Building tables with spaces, tabs, or individually placed text boxes
- Coloring every row or column
- Using very small type to fit excessive data
- Mixing several units without clear labels
- Highlighting more cells than remain neutral
- Using a table when the message depends on a pattern better shown as a chart

---

## Chart

### Purpose

A Chart makes quantitative patterns, differences, distribution, composition, or change visible.

### Selection by Relationship

| Relationship | Preferred Chart Family |
|---|---|
| Change over time | Line or column |
| Comparison | Bar or column |
| Distribution | Histogram, dot plot, box plot, or ordered values |
| Composition | Stacked bar; pie or donut only for simple part-to-whole cases |
| Relationship between variables | Scatter plot |
| Progress toward target | Bar, bullet, or direct metric with target |
| Range or uncertainty | Interval, band, error bar, or scenario range |

### Anatomy

- Message-led title
- Plot area
- Scale and unit
- Direct labels or concise legend
- Focal series or point
- Annotation
- Source and time period

### Rules

- Start from the question the chart must answer.
- Use a truthful scale.
- Use a shared baseline when comparison requires it.
- Sort categories when order improves interpretation.
- Use neutrals for context and Accent for the focal series.
- Use direct labels where practical.
- Remove non-essential gridlines, borders, and effects.
- State the unit and time period.
- Preserve color meaning across the complete deck.
- Make the chart understandable in grayscale when practical.

### Avoid

- 3D charts
- Decorative perspective
- Dual axes without a strong and explicit reason
- Too many series
- Rainbow palettes
- Truncated axes that exaggerate difference without disclosure
- Pie charts with many categories
- Legends that force repeated visual searching
- Charts included only because data exists

---

## Timeline

### Purpose

A Timeline communicates events or states in chronological order.

### Anatomy

- Time axis
- Milestones or periods
- Labels
- Optional status or phase
- Optional current-position marker

### Rules

- Use a consistent direction.
- Represent time intervals proportionally when duration matters.
- If spacing is not proportional, state that the timeline is schematic.
- Distinguish completed, current, and future states using more than color alone.
- Limit milestones to those that support the slide message.
- Use direct labels close to each event.

### Avoid

- Equal spacing that falsely implies equal duration
- Too many minor dates
- Decorative curves that obscure sequence
- Mixing roadmap commitments with historical events without clear separation

---

## Roadmap

### Purpose

A Roadmap communicates intended progression, priorities, dependencies, and outcomes over time.

A roadmap is not merely a timeline of dates.

### Anatomy

- Time horizon or phase structure
- Workstreams
- Outcomes or capabilities
- Dependencies
- Decision gates
- Status, when relevant
- Assumptions or confidence level

### Rules

- Focus on outcomes before task lists.
- Distinguish commitment from aspiration.
- Show dependencies that materially affect sequence.
- Use consistent phase definitions.
- State whether timing is fixed, estimated, or directional.
- Keep the current phase visible.

### Avoid

- Presenting uncertain dates as commitments
- Filling the roadmap with every task
- Using color alone for status
- Mixing strategic outcomes and operational tasks at the same hierarchy level
- Calling a decorative arrow a roadmap

---

## Flow

### Purpose

A Flow communicates movement of information, people, value, or states through a system.

### Anatomy

- Start and end points
- Nodes
- Connections
- Direction
- Optional decisions, inputs, outputs, or loops

### Rules

- Make direction unmistakable.
- Use a consistent reading path.
- Label connections when the relationship is not obvious.
- Minimize line crossings.
- Distinguish primary flow from exceptions or feedback loops.
- Use Accent only for the focal path or critical transition.

### Avoid

- Arrows without defined meaning
- Decorative loops
- Several directions without an entry point
- Unequal nodes shown as equivalent
- Complex system maps when a simpler process is sufficient

---

## Process

### Purpose

A Process communicates a defined sequence of actions, stages, or transformations.

### Anatomy

- Process name
- Ordered stages
- Stage labels
- Optional owner, input, output, duration, or status
- Optional feedback loop

### Rules

- Use numbered or directional stages.
- Begin each stage label with a parallel grammatical form.
- Show inputs and outputs when they clarify transformation.
- Use equal visual weight only when stages are equivalent.
- Indicate loops or branching explicitly.
- Separate the current process from the proposed process when comparing change.

### Avoid

- Forcing a linear process when the system branches
- Using chevrons because the tool provides them
- Hiding ownership or decision points when they matter
- Using too many steps on one slide

---

## Comparison

### Purpose

A Comparison component makes similarities, differences, trade-offs, or choices explicit.

### Anatomy

- Compared items
- Shared dimensions or criteria
- Baseline or reference
- Evidence
- Focal difference
- Implication or recommendation

### Variants

- Two-column
- Before and after
- Option matrix
- Feature comparison
- Current and target state
- Pros and trade-offs

### Rules

- Compare like with like.
- Use the same dimensions and level of detail.
- Align shared criteria.
- Normalize units and time periods.
- Explain the decision significance of the difference.
- Use neutral treatment for most content and limited emphasis for the deciding factor.

### Avoid

- Unequal visual scales
- Different criteria for each option
- Biased wording that replaces evidence
- Decorative cards without shared comparison axes
- Checkmark grids that ignore quality, degree, or trade-off

---

## Metric

### Purpose

A Metric component presents one quantitative value with enough context to interpret it correctly.

### Anatomy

- Value
- Unit
- Metric label
- Time period
- Baseline, target, or comparison
- Trend or variance, optional
- Source, when required

### Variants

- Focal metric
- Metric group
- Target progress
- Variance
- Trend summary

### Rules

- Make the unit inseparable from the value.
- State the time period.
- Provide a baseline or target when the number lacks standalone meaning.
- Use number formatting consistently.
- Use Accent for one focal metric, not every number.
- Use semantic status colors only when performance meaning is defined.
- Avoid false precision.

### Avoid

- Large numbers without context
- Mixing percentages and percentage-point change
- Using color to imply success without a defined target
- Showing more metrics than the audience can interpret
- Decorative gauge charts without analytical value

---

## Quote

### Purpose

A Quote component presents a verified human statement that provides evidence, perspective, or emotional context.

### Anatomy

- Quote text
- Speaker or source
- Role or relationship, when relevant
- Date or research context, when relevant

### Rules

- Preserve the speaker's meaning.
- Use only verified quotes.
- Keep the quote concise enough to understand quickly.
- Include sufficient attribution.
- Use quotation marks or a clear quote structure.
- Distinguish direct quotation from paraphrase.

### Avoid

- Invented customer quotes
- Anonymous quotes without necessary context
- Long transcripts
- Decorative quotation marks larger than the message
- Quotes used as evidence when the source is unrepresentative or unclear

---

## Image

### Purpose

An Image component provides evidence, context, explanation, atmosphere, or human relevance that text and diagrams cannot communicate as effectively.

### Anatomy

- Image
- Crop or focal area
- Caption, optional
- Source or credit, when required
- Annotation, optional
- Alt-text or descriptive equivalent, when required

### Image Roles

- Evidence
- Demonstration
- Context
- Human story
- Product or interface view
- Conceptual framing

### Rules

- Define the image role before selecting it.
- Use authentic, specific imagery when evidence matters.
- Crop around the intended subject.
- Maintain sufficient resolution.
- Preserve legal usage rights and attribution requirements.
- Use text overlays only with verified contrast.
- Annotate screenshots or evidence images when the audience needs guidance.
- Use one dominant image rather than several weak images when the message requires focus.

### Avoid

- Generic stock photography used only to fill space
- AI imagery presented as factual evidence
- Unclear crops
- Distorted aspect ratios
- Text placed over complex details
- Decorative image mosaics without narrative purpose

---

## Icon

### Purpose

An Icon supports rapid recognition, navigation, category distinction, or a familiar action.

Icons are supporting signals. They are not substitutes for clear language when the meaning is unfamiliar.

### Anatomy

- Icon glyph
- Optional text label
- Optional semantic background or status

### Rules

- Use one icon family within a presentation.
- Use consistent size, stroke weight, optical size, and alignment.
- Pair unfamiliar icons with text.
- Use icons only when they improve scanning or recognition.
- Align icons optically with text and containers.
- Use semantic color only when meaning requires it.

### Avoid

- Mixing filled, outlined, hand-drawn, and multicolor icon styles
- Using icons as bullets for every list
- Using several icons with overlapping meanings
- Enlarging an icon to fill empty space
- Using an icon without an understandable relationship to the content

---

## Material Symbols Outlined

### Default Family

The default presentation icon family is:

```text
Material Symbols Outlined
```

This is the applied Presentation System rule until the canonical Iconography System is defined in `../06_Iconography.md`.

When the Iconography System becomes active, it takes precedence.

### Usage Rules

- Use the Outlined style consistently.
- Keep `fill` disabled unless a future semantic rule explicitly defines a filled state.
- Use a consistent weight within one composition or deck.
- Use a consistent optical size appropriate to the rendered size.
- Use rounded or sharp variants only if approved by the future Iconography System.
- Prefer universally recognized symbols.
- Pair specialist or ambiguous symbols with labels.
- Use icons as semantic support, not visual decoration.

### Recommended Behavior

| Context | Rule |
|---|---|
| Small label icon | Use simple glyphs with strong recognition |
| Process step | Use only when each icon adds distinct meaning |
| Status | Combine icon, label, and semantic color |
| Navigation | Maintain the same icon for the same destination |
| Focal illustration | Do not enlarge a UI icon into decorative artwork |

### Avoid

- Mixing Material Symbols Outlined with unrelated icon libraries
- Using emoji as brand icons
- Applying gradients, shadows, or 3D effects
- Using icons as the only carrier of critical meaning
- Selecting symbols because they look attractive rather than communicate accurately

---

## Component Composition

### Primary and Supporting Components

A slide should normally contain:

```text
One primary component
+ supporting components only as needed
```

Examples:

- Chart + Callout
- Comparison + Recommendation Callout
- Process + Metric
- Image + Insight
- Table + Focal Highlight

Do not assemble several primary components into one slide unless the slide's purpose is explicitly to show their relationship.

### Shared Anatomy

Repeated components should align:

- Titles
- Labels
- Values
- Baselines
- Internal padding
- Source placement
- Icon position

Visual consistency should reflect semantic consistency.

### Variant Governance

Create a new variant only when:

- The information role changes
- The interaction or state changes
- The layout behavior changes materially
- Accessibility requires a distinct implementation
- A recurring use case cannot be handled clearly by an existing variant

Do not create variants only for:

- Different corner radius
- Small spacing changes
- Arbitrary color changes
- One-off decoration
- A single slide exception

---

## Accessibility

Every component must:

- Preserve a clear reading order
- Meet applicable contrast requirements
- Keep essential text at approved typography sizes
- Avoid color-only meaning
- Use direct labels where practical
- Remain understandable in grayscale when possible
- Provide source and unit information when interpretation depends on them
- Preserve editability for future correction
- Avoid motion or animation as the only communication method

---

## AI Component Selection

AI should select components from the information relationship.

```text
Single conclusion → Title, Callout, or Metric
Precise lookup → Table
Quantitative pattern → Chart
Chronology → Timeline
Planned progression → Roadmap
Movement through a system → Flow
Ordered actions → Process
Difference or choice → Comparison
Human evidence → Quote
Visual evidence or context → Image
Recognition support → Icon
```

AI must not choose components based on template availability or visual novelty.

---

## Final Principle

```text
A component is successful when its meaning
is more reusable than its appearance.
```
