# Presentation Layout

> Version: 1.0.0  
> Status: Active  
> Owner: LINKGENT Brand OS  
> Last Updated: 2026-07-24

---

## Purpose

The LINKGENT Presentation Layout System defines how information architecture becomes visible space.

Layout is not the arrangement of decorative objects.

It is the spatial expression of:

- Meaning
- Priority
- Grouping
- Sequence
- Comparison
- Relationship
- Reading order
- Focus

This system applies across PowerPoint, Google Slides, Keynote, Canva, Figma Slides, Gamma, AI presentation tools, and future presentation environments.

Exact measurements may vary by platform. Spatial relationships and quality standards must remain consistent.

---

## Inheritance

This file applies:

- Structure First and UX Before UI from [`../01_Brand_Core.md`](../01_Brand_Core.md)
- Semantic color roles from [`../03_Color_System.md`](../03_Color_System.md)
- Typography hierarchy and vertical rhythm from [`../04_Typography.md`](../04_Typography.md)
- Presentation reasoning from [`Thinking.md`](./Thinking.md)

Shared spacing tokens should be inherited from `../05_Design_Tokens.md` when defined.

Until those global tokens are available, this file uses normalized presentation-relative ratios. These ratios are Applied System defaults, not Brand OS-wide spacing primitives.

---

## Layout Principles

### 1. Structure Before Composition

Determine the information relationship before selecting a layout.

```text
Meaning
  ↓
Relationship
  ↓
Reading Order
  ↓
Spatial Structure
  ↓
Visual Refinement
```

Do not start by selecting a visually attractive slide pattern.

### 2. Alignment Creates Trust

Consistent alignment makes the system feel reliable and intentional.

Every visible element should align to:

- The safe area
- A grid line
- A shared text anchor
- A component boundary
- A meaningful visual axis

Avoid accidental near-alignment.

### 3. Whitespace Communicates Relationship

Whitespace is active information.

It indicates:

- Separation
- Grouping
- Hierarchy
- Pause
- Focus
- Transition

Do not fill space simply because it is available.

### 4. One Dominant Composition

A slide should normally have one dominant spatial idea.

Examples:

- One message with supporting evidence
- One comparison
- One process
- One chart
- One system diagram
- One image with one interpretation

Multiple components may appear, but they should participate in one coherent composition.

### 5. Consistency Without Uniformity

Slides should share alignment, spacing, typography, and component logic.

They do not need to use the same layout repeatedly.

Variation is appropriate when the information relationship changes. Variation is not appropriate merely to make each slide look different.

---

## Canvas Model

### Platform-Neutral Coordinate System

For design reasoning, treat the canvas as a normalized coordinate space.

For a 16:9 landscape canvas:

```text
Width  = 100 units
Height = 56.25 units
```

This allows ratios to be transferred across tools without depending on points, pixels, centimeters, or application-specific rulers.

For other aspect ratios, apply the same rules proportionally.

### Default Aspect Ratio

The default presentation canvas is:

```text
16:9 landscape
```

Use another ratio when required by:

- Venue or display hardware
- Print or document use
- Vertical social presentation
- Kiosk or installation
- Existing organizational standards
- Accessibility or viewing constraints

The aspect ratio is an implementation decision. It must not change the message hierarchy.

### Reflow, Do Not Merely Scale

When adapting between aspect ratios:

- Preserve semantic groups
- Preserve reading order
- Preserve minimum type roles
- Preserve safe areas
- Reconfigure columns
- Reposition or crop imagery intentionally
- Simplify where the available space is reduced

Do not uniformly shrink the entire composition until it fits.

---

## Safe Area

### Purpose

The safe area protects content from:

- Projection cropping
- Screen overscan
- Export variation
- Tool chrome during live presentation
- Print trimming
- Edge crowding
- Reduced readability at distance

### Default Safe Area

For a standard 16:9 canvas, use the following presentation-relative defaults:

| Edge | Default Inset |
|---|---:|
| Left | `5%` of canvas width |
| Right | `5%` of canvas width |
| Top | `6%` of canvas height |
| Bottom | `6%` of canvas height |

This creates a primary content region of approximately:

```text
90% width × 88% height
```

The safe area is a minimum boundary, not a target to fill.

### Extended Safe Area

Increase the inset when:

- The slide will be projected in a large room
- The audience is far from the screen
- The canvas contains a single statement
- The content needs a calm or premium expression
- The screen or export behavior is uncertain
- Captions or sources require stable separation

### Edge Exceptions

Full-bleed imagery, color fields, or structural rules may extend to the canvas edge.

Essential content must remain within the safe area unless a deliberate, tested exception is required.

Do not place:

- Body text
- Key metrics
- Essential labels
- Sources
- Decision prompts

against the canvas edge.

---

## Grid

### Grid Purpose

The grid provides a shared spatial grammar.

It supports:

- Alignment
- Reuse
- Responsive adaptation
- Component consistency
- Human and AI generation
- Cross-tool transfer

The grid must support information. It must not force every slide into equal boxes.

### Default Grid

Use a 12-column grid inside the safe area.

```text
Safe Area
└── 12 equal columns
    └── consistent gutters
```

The 12-column structure supports common spans:

- `12` columns: full-width statement, table, chart, or image
- `8 + 4`: primary evidence with supporting interpretation
- `7 + 5`: dominant content with substantial support
- `6 + 6`: direct comparison
- `4 + 4 + 4`: three-part structure
- `3 + 3 + 3 + 3`: four-item structure
- `3 + 9`: label or navigation with primary content

### Gutter

Use a consistent gutter of approximately:

```text
1.5%–2% of canvas width
```

Increase the gutter when:

- Components contain dense text
- The audience requires stronger separation
- Cards or comparison items have similar visual weight

Reduce the gutter only when the relationship requires visual continuity and readability is preserved.

### Grid Flexibility

The grid may be subdivided or combined, but all major objects should retain clear shared anchors.

Do not create a new alignment system for each slide.

### Nested Grid

Components may use an internal grid when needed.

Examples:

- A table uses aligned columns within a full-width region.
- A card group uses consistent internal padding and title alignment.
- A process uses equal step widths within an 8-column span.

Nested grids must align with the parent composition where practical.

---

## Layout Zones

A standard slide may contain the following semantic zones:

```text
Canvas
├── Header Zone
│   ├── Eyebrow or chapter label, optional
│   └── Message title
├── Content Zone
│   ├── Primary visual or evidence
│   └── Supporting interpretation
└── Footer Zone
    ├── Source or metadata
    └── Page or navigation marker, optional
```

These are semantic roles, not fixed boxes.

### Header Zone

The header should establish the slide message and reading entry point.

Rules:

- Use a stable left or intentional center anchor.
- Keep the title visually connected to the content it governs.
- Do not create excessive empty distance between title and evidence.
- Do not repeat decorative chapter labels when they do not improve orientation.

### Content Zone

The content zone carries the primary communication object.

Rules:

- Reserve the strongest spatial emphasis for the main message or evidence.
- Avoid multiple unrelated focal areas.
- Align supporting text to the object it interprets.
- Use whitespace to separate semantic groups.

### Footer Zone

The footer is for genuinely supporting information.

Rules:

- Sources must remain readable.
- Do not use the footer as overflow storage.
- Keep repeated navigation quiet and consistent.
- Avoid placing essential conclusions in the footer.

---

## Whitespace

### Principle

Whitespace reduces cognitive burden by making relationships visible.

Use whitespace to show:

- Items that belong together
- Items that belong to different groups
- A transition between message levels
- The dominant visual object
- A pause before a conclusion

### Proximity Rule

Related elements should be closer to each other than to unrelated elements.

```text
Internal spacing < Group spacing < Section spacing
```

The exact ratio may vary, but the relationship must remain visible.

### Whitespace Hierarchy

Use at least three spatial levels when the slide requires them:

| Level | Meaning |
|---|---|
| Tight | Elements within one semantic unit |
| Standard | Related units within one group |
| Open | Separate sections, ideas, or narrative moments |

Do not use equal spacing between everything. Equal spacing removes semantic cues.

### Empty Space

Empty space is valid when it creates:

- Focus
- Calm
- Premium restraint
- Separation
- Anticipation
- Stronger reading order

Empty space is not valid when it results from missing structure or an unresolved message.

---

## Alignment

### Primary Alignment

Prefer left alignment for:

- Message titles
- Paragraphs
- Lists
- Tables
- Charts with textual interpretation
- Process labels
- Analytical slides

Left alignment creates a stable reading anchor and supports scanning.

### Center Alignment

Center alignment may be used for:

- Cover slides
- Chapter transitions
- Short statements
- Single metrics
- Quotes
- Deliberate pause moments

Avoid long centered paragraphs or multi-column centered text.

### Optical Alignment

Geometric alignment may require optical adjustment for:

- Icons
- Circular shapes
- Large numerals
- Punctuation
- Image subjects
- Irregular logos

Optical correction must improve perceived alignment without breaking the grid system.

### Baseline Alignment

Where the tool supports it, align:

- Text across columns by baseline
- Metrics and units consistently
- Table values by numerical logic
- Repeated labels at the same vertical position

Do not vertically center unrelated text blocks solely because they share a container.

---

## Column System

### One Column

Use for:

- Statements
- Narrative text with one visual
- Full-width charts
- Tables
- Timelines
- System diagrams

One column creates a strong, direct reading path.

### Two Columns

Use for:

- Comparison
- Problem and implication
- Visual and explanation
- Current and future state
- Recommendation and evidence

Two columns must have an explicit relationship.

Do not use two columns merely to fill width.

### Three Columns

Use for:

- Three alternatives
- Three stages
- Three principles
- Three equivalent categories

All three columns should use comparable semantic structures.

### Four or More Columns

Use cautiously for:

- Compact roadmaps
- Small metric groups
- High-level portfolio views
- Repeated reference items

When columns become too narrow for approved typography, reduce the number of columns or change the representation.

---

## Vertical Rhythm

### Principle

Vertical rhythm makes the reading sequence predictable.

Typography and spacing must work as one system.

### Rhythm Order

A standard slide should use a repeatable relationship among:

```text
Chapter label
  ↓ small separation
Message title
  ↓ medium separation
Primary content
  ↓ medium or large separation
Supporting annotation
  ↓ small separation
Source or metadata
```

### Semantic Spacing

- A title should remain visually attached to the content it governs.
- A caption should remain attached to its image, chart, or table.
- A new section should have clearly greater separation than a new paragraph.
- Repeated cards should use consistent internal padding.
- Supporting notes should not interrupt the primary reading path.

### Text Block Rhythm

Follow the line-height and hierarchy rules in [`../04_Typography.md`](../04_Typography.md).

Do not compensate for weak layout by reducing line height or forcing manual line breaks.

---

## Information Density Layouts

Layout must respond to the density mode defined in [`Thinking.md`](./Thinking.md).

### Statement Layout

Use for a single conclusion, transition, or framing message.

Characteristics:

- One primary text block or metric
- Large safe area
- Minimal supporting detail
- One deliberate anchor
- No decorative filler

### Standard Layout

Use for most live presentation slides.

Characteristics:

- One message title
- One primary visual or structured group
- Two to four supporting units
- Clear reading order
- Sufficient whitespace between groups

### Analytical Layout

Use for data, comparison, process, or evidence.

Characteristics:

- One dominant analytical object
- Direct annotation
- Clear scale, unit, source, and baseline
- Limited supporting prose
- Controlled color emphasis

### Reference Layout

Use for read-ahead or appendix content.

Characteristics:

- Higher density
- Explicit labels and grouping
- Strong alignment
- Complete sources and qualifiers
- Approved typography minimums
- No dependence on spoken explanation

Reference density must not be imported into the live story without a reason.

---

## Visual Balance

### Visual Weight

Visual weight increases with:

- Size
- Darkness
- Saturation
- Contrast
- Density
- Detail
- Isolation
- Irregularity
- Proximity to the center or edge, depending on composition

Use visual weight to support the intended message hierarchy.

### Asymmetrical Balance

Symmetry is not required.

An asymmetrical layout may be balanced when:

- One large object is balanced by several smaller related objects
- A dark structural region is balanced by open neutral space
- An image is balanced by a concise, high-value message

### Tension

Controlled tension may create focus or movement.

It must not create:

- Unstable reading order
- Accidental crowding
- Misaligned components
- Edge anxiety
- Competition between focal points

### Balance Test

Blur or reduce the slide to a thumbnail.

The dominant message and primary grouping should remain visible.

If every area appears equally strong, hierarchy is insufficient.

---

## Color in Layout

Apply the Color System, not arbitrary styling.

### Default Area Distribution

- Neutral backgrounds should dominate.
- Primary may define structural anchors and section framing.
- Accent should identify one focal point, selected item, or key data series.
- Semantic colors should appear only when their meaning is present.

The Color System recommends Accent generally remain below approximately `10%` of the visible slide area. Meaning takes precedence over mechanical measurement.

### Surface Use

Use tinted or colored surfaces to clarify:

- Grouping
- Selection
- Structural level
- Status
- Focus

Do not use alternating fills to create artificial rhythm.

---

## Imagery and Full-Bleed Layouts

Full-bleed imagery may be used when the image is essential to the message.

Requirements:

- The subject and crop must support the intended interpretation.
- Essential text must remain readable in the actual composition.
- Use a controlled solid area or verified overlay when text appears on imagery.
- Do not rely on a complex image as a background for detailed content.
- Preserve the safe area for essential text.
- Avoid imagery used only to make a slide feel less empty.

---

## Projection and Viewing Conditions

Design for the real environment.

Review at:

- Presentation distance
- Laptop size
- Exported PDF size
- Bright-room projection conditions
- Grayscale, when printing is possible
- Uncalibrated display conditions

A slide that works only at 100% zoom on the designer's screen is not complete.

### Room Condition Rule

When projection quality is uncertain:

- Increase whitespace
- Increase contrast
- Reduce supporting detail
- Simplify charts
- Avoid pale borders and fills
- Avoid text over imagery
- Use direct labels

---

## Cross-Platform Implementation

### PowerPoint and Keynote

- Use masters, guides, and reusable layouts.
- Avoid local coordinate drift.
- Preserve editable text and shapes.

### Google Slides

- Use theme layouts and consistent guides.
- Check font substitution and line wrapping.
- Avoid fragile compositions that depend on precise effects.

### Canva

- Use brand styles and locked structural guides where appropriate.
- Preserve consistent spacing when templates are duplicated.
- Check exports for font and alignment shifts.

### Figma Slides

- Use shared styles, components, auto layout, and constraints where appropriate.
- Avoid creating visual variants without semantic reason.

### Gamma and AI Presentation Tools

- Define the layout semantically before generation.
- Review automated reflow, density, reading order, and component consistency.
- Replace decorative auto-layout decisions that do not express the information structure.

---

## Do

- Start from the information relationship
- Use a consistent safe area
- Use shared grid anchors
- Make one composition dominant
- Use proximity to show grouping
- Preserve approved typography minimums
- Use whitespace intentionally
- Reflow across aspect ratios
- Test at actual viewing distance
- Keep sources readable
- Use color to support structure and focus
- Preserve editability

---

## Don't

- Start from a decorative template
- Fill every area of the canvas
- Use equal spacing for unrelated and related items
- Center long text blocks
- Create a new grid for every slide
- Use cards for all information
- Use colored backgrounds to create artificial variety
- Reduce typography to fit excess content
- Place essential information outside the safe area
- Depend on subtle borders under projection
- Scale a composition mechanically across aspect ratios
- Use alignment that is almost, but not actually, consistent

---

## Final Principle

```text
Layout is successful when the audience
can see the structure before reading the detail.
```
