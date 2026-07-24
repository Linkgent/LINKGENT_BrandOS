# AI Presentation Generation

> Version: 1.0.0  
> Status: Active  
> Owner: LINKGENT Brand OS  
> Last Updated: 2026-07-24

---

## Purpose

AI Presentation Generation defines how AI should reason, structure, generate, adapt, and review LINKGENT presentations.

AI may accelerate presentation work, but it must follow the same quality hierarchy as a human designer.

AI must not treat presentation generation as automatic layout production.

```text
AI Presentation Generation
≠ text placed into slide templates
```

It is the controlled transformation of audience needs and evidence into a structured communication system.

---

## Inheritance

AI must read and apply the following sources before generating a presentation:

1. [`../../CONSTITUTION.md`](../../CONSTITUTION.md)
2. [`../01_Brand_Core.md`](../01_Brand_Core.md)
3. [`../03_Color_System.md`](../03_Color_System.md)
4. [`../04_Typography.md`](../04_Typography.md)
5. `../05_Design_Tokens.md` when defined
6. `../06_Iconography.md` when defined
7. [`README.md`](./README.md)
8. [`Thinking.md`](./Thinking.md)
9. [`Layout.md`](./Layout.md)
10. [`Components.md`](./Components.md)
11. [`Templates.md`](./Templates.md)
12. [`Checklist.md`](./Checklist.md)
13. `../13_AI_Generation_Rules.md` when defined

AI must not create independent brand rules when a canonical source exists.

When a referenced canonical file is not yet defined, AI must:

- Use the closest approved semantic rule from an existing source
- Avoid inventing a new Brand OS-wide standard
- Mark unresolved implementation decisions clearly
- Preserve semantic naming so future tokens can replace provisional values

---

## AI Role

AI is a production and reasoning partner.

AI may:

- Analyze audience and purpose
- Inventory and classify content
- Identify information relationships
- Propose a deck thesis
- Build story alternatives
- Draft slide messages
- Recommend representations
- Select layouts and components
- Apply typography and color roles
- Generate editable presentation structures
- Adapt content across tools and aspect ratios
- Review logic, density, consistency, and accessibility

AI may not replace human responsibility for:

- Final purpose
- Strategic judgment
- Ethical judgment
- Evidence validity
- Confidentiality
- Legal claims
- Decision ownership
- Brand approval
- Final publication

---

## Required Thinking Order

AI must use the following sequence:

```text
Audience
  ↓
Purpose
  ↓
Key Message
  ↓
Story
  ↓
Information Architecture
  ↓
Information Density
  ↓
Layout
  ↓
Components
  ↓
Typography
  ↓
Color
  ↓
Visual Design
  ↓
Review
```

AI must not begin with layout, template selection, color, imagery, or decoration.

If a higher layer is unresolved, AI should resolve it, state an assumption, or mark it as unknown before continuing.

---

## Knowledge States

AI must distinguish the status of information.

| State | Meaning | AI Behavior |
|---|---|---|
| Defined | Explicitly approved in a canonical source or provided as verified input | Use directly and preserve meaning |
| Derived | Logically inferred from defined information | State or record the reasoning |
| Proposed | A new recommendation or draft decision | Label as proposed; do not present as approved |
| Unknown | Missing, contradictory, or unverifiable | Do not invent; mark for resolution |

AI must not convert proposed or unknown information into apparent fact through confident language or polished visual treatment.

---

## Input Contract

Before generation, AI should establish a Presentation Brief.

### Required Inputs

- Primary audience
- Presentation purpose
- Intended decision or action
- Presentation mode: live, read-ahead, decision, workshop, or reference
- Available time or expected reading depth
- Source content
- Known constraints
- Required output tool or format
- Language

### Strongly Recommended Inputs

- Audience knowledge level
- Stakeholder concerns
- Evidence and source quality
- Required sections
- Confidentiality level
- Aspect ratio
- Delivery environment
- Deadline or version state
- Existing template or master
- Required editability

### Missing Inputs

When essential information is missing, AI should use one of three actions:

1. Infer a low-risk operational detail and record the assumption.
2. Mark the missing field and continue with a clearly provisional structure.
3. Stop the affected claim or slide from being generated when accuracy would be compromised.

AI must not invent:

- Data
- Sources
- Quotes
- Customer statements
- Research findings
- Financial values
- Dates
- Legal or regulatory claims
- Approved decisions
- Performance outcomes

---

## Generation Process

## Stage 1: Audience

AI must define:

- Primary audience
- Decision owner
- Secondary stakeholders
- Existing knowledge
- Expected objections
- Relevant vocabulary
- Viewing context
- Accessibility needs

Output:

```text
Audience Profile
```

AI must adapt detail, pacing, terminology, and evidence to the audience without changing factual meaning.

---

## Stage 2: Purpose

AI must write one primary purpose statement as an audience outcome.

Required structure:

```text
Enable [audience]
to [understand / decide / align / act]
about [subject]
within [relevant context].
```

Output:

```text
Presentation Purpose
Decision or Action Required
Success Condition
```

AI must not define success as “a professional-looking deck.”

---

## Stage 3: Key Message

AI must define:

- Deck thesis
- Supporting chapter messages
- Evidence required
- Main implication
- Intended action

Output:

```text
Deck Thesis
Chapter Message Map
Claim–Evidence–Implication–Action Map
```

The deck thesis must be more specific than the presentation topic.

---

## Stage 4: Story

AI must create a reasoning sequence before creating slides.

The story should define:

- Entry point
- Context
- Tension, question, or opportunity
- Insight
- Response
- Evidence and feasibility
- Decision
- Action

Output:

```text
Story Spine
Chapter Order
Transition Logic
```

Every transition should be explainable through a logical relationship such as:

- Therefore
- However
- Because
- Compared with
- For example
- As a result
- To decide this
- Next

AI should produce alternative story structures only when they represent meaningfully different communication strategies.

---

## Stage 5: Information Architecture

AI must:

- Inventory source information
- Remove duplication
- Normalize terminology
- Reconcile units and time periods
- Separate fact, interpretation, assumption, proposal, and unknown
- Classify content as essential, supporting, reference, or remove
- Group information by meaning
- Map relationships

Output:

```text
Content Inventory
Information Role Map
Main Story Content
Appendix Content
Removed or Deferred Content
Evidence Gaps
```

AI must not copy the source document structure automatically.

A report heading structure may not be the correct presentation story.

---

## Stage 6: Information Density

AI must assign a density mode to each slide:

- Statement
- Standard
- Analytical
- Reference

AI should balance density across the deck.

Rules:

- Live decks should favor Statement, Standard, and focused Analytical slides.
- Read-ahead decks may use more Analytical and Reference slides.
- A complex visual requires simpler surrounding content.
- A dense table requires restrained annotation.
- Supporting detail should move to the appendix when it interrupts the main story.
- Text must not be reduced below approved typography minimums to fit content.

Output:

```text
Slide Density Map
```

---

## Stage 7: Slide Specification

AI must define each slide semantically before rendering it.

### Required Slide Specification

```yaml
slide_id: S01
story_role: Establish the decision context
purpose: Explain why the decision is required now
message: The current operating model cannot support the next growth phase
message_type: claim
evidence:
  - source_reference_01
implication: A structural change is required before expansion
information_relationship: cause-and-effect
density: analytical
preferred_template: Problem
primary_component: Flow
supporting_components:
  - Metric
  - Callout
reading_order:
  - message
  - evidence
  - implication
source_requirement: visible
status: proposed
```

The schema may be adapted to the system, but the semantic fields must remain available.

### Slide Title Rule

AI should use message-led titles for analytical, persuasive, and decision slides.

Topic labels are appropriate for:

- Cover
- Agenda
- Chapter
- Reference

### One Slide, One Message

AI must test whether every element supports one primary conclusion.

When several conclusions exist, AI should split the slide or define a higher-order message that genuinely unifies them.

---

## Stage 8: Representation and Layout

AI must select representation from the information relationship.

| Information Relationship | Preferred Representation |
|---|---|
| Single conclusion | Statement, Callout, or Metric |
| Precise lookup | Table |
| Quantitative pattern | Chart |
| Chronology | Timeline |
| Planned progression | Roadmap |
| Movement | Flow |
| Ordered action | Process |
| Difference or choice | Comparison |
| Hierarchy | Hierarchy diagram |
| Human evidence | Quote |
| Visual evidence or context | Image |

AI must then apply:

- Safe area
- Grid
- Alignment
- Whitespace
- Vertical rhythm
- One dominant composition
- Appropriate density mode

AI must not select a layout because it is visually varied or available in a template library.

---

## Stage 9: Component Selection

AI must use approved components from [`Components.md`](./Components.md).

Selection must be semantic.

Preferred:

```text
Presentation/Comparison/TwoColumn
```

Avoid:

```text
Two blue boxes with icons
```

AI should use:

```text
One primary component
+ supporting components only when necessary
```

New component variants must not be created for arbitrary color, radius, spacing, or decorative differences.

---

## Stage 10: Typography

AI must reference semantic typography roles before numeric values.

Required roles:

- `Typography/Display`
- `Typography/Heading/H1`
- `Typography/Heading/H2`
- `Typography/Body/Large`
- `Typography/Body/Default`
- `Typography/Caption`

Typography source:

- [`../04_Typography.md`](../04_Typography.md)

Rules:

- Preserve hierarchy by meaning.
- Use a maximum of three visible hierarchy levels per slide.
- Use BIZ UDPゴシック for Japanese when supported.
- Use Inter for Latin text and numbers when supported.
- Use approved fallbacks when required.
- Do not invent font sizes.
- Do not reduce Body below `16 pt` or Caption below `11 pt` in the current PowerPoint implementation baseline.
- For other tools, preserve equivalent perceived hierarchy and readability.
- Rewrite, restructure, or split content before reducing type.
- Avoid long centered paragraphs.

AI must not make text larger simply to fill space or attract attention without semantic reason.

---

## Stage 11: Color

AI must select semantic color roles before raw values.

Color source:

- [`../03_Color_System.md`](../03_Color_System.md)

Core behavior:

```text
Neutral  = content, surfaces, rhythm
Primary  = structure, hierarchy, trust
Accent   = focal attention, action, selected emphasis
Semantic = explicit state or meaning
```

Rules:

- Neutral backgrounds should dominate.
- Primary should define structural anchors and trusted hierarchy.
- Accent should identify one focal point, selected step, recommendation, or data series.
- Semantic colors must be used only for their defined meaning.
- Accent should generally remain below approximately `10%` of the visible slide area.
- Use `text.primary` for essential body content.
- Do not use white text on `accent.500`.
- Do not use color as the only carrier of meaning.
- Do not invent new hues or uncontrolled opacity variants.
- Avoid gradients by default.
- Do not increase saturation to make the presentation appear more futuristic.

Preferred AI instruction:

```text
Use background.canvas for the slide.
Use structure.primary for the section anchor.
Use emphasis.focal for the single key data series.
```

Avoid:

```text
Make it blue and modern.
```

---

## Stage 12: Iconography, Imagery, and Decoration

### Iconography

Until `../06_Iconography.md` is defined, use the applied rule in [`Components.md`](./Components.md):

```text
Material Symbols Outlined
```

Rules:

- Use one icon family.
- Use icons only when they improve recognition or scanning.
- Pair unfamiliar icons with labels.
- Do not use icons as decorative bullets.
- Do not use icons as the only carrier of critical meaning.

### Imagery

AI must classify generated or selected imagery as:

- Evidence
- Demonstration
- Context
- Human story
- Conceptual framing

AI-generated imagery must not be presented as factual evidence.

AI must avoid:

- Generic stock-style filler
- Unverifiable people or environments presented as real
- Decorative technology imagery
- Complex backgrounds behind essential text
- Uncontrolled stylistic variation across the deck

### Decoration

Decoration is the final layer.

AI must first verify that audience, purpose, message, structure, story, layout, typography, and color are resolved.

AI should normally avoid:

- Gradients
- Glow
- Neon effects
- Unnecessary shadows
- 3D effects
- Decorative lines
- Unrelated geometric motifs
- Excessive corner radius
- Motion without communication value

---

## Design Token Use

When `../05_Design_Tokens.md` is active, AI must use tokens as the implementation interface.

Required behavior:

```text
Semantic role
  ↓
Design token
  ↓
Platform mapping
  ↓
Rendered value
```

AI must not hardcode values when an approved semantic token exists.

Until the Design Token System is defined:

- Use semantic role names from the Color and Typography Systems.
- Use normalized layout ratios from [`Layout.md`](./Layout.md).
- Keep mappings visible and replaceable.
- Do not present provisional implementation values as global Brand OS tokens.

---

## Cross-Platform Generation

The AI-generated presentation must preserve meaning across tools.

### Universal Requirements

- Editable text
- Editable structured shapes where practical
- Consistent reading order
- Semantic component naming where supported
- Approved typography hierarchy
- Approved color meaning
- Source visibility
- Accessible contrast
- Stable export
- No dependence on unsupported effects

### PowerPoint

- Use theme fonts, theme colors, and masters when available.
- Use native tables and editable charts where reliable.
- Avoid local typography overrides.
- Preserve source and notes.

### Google Slides

- Use theme layouts and guides.
- Check font substitution and wrapping.
- Avoid fragile effects and unsupported formatting.
- Verify exported PDF rendering.

### Keynote

- Use master slides and shared styles.
- Verify PowerPoint and PDF export when interchange is required.
- Avoid effects that become rasterized or unstable.

### Canva

- Use Brand Kit styles and reusable page structures.
- Preserve hierarchy when duplicating templates.
- Check font availability and export shifts.
- Avoid unstructured placement that prevents consistent editing.

### Figma Slides

- Use shared styles, variables, components, and auto layout where appropriate.
- Preserve semantic names.
- Use constraints for aspect-ratio adaptation.

### Gamma and AI Presentation Tools

- Provide the semantic slide specification before visual generation.
- Review automated grouping, rewriting, imagery, and density.
- Replace decorative layouts that distort the story.
- Verify exports in the final delivery format.

---

## Output Package

A complete AI presentation workflow should produce:

1. Presentation Brief
2. Audience Profile
3. Deck Thesis
4. Story Spine
5. Information Architecture Map
6. Slide List with one message per slide
7. Slide Specifications
8. Generated editable presentation
9. Source and assumption record
10. Checklist review report

The rendered deck alone is not sufficient for traceable, maintainable AI generation.

---

## Review Process

AI must review at three levels.

### Slide Review

- One primary message
- Clear reading order
- Appropriate representation
- Controlled density
- Correct typography roles
- Correct color roles
- Readable sources
- No unsupported claim

### Story Review

- Each slide contributes to the deck thesis
- Transitions are logical
- Evidence appears before conclusions that depend on it
- Objections and risks are addressed proportionately
- The ending enables decision or action

### System Review

- Brand Core inheritance
- Color System compliance
- Typography System compliance
- Component consistency
- Template logic
- Accessibility
- Editability
- Cross-platform stability
- AI traceability

Use [`Checklist.md`](./Checklist.md) for the final review.

---

## AI Self-Correction Order

When a generated slide fails, AI should correct it in this order:

```text
1. Purpose
2. Message
3. Information architecture
4. Story position
5. Representation
6. Density
7. Layout
8. Typography
9. Color
10. Decoration
```

Do not begin by changing colors or moving objects when the failure is conceptual.

---

## Prohibited AI Behaviors

AI must not:

- Generate directly from raw notes without structuring them
- Begin with a template or layout gallery
- Invent evidence, quotes, data, or sources
- Present assumptions as facts
- Use a different visual language on every slide
- Use color to replace hierarchy
- Use icons as decorative bullets
- Fill empty space with shapes or imagery
- Shrink text below approved minimums
- Create rasterized slides that cannot be maintained when editability is required
- Hide source limitations
- Use visual polish as evidence of correctness
- Automatically apply dark mode
- Use unsupported futuristic effects
- Optimize for novelty over understanding

---

## Final Principle

```text
AI must not generate slides first.
AI must generate understanding first,
then express it as a presentation.
```
