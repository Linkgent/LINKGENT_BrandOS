# LINKGENT PowerPoint Presentation Visual Direction

> Version: 0.1.0  
> Status: In Review  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-25

---

## 1. Purpose

This document defines reproducible visual and implementation rules for generating editable LINKGENT PowerPoint presentations.

It is not a fixed decorative template. It is a PowerPoint-specific production contract that translates meaning into typography, whitespace, information grouping, tables, comparisons, processes, diagrams, contained modules, and native editable objects.

> **Structure creates understanding.**

The goal is not to perfect one deck. The goal is to make the same quality of judgment repeatable in a new chat, by another AI, or in another production environment.

## 2. Scope and ownership

This document applies to:

- Microsoft PowerPoint presentations
- AI-generated or AI-assisted PowerPoint files
- PowerPoint templates and slide masters
- Redesign of existing source decks
- Reconstruction from approved visual references
- Deck-wide visual QA

This document owns PowerPoint-specific application of:

- Visual direction
- Slide composition
- Pattern selection
- Information blocking
- Native-object implementation
- PowerPoint release checks

It does not redefine Brand Core, canonical color meaning, canonical typography, brand-wide tokens, or general AI behavior.

## 3. Inheritance

Apply the following sources in order:

1. [`../../CONSTITUTION.md`](../../CONSTITUTION.md)
2. [`../01_Brand_Core.md`](../01_Brand_Core.md)
3. [`../03_Color_System.md`](../03_Color_System.md)
4. [`../04_Typography.md`](../04_Typography.md)
5. [`../05_Design_Tokens.md`](../05_Design_Tokens.md)
6. This document
7. Presentation templates
8. Generated artifacts

Past decks, screenshots, generated images, and local PowerPoint files are reference implementations, not canonical rules.

## 4. Core visual direction

LINKGENT presentations should feel:

- Structured
- Intelligent
- Reliable
- Minimal
- Sophisticated
- Calm
- Future-ready

Use:

- Typography-first hierarchy
- Strong whitespace
- Thin structural lines
- Precise alignment
- Meaningful asymmetry
- Restrained color
- Structural diagrams instead of decorative imagery
- One dominant composition per slide

A slide should look designed because its relationships are clear, not because whitespace has been filled.

## 5. Hard prohibitions

Do not use:

- Meaningless rounded cards
- Excessive corner radius
- Multiple identical boxes used only to fill space
- Drop shadows
- Gradients
- Glow or neon
- 3D effects
- Decorative icons
- Generic AI or technology imagery
- Decorative lines without information value
- Shapes added only to occupy whitespace
- Duplicate footer lines
- Stray short Accent lines
- Text flattened into images
- Screenshots of tables
- Full-width Japanese slash `／`

Use the half-width slash `/` throughout the presentation.

## 6. Content fidelity

When redesigning an existing presentation:

- Preserve original text exactly unless editing is explicitly requested.
- Preserve factual meaning and slide order unless restructuring is requested.
- Do not silently summarize, rewrite, merge, or duplicate source content.
- Remove old objects completely before replacing a layout.
- Compare each generated slide with its corresponding source slide.

Maintain a slide-level inventory:

```yaml
slide_number:
source_title:
source_text_blocks:
source_tables:
source_list_items:
source_diagram_labels:
content_must_remain_exact: true
```

Any mismatch must be reviewed before release.

## 7. Required reasoning order

```text
Audience and purpose
  ↓
Primary slide message
  ↓
Information relationship
  ↓
Presentation pattern
  ↓
Information blocking
  ↓
Typography
  ↓
Spacing and alignment
  ↓
Color and stroke
  ↓
PowerPoint implementation
  ↓
Deck-wide validation
```

Do not choose a table, card, or diagram because it is visually available. Representation follows the information relationship.

## 8. Standard slide anatomy

### 8.1 Header

A standard content-slide header contains:

1. Section number and English label
2. One short Accent section anchor
3. Slide title
4. Subtitle or lead sentence when required

Rules:

- Keep the Accent anchor visually close to the section label.
- Target rendered gap: approximately `4–8 px`.
- If the anchor moves upward, pull the title and following content upward by the same amount.
- Use only one section anchor in the header.
- Do not repeat the Accent anchor under every local heading.

### 8.2 Typography

Use the canonical PowerPoint baseline from `04_Typography.md`:

| Role | Baseline | Use |
|---|---:|---|
| `Typography/Display` | 36 pt | Cover title, hero statement |
| `Typography/Heading/H1` | 28 pt | Slide title |
| `Typography/Heading/H2` | 20 pt | Major local heading |
| `Typography/Body/Large` | 18 pt | Subtitle, lead, key explanation |
| `Typography/Body/Default` | 16 pt | Standard and table content |
| `Typography/Caption` | 11 pt | Footer, source, metadata, secondary label |

Do not shrink text to make a slide fit. Split, restructure, move detail to an appendix, or change the representation.

Japanese uses BIZ UDPゴシック. Latin and numbers follow `04_Typography.md`; do not switch fonts when it creates unstable layout.

### 8.3 Footer

Use one footer system consistently:

- One Primary hairline near the bottom
- Small open circle at each endpoint
- Presentation name below the line, left aligned
- Page number below the line, right aligned

Do not:

- Add an Accent line to the footer
- Add a second neutral line above or below it
- Change line length, weight, or position slide by slide

## 9. Information blocking and spacing

The distance within one meaning block must be smaller than the distance between meaning blocks.

```text
Heading
small gap
Description belonging to the heading

larger gap

Next heading
small gap
Next description
```

PowerPoint target:

| Relationship | Target |
|---|---:|
| Heading → description | `4–8 pt` |
| Lines inside one item | Tight, approximately `1.0–1.15` line spacing |
| Item → next item | `16–24 pt` |
| Major block → next block | `24–48 pt` |

Rule:

```text
Inter-item gap ≥ 2 × intra-item gap
```

For lists:

- Keep a heading close to its own description.
- Leave more space between separate items.
- Do not let a description look closer to the next heading.
- Use bullets only when items are independently scannable.
- Do not use decorative icon bullets.

For columns:

- Align equivalent headings and content starts.
- Do not force equal heights when meaning differs.
- Do not create equal boxes only for symmetry.

## 10. Color application

Canonical source: `03_Color_System.md`.

| Role | Value or token | Use |
|---|---|---|
| Structure / Primary | `#173A63` | Titles, structure, diagram lines, hierarchy |
| Focus / Accent | `#29B6E8` | Selected node, focal relationship, section anchor |
| Subtle border | `primary.200` or approved neutral divider | Tables, light boundaries, secondary connections |
| Canvas | White or approved neutral canvas | Main background |

Rules:

- Neutral surfaces dominate.
- Primary creates the system.
- Accent directs attention within the system.
- Accent normally remains below approximately `10%` of visible area.
- Do not use Accent under every heading.
- Do not introduce unrelated hues for variety.
- Color is never the only carrier of meaning.

## 11. Lines, strokes, and connectors

Use lines only for:

- Table row separation
- Necessary column division
- Process connection
- Diagram relationships
- Footer navigation
- Boundaries that whitespace alone cannot clarify

Do not use lines for:

- Filling empty space
- Underlining every heading
- Arbitrary rhythm
- Repeating the same emphasis

### 11.1 Accent micro-rule

A short Accent line may be used for:

- The main section anchor
- One deliberate focal local heading when necessary

Limits:

- Maximum one header anchor per slide
- Maximum one additional local Accent line per major region
- Never under every card title or list heading
- Remove any line that cannot be explained semantically

### 11.2 Connector endpoints

For processes, timelines, and maturity scales:

- Connector starts at the center of the first node.
- Connector ends at the center of the final node.
- It never extends beyond the final defined step.
- Labels align to node centers.
- Text and geometry share the same horizontal rhythm.

## 12. Radius and containment

PowerPoint default:

```text
radius.none
```

Use square corners for tables, process lanes, comparison regions, roadmaps, and structural panels.

Use a small radius only when the object is semantically a card or callout.

Rules:

- Do not use large radius in standard slides.
- Do not use radius as a substitute for grouping.
- Do not mix several radius levels without semantic reason.
- Do not wrap every region in a container.
- Avoid containers inside containers.

### One containment layer

A slide should generally have no more than one dominant containment layer.

- If process lanes are contained, supporting lists remain open.
- If governance modules use cards, do not add an outer card.
- If a table defines structure, do not place a large card behind it.

## 13. Pattern selection

| Relationship | Preferred pattern | Avoid |
|---|---|---|
| One conclusion | Statement / Purpose | Multiple equal boxes |
| Precise matrix | Native Table | Manually aligned text and lines |
| A changes into B | Transition Comparison | Static table without direction |
| Two states or choices | Open Two-column Comparison | Decorative cards |
| Ordered steps | Process / Workflow | Equal cards without connection logic |
| Time or maturity | Timeline / Roadmap | Table when sequence is primary |
| Closed feedback system | Cycle / System Architecture | Generic AI image |
| Independent governance areas | Modular Cards | Long table hiding independence |
| Knowledge domains | Open Knowledge Clusters | Uniform card grid by default |
| Metrics | Metric Modules | Decorative icons and shadows |

## 14. Pattern specifications

### 14.1 Cover / system architecture

Use when the thesis is a connected system or operating model.

- Large title on the left
- Editable system diagram on the right
- Strong whitespace
- Primary structure and Accent focal nodes
- Minimal metadata

Do not use cards, generic AI imagery, or unnecessary vertical rules beside body lines.

### 14.2 Purpose / statement

Use for objectives, intent, and conclusions.

- Large title and lead
- Open semantic rows or blocks
- Whitespace as the main separator
- Optional concluding statement near the bottom

Do not convert every statement into a card.

### 14.3 Native table

Use when precise row-and-column lookup is required.

Implementation requirements:

- Use a real PowerPoint table object.
- Vertically center text in all cells.
- Keep text away from vertical dividers.
- Use restrained horizontal rules and a clear header.

| Property | Target |
|---|---:|
| Vertical alignment | Middle |
| Left / right padding | `10–16 pt` |
| Top / bottom padding | `6–10 pt` |
| Primary content | `Typography/Body/Default` |
| Secondary label | `Typography/Caption` only when genuinely secondary |

If the table does not fit, split rows, reduce columns through grouping, move detail to an appendix, or use another pattern. Do not shrink primary content below the canonical body minimum.

### 14.4 Open knowledge clusters

Use for knowledge domains or categories that do not require comparison.

- Two or three open columns
- Heading and description form one block
- Large gap between items
- No outer card
- No repeated underline under every heading

### 14.5 Open two-column comparison

Use for static contrast.

- Two open columns
- One heading per column
- Optional single structural rule below each column heading
- Whitespace between list items
- Central divider only when necessary

### 14.6 Transition comparison: A → B

Use when the primary meaning is transformation.

- Left state
- Central directional arrow with visible height
- Right state
- Lists grouped by meaning
- Optional bottom conclusion

Rules:

- Arrow must communicate movement, not appear decorative.
- Do not add unnecessary Accent lines below state headings.
- Use one Primary or neutral rule if a heading boundary is needed.
- Keep bullets and their text intact.
- Use `/`, never `／`, in compound phrases.

### 14.7 Process / workflow

Use for ordered operational steps.

- Numbered nodes
- Connector ending at the final node
- Main label and description centered to the node
- Optional As-Is and To-Be lanes
- Open supporting lists below

Rules:

- Do not extend the line beyond the last node.
- Do not enclose both upper lanes and lower lists in four equal cards.
- If upper lanes are contained, lower explanation remains open.
- Use square-corner panels when containment is necessary.

### 14.8 Timeline / roadmap / maturity

Use for time, sequence, or progressive maturity.

- One continuous axis
- Nodes or phases
- Clear current and target states
- Supporting descriptions below relevant regions

Rules:

- Axis ends at the final phase.
- Do not add floating Accent lines above conclusions.
- Do not add a secondary neutral line above the footer.

### 14.9 Modular cards

Use only when each item is an independent module.

Approved examples:

- Governance domains
- KPI modules
- Distinct project phases with substantial content
- Independent callouts

Rules:

- Cards are not the default.
- Use fewer, larger cards.
- Internal padding target: `24–32 pt`.
- Use square corners or the smallest valid radius.
- No shadows.
- No icons unless they improve recognition.
- No dashboard-like grid unless content is genuinely modular.

### 14.10 Cycle / system architecture

Use for feedback loops and connected operating models.

- Semantic nodes
- Primary directional connection
- Accent only for selected nodes or active relationships
- Thin secondary lines only when they clarify structure

Every line must represent a relationship. Avoid decorative orbit lines and excessive complexity.

## 15. Balance across a deck

Do not force one pattern onto every slide.

Use:

- Tables for precise lookup
- Open blocks for explanation and knowledge groups
- Transition comparison for A → B
- Process diagrams for ordered steps
- Roadmaps for progression
- Cards for independent modules only
- Cycle diagrams for connected systems

Consistency comes from shared typography, spacing, color, footer, and quality rules—not from using the same box everywhere.

## 16. Native PowerPoint editability

Use:

- Native text boxes
- Native PowerPoint tables
- Native shapes
- Native connectors and lines
- Native charts when required
- Grouped shapes only when grouping improves editing

Do not use:

- Full-slide generated PNGs
- Rasterized text
- Screenshots of tables
- One-image diagrams when editable shapes are possible
- Invisible duplicate text behind images

## 17. Generation workflow

### Stage 1: Read

Read this document, canonical Color and Typography files, the source PowerPoint, and all user constraints.

### Stage 2: Inventory

Create a slide inventory and preserve exact content when required.

### Stage 3: Classify

Assign one semantic pattern to every slide:

```yaml
pattern:
  cover
  statement
  native-table
  open-knowledge-clusters
  open-comparison
  transition-comparison
  process
  roadmap
  modular-cards
  system-cycle
```

### Stage 4: Specify

Example:

```yaml
slide_id: S21
story_role: Explain transformation from vendor dependency to vendor utilization
message: Internal quality standards convert vendor work into reusable organizational assets
information_relationship: transition
pattern: transition-comparison
primary_component: directional-comparison
containment: open
radius: none
accent_usage: transition-focus-only
footer: standard
content_fidelity: exact
```

### Stage 5: Build master elements

Verify canvas, section label, Accent anchor, title roles, footer line, footer label, and page number before individual slides.

### Stage 6: Build by pattern

Do not copy a previous slide layout when the information relationship differs.

### Stage 7: Propagate deck-wide

When a rule changes:

1. Identify affected patterns.
2. Identify all slides using those patterns.
3. Apply the correction to every affected slide.
4. Do not patch only the slide cited by the reviewer.

Examples:

- Radius change → review every contained surface.
- Accent-line change → review every header and local heading.
- Table-padding change → review every table.
- Footer change → review every content slide.
- Connector change → review every process, timeline, and maturity slide.

### Stage 8: Render and audit

Render all slides, not only edited slides.

Required inspection:

- Individual full-size renders
- Full-deck montage
- 100% crops for tables and dense slides

Review for partial application, accidental radius, repeated cards, stray Accent lines, footer drift, title drift, density imbalance, duplication, omission, overflow, and clipping.

## 18. Release gates

### Gate 1: Content fidelity

- No text changed without permission.
- No duplication or omission.
- Source mapping verified.

### Gate 2: Native editability

- Text editable.
- Tables native.
- Diagrams editable.
- No flattened slides unless approved.

### Gate 3: Typography and blocking

- Canonical roles used.
- Primary content not below the canonical minimum.
- Heading and description grouped correctly.
- Inter-item gap larger than intra-item gap.

### Gate 4: Tables

- Vertical alignment is middle.
- Padding is sufficient.
- Text does not touch dividers.
- Table pattern used only for tabular relationships.

### Gate 5: Structural graphics

- Lines end at final nodes.
- Labels align to nodes.
- Arrows communicate direction clearly.
- Every diagram line has meaning.

### Gate 6: Containment and radius

- Default radius is none.
- Cards used only for independent modules.
- No multiple competing containment layers.

### Gate 7: Accent and line audit

- No stray Accent lines.
- No repeated Accent line under every heading.
- No duplicate footer line.
- No decorative line without meaning.

### Gate 8: Deck-wide consistency

- Same patterns follow the same rules.
- Corrections applied deck-wide.
- Footer, header, color, and typography consistent.
- All slides reviewed in montage view.

## 19. Confirmed failure modes

### Partial application

A cited slide is fixed while other slides using the same pattern remain unchanged.

Prevention: maintain a slide-to-pattern map and propagate every rule deck-wide.

### Excessive rounded containers

Process, roadmap, governance, and supporting lists all use rounded cards.

Prevention: default to `radius.none`, use one containment layer, keep supporting lists open.

### Stray Accent lines

Short blue lines appear above conclusions, under every heading, or in unrelated regions.

Prevention: use Accent only for the section anchor or a deliberate focal relationship and audit every Accent object after rendering.

### Overextended process line

Connector continues after the final step.

Prevention: bind endpoints to the first and final node centers.

### Weak information blocking

A description appears closer to the next heading than to its own heading.

Prevention: reduce heading-to-description gap and increase item-to-item gap.

### Table text too small or misaligned

Text is bottom-heavy, touches vertical dividers, or is unreadable.

Prevention: use native tables, middle alignment, sufficient padding, and split slides instead of shrinking type.

### Duplicate or ghost content

Old layout objects remain after replacement or source content is repeated.

Prevention: clear replaced regions completely and compare source and generated object inventories.

## 20. Reusable AI instruction

```text
Read and follow LINKGENT PowerPoint Presentation Visual Direction.

Preserve all source text exactly unless editing is explicitly requested.
Classify every slide by its information relationship before selecting a layout.
Use native PowerPoint objects: editable text, shapes, connectors, charts, and real PowerPoint tables.
Do not flatten slides into images.

Use BIZ UDPゴシック for Japanese.
Use the canonical LINKGENT typography roles and minimum sizes.
Use Primary #173A63 for structure and Accent #29B6E8 only for limited focal emphasis.
Default to square corners and radius.none.
Do not use gradients, shadows, neon, 3D, decorative icons, generic AI imagery, or meaningless cards.

Use tables only for genuinely tabular relationships.
Use A→B transition layouts for transformation.
Use processes for ordered steps.
Use roadmaps for progression.
Use open knowledge clusters for grouped concepts.
Use cards only for independent modules with sufficient internal padding.

Keep headings close to their descriptions and leave larger gaps between separate items.
Vertically center table text and provide sufficient cell padding.
End process and timeline connector lines at the final defined node.
Use half-width / and never full-width ／.

When a rule changes, identify and update every affected slide across the deck.
Render and review every slide and a full-deck montage before delivery.
Do not claim completion if any slide remains partially updated, clipped, duplicated, or visually inconsistent.
```

## 21. Validation status

Status is `In Review`.

Before promotion to `Active`, validate through one complete regeneration covering:

- Cover
- Purpose slide
- Native table
- Knowledge cluster
- A → B transition
- Process / workflow
- Roadmap / maturity
- Modular governance cards
- System architecture diagram

Validation must confirm reproducibility in a new chat, no reliance on hidden local state, native editability, deck-wide propagation, montage-level quality, and no regression into excessive cards, radius, or decorative Accent lines.
