# Presentation Layout

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

Presentation Layout defines cross-platform spatial rules for making Slide Architecture visible.

It applies to PowerPoint, Google Slides, Keynote, Canva, Figma Slides, Gamma, AI presentation systems, PDF exports, and future presentation tools.

Layout is not decoration. It communicates:

- Reading order
- Grouping
- Hierarchy
- Relationship
- Sequence
- Focus
- Density
- Stability
- Change

Layout begins after the semantic decisions in `PRES-PROCESS-001`.

---

## Inheritance

Layout applies:

- [`Thinking.md`](./Thinking.md) for Slide Architecture and density
- [`Content.md`](./Content.md) for title, label, source, and notes behavior
- [`../04_Typography.md`](../04_Typography.md) for typography hierarchy and minimums
- [`../03_Color_System.md`](../03_Color_System.md) for color roles and contrast
- `../05_Design_Tokens.md` when active
- `../09_Layout_System.md` when active
- [`Accessibility.md`](./Accessibility.md) for reading order and accessible composition

This file does not own font sizes, color values, or contrast thresholds.

---

## Layout Decision Sequence

```text
Slide Architecture
  ↓
Reading Order
  ↓
Information Relationship
  ↓
Density
  ↓
Safe Area
  ↓
Grid and Columns
  ↓
Grouping and Whitespace
  ↓
Alignment and Rhythm
  ↓
Visual Balance
  ↓
Platform Adaptation
```

Do not choose a composition before reading order and information relationship are defined.

---

## Safe Area

Every slide must preserve a safe area around essential content.

The safe area protects against:

- Projection cropping
- Display overscan
- Tool conversion
- Export differences
- Audience distance
- Visual crowding
- Presenter interface overlays
- Print and PDF trimming

Rules:

- Essential titles, labels, values, sources, and controls remain within the safe area.
- Decorative elements may extend beyond it only when meaning is unaffected.
- The safe area should be defined as a proportional region, not a platform-specific absolute measurement.
- Platform templates may map that proportion to tool-specific guides.
- Edge proximity must not be used as a substitute for emphasis.

When unsure, increase the safe area rather than reduce text.

---

## Grid

Use a repeatable grid to create alignment and predictable relationships.

A grid should define:

- Outer safe area
- Columns
- Gutters
- Baseline or vertical rhythm
- Anchor lines
- Standard content zones

The grid is a decision aid, not a visual prison.

Break the grid only when:

- The break communicates a deliberate hierarchy or relationship.
- Reading order remains clear.
- The exception is reproducible.
- The exception does not reduce accessibility.

Do not break the grid merely to create novelty.

---

## Columns

Column choice follows information structure.

### Single Column

Use for:

- Statements
- Sequential explanation
- Strong narrative focus
- Large visual evidence
- Simple process or timeline

### Two Columns

Use for:

- Comparison
- Cause and effect
- Problem and response
- Evidence and implication
- Text and image
- Current and future state

Two columns require a meaningful relationship. They are not a default way to fill width.

### Three or More Columns

Use for:

- Parallel categories
- Short comparable options
- Repeated metrics
- Compact stages

Requirements:

- Shared semantic level
- Comparable content
- Consistent anatomy
- Adequate width
- Clear reading order

Avoid many narrow columns containing paragraph text.

---

## Whitespace

Whitespace communicates separation, grouping, priority, and calm.

Use less space within a semantic group and more space between groups.

Whitespace should:

- Make hierarchy visible
- Reduce cognitive burden
- Protect the focal point
- Attach captions and sources to their objects
- Separate unrelated content
- Preserve readable line length

Whitespace must not:

- Hide missing content
- Create false luxury
- Force essential detail into unreadable type
- Separate labels from the objects they describe

Empty space is not wasted when it improves understanding.

---

## Alignment

Prefer shared alignment anchors.

Use:

- Left alignment for paragraphs, lists, tables, labels, and analytical content
- Center alignment for brief cover, chapter, or statement moments
- Numeric alignment appropriate to the comparison
- Direct alignment between labels and data
- Consistent chart plot and annotation anchors

Avoid:

- Long centered paragraphs
- Near-alignment
- Independent card positions without shared anchors
- Arbitrary optical nudges that destroy repeatability

Optical correction is allowed after structural alignment is established.

---

## Vertical Rhythm

Vertical rhythm governs the relationship between:

- Title and content
- Heading and explanation
- Label and value
- Visual and caption
- Chart and source
- Section and subsection
- Slide body and footer

Spacing should reflect semantic distance.

Do not use one uniform gap between every element.

Apply canonical typography line-height and hierarchy rules rather than creating local text spacing systems.

---

## Reading Order

Reading order must be understandable visually and, when the platform supports it, technically.

A default reading sequence is:

```text
Context or label
  ↓
Primary message
  ↓
Primary evidence or explanation
  ↓
Implication or action
  ↓
Source or note
```

This sequence may change when the communication purpose requires it, but the chosen order must be explicit.

Reading order must survive:

- Grayscale
- Export to PDF
- Platform conversion
- Removal of animation
- Assistive technology traversal where supported

---

## Visual Hierarchy

Create hierarchy through:

1. Position
2. Grouping
3. Whitespace
4. Scale
5. Weight
6. Contrast
7. Color
8. Decoration

Use a limited number of visible hierarchy levels.

Typography hierarchy is governed by `TYPE-PRESENTATION-HIERARCHY`.

Do not create local hierarchy by inventing sizes, colors, or effects.

---

## Information Density

Use the density definitions from [`Thinking.md`](./Thinking.md):

- Statement
- Standard
- Analytical
- Reference

### Statement

- One dominant message
- Minimal support
- Strong whitespace
- Immediate comprehension

### Standard

- One message
- Essential explanation or evidence
- Clear primary and secondary zones

### Analytical

- One message
- Structured evidence
- Direct labels
- Visible implication
- Controlled annotation

### Reference

- Lookup-oriented
- Explicit labels
- Complete source information
- Strong grouping and navigation
- May be appendix-led

Do not reduce type below canonical requirements to preserve a chosen density. Change the architecture instead.

---

## Visual Balance

Balance considers:

- Text mass
- Data mass
- Image weight
- Color weight
- Empty space
- Direction
- Contrast
- Focal point
- Stability
- Intentional tension

Balance does not require symmetry.

A comparison may require symmetry. A recommendation may require asymmetry to create focus.

One slide should normally have one dominant composition.

---

## Cards

Cards may group independent but related units.

Use cards when:

- Each unit has a shared anatomy.
- Units need separate scanning.
- Boundaries improve understanding.
- Comparison remains possible.

Do not use cards when:

- Content is one continuous argument.
- Boxes exist only to fill the canvas.
- Every paragraph becomes a card.
- Colored fills replace hierarchy.
- Card count makes scanning harder.

Cards are components, not the layout system.

---

## Tables and Charts

Tables and charts must receive enough space for their actual reading task.

Do not:

- Place a dense table in a narrow column.
- Shrink labels to preserve an ornamental layout.
- Crop axes, legends, sources, or notes.
- Separate a chart from its conclusion.
- Use surrounding cards that reduce usable plot area without adding meaning.

Direct labels are preferred where they improve reading.

---

## Images

Image placement must preserve:

- Subject integrity
- Evidence credibility
- Text contrast
- Alt-text meaning
- Cropping safety
- Source attribution
- Negative space required for overlaid content

Avoid essential text over complex imagery.

Do not crop documentary evidence in a way that changes meaning.

---

## Footer and Source Zone

A footer may contain:

- Source
- Confidentiality
- Version
- Page number
- Owner
- Date

The footer must remain subordinate but readable.

Apply `TYPE-PRESENTATION-MIN-CAPTION`.

Do not place essential reasoning only in the footer.

---

## Aspect Ratio and Adaptation

Do not mechanically stretch a layout between aspect ratios.

Adaptation sequence:

1. Preserve message.
2. Preserve reading order.
3. Preserve information relationships.
4. Preserve essential content.
5. Recompose columns and zones.
6. Re-evaluate density.
7. Validate typography and sources.
8. Validate accessibility.

Scaling every object uniformly is not adaptation.

---

## Cross-platform Rules

### PowerPoint

Use master layouts, guides, semantic placeholders, and editable objects where practical.

### Google Slides

Account for font substitution, theme limitations, grouping behavior, and browser rendering.

### Keynote

Validate master behavior, type metrics, PDF export, and animation removal.

### Canva

Use brand styles and reusable layouts while avoiding flattened critical content.

### Figma Slides

Use shared styles, components, constraints, and semantic naming.

### Gamma and AI Tools

Treat generated layout as provisional. Validate reading order, editability, source integrity, and compliance with all canonical references.

---

## Layout Exceptions

An exception must record:

```yaml
rule:
reason:
scope:
platform:
risk:
mitigation:
approved_by:
review_date:
```

An exception for one artifact does not redefine the system.

---

## Prohibited Practices

Do not:

- Start from a visual template before Slide Architecture
- Fill empty space with larger text without semantic reason
- Use equal boxes for unequal information
- Use arbitrary alignment
- Depend on animation for essential meaning
- Create dense layouts by reducing typography
- Use whitespace as a reason to remove necessary context
- Stretch layouts across aspect ratios
- Place sources where they become unreadable
- Treat platform conversion as a final administrative step

---

## Validation

Layout passes when:

- Reading order is immediate
- Grouping reflects meaning
- Alignment is systematic
- Density matches use
- Sources remain attached
- Typography meets canonical rules
- Color meets canonical rules
- Export and conversion preserve meaning
- Accessibility review passes
- The layout can be explained from Slide Architecture
