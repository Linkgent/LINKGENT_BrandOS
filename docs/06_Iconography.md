# 06_Iconography

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

The LINKGENT Iconography System defines how icons communicate actions, objects, states, categories, and relationships across brand touchpoints.

Icons are functional language. They are not decorative illustrations or visual filler.

The system exists to make icon use:

- Recognizable
- Consistent
- Accessible
- Cross-platform
- AI-readable
- Maintainable

---

## Inheritance

This file inherits:

1. [`../CONSTITUTION.md`](../CONSTITUTION.md)
2. [`01_Brand_Core.md`](./01_Brand_Core.md)
3. [`03_Color_System.md`](./03_Color_System.md)
4. [`04_Typography.md`](./04_Typography.md)
5. [`05_Design_Tokens.md`](./05_Design_Tokens.md)

This file is the canonical owner of icon family, semantic use, sizing logic, accessibility, and platform implementation rules.

Applied Systems may define context-specific icon use but must not create an independent icon language.

---

## Canonical Family

Rule ID:

```text
ICON-PRESENTATION-FAMILY
```

Canonical default:

```text
Material Symbols Outlined
```

Use the Outlined family as the default across presentations, documents, internal systems, and early digital implementations unless a documented platform limitation requires another mapping.

The selection supports:

- Broad semantic coverage
- Consistent construction
- Cross-platform availability
- Variable weight and grade
- Reliable AI identification
- Accessible pairing with text labels

Use one family within an artifact. Do not mix Outlined, Rounded, Sharp, Filled, and unrelated icon libraries without an approved semantic reason.

---

## Icon Principles

### Meaning Before Decoration

Use an icon only when it improves recognition, scanning, orientation, or comprehension.

Do not add icons merely to make a slide, card, or bullet list look designed.

### Text Remains Primary for Critical Meaning

An icon must not be the sole carrier of essential information unless the symbol is universally understood in context and has an accessible name.

### Consistency Without Uniformity

Icons should share a family and construction logic. Size and emphasis may vary according to hierarchy and context.

### Familiarity Before Novelty

Prefer established symbols over custom metaphors when the established symbol is clear.

### Minimal Expression

Use the smallest number of icons necessary. Repeated decorative icons create noise and weaken hierarchy.

---

## Semantic Roles

Icons may serve the following roles:

| Role | Purpose |
|---|---|
| Action | Indicates an operation or next step |
| Object | Represents a recognizable item or entity |
| Navigation | Supports movement or orientation |
| Status | Communicates state or condition |
| Category | Helps distinguish recurring content groups |
| Relationship | Clarifies connection, sequence, or direction |
| Annotation | Adds a compact supporting cue |

Icons must not replace charts, diagrams, evidence, or explanatory content when those representations are required.

---

## Naming

Use the canonical Material Symbol name when available.

```text
Icon/action/search
Icon/status/check_circle
Icon/navigation/arrow_forward
Icon/object/description
```

Naming principles:

- Use semantic category and canonical symbol name.
- Do not name by color, location, or arbitrary visual appearance.
- Record aliases only when user language differs materially from the source name.
- Avoid organization-specific meanings for common symbols unless documented.

---

## Style Configuration

Candidate default configuration:

```yaml
family: Material Symbols Outlined
fill: 0
weight: 400
grade: 0
optical_size: context-dependent
```

Variation is allowed only when it communicates hierarchy, interaction state, or platform necessity.

### Weight

- Default to the standard family weight.
- Align perceived weight with adjacent typography and strokes.
- Do not use heavy icons beside light text without purpose.

### Fill

- Default to unfilled Outlined icons.
- Filled state may indicate selection, activation, or a strong status only when the distinction is documented.
- Do not mix filled and outlined icons as arbitrary visual variety.

### Grade

Use grade adjustments sparingly to improve optical balance without changing dimensions.

---

## Size

Icon size must follow context and adjacent text rather than arbitrary preference.

Semantic roles:

```text
icon.size.inline
icon.size.control
icon.size.component
icon.size.feature
```

Rules:

- Inline icons should align optically with text.
- Component icons must not dominate the message.
- Feature icons may be larger only when the icon is a meaningful primary identifier.
- Very small icons must remain recognizable after export and projection.
- Do not enlarge low-information icons to fill empty space.

Platform-specific numeric mappings belong in implementation assets or Design Tokens.

---

## Color

Icon color must use semantic Color tokens.

Preferred roles:

```text
color.icon.primary
color.icon.secondary
color.icon.inverse
color.icon.status.success
color.icon.status.warning
color.icon.status.error
color.icon.status.info
```

Rules:

- Use the same semantic state color as the associated text or status component.
- Do not use color as the only distinction between icon states.
- Do not create multicolor icons unless the icon is a controlled brand asset.
- Do not recolor icons merely for variety.
- Preserve required contrast against the background.

---

## Labels

Pair icons with text when:

- The meaning is unfamiliar
- The audience is broad or mixed
- The action is consequential
- The icon may have several interpretations
- Accessibility requires an explicit name

Labels should describe the action or meaning, not the icon shape.

Preferred:

```text
Download report
```

Avoid:

```text
Down arrow icon
```

---

## Accessibility

### Accessible Name

Interactive icons require an accessible name in digital environments.

Decorative icons should be hidden from assistive technology when the same meaning is already expressed in adjacent text.

### Redundancy

Status and meaning must be communicated through at least one additional cue:

- Text label
- Shape
- Position
- Pattern
- Explicit annotation

### Contrast

Icons carrying information must meet the applicable canonical contrast requirements from `03_Color_System.md`.

### Touch and Control Size

Interactive hit areas must follow the target platform accessibility standard. The visible icon does not define the full hit area.

### Motion

Animated icons require a static equivalent and must not create distraction or vestibular risk.

---

## Presentation Application

Presentation icons should support rapid scanning without turning every content block into an icon card.

Use icons for:

- Repeated categories
- Compact status communication
- Process annotations
- Navigation cues
- Familiar actions

Avoid icons for:

- Decorative bullets
- Every heading
- Abstract strategic concepts that require explanation
- Replacing evidence
- Filling unused space
- Simulating visual sophistication

A presentation may contain no icons. Icon absence is not a design failure.

---

## Diagram Application

Icons inside diagrams must:

- Use one family
- Share consistent scale
- Align to the diagram grid
- Preserve label proximity
- Avoid becoming the dominant visual unless the object identity is essential
- Remain understandable when printed or exported

Icons do not replace relationship lines, hierarchy, sequence, or labels.

---

## Custom Icons

Create a custom icon only when:

- No canonical symbol communicates the required meaning
- The concept is recurring and strategically important
- A custom icon improves recognition materially
- The icon can follow the construction and accessibility system

Custom icon documentation must include:

```yaml
name:
purpose:
status:
owner:
source_files:
construction_grid:
optical_corrections:
platform_support:
accessibility_name:
known_limitations:
```

Do not create one-off custom icons for a single slide unless they function as illustration rather than system iconography.

---

## Platform Mapping

### PowerPoint

- Use SVG when editability and quality are preserved.
- Maintain one source library.
- Avoid mixing pasted raster icons and font glyphs.
- Confirm export and Windows compatibility.

### Google Slides

- Prefer SVG or supported vector insertion.
- Confirm that color and proportions survive import.

### Keynote

- Preserve vector editability where possible.
- Confirm PDF export and cross-platform conversion.

### Canva

- Use approved Brand Kit or project assets.
- Do not substitute visually similar icons from unrelated families.

### Figma and Figma Slides

- Use a controlled component library.
- Expose semantic icon name and state properties.
- Preserve accessible labels in specifications.

### AI Systems

AI must specify icons by canonical semantic name.

Preferred:

```text
Use Icon/status/check_circle with the success semantic role.
```

Avoid:

```text
Add a nice green icon.
```

AI must not invent a symbol when a canonical icon exists.

---

## Icon Contract

Every approved custom icon or controlled mapping must define:

```yaml
name:
semantic_role:
canonical_symbol:
family:
status: draft | candidate | stable | deprecated
owner:
introduced_in:
platform_support:
tested_in:
accessibility_status:
known_limitations:
replaced_by:
```

---

## Prohibited Use

Do not:

- Mix unrelated icon families
- Use icons as decorative bullets
- Use an icon without a clear meaning
- Use emoji as system icons
- Use color as the only status cue
- Distort proportions
- Add uncontrolled shadows, gradients, or 3D effects
- Use generated icons as approved assets without review
- Present an unfamiliar icon without a label
- Use an icon as a substitute for a required explanation

---

## Validation

Before `1.0.0 / Active`, validate:

- PowerPoint use and export
- Google Slides import
- PDF output
- Figma component mapping
- Canva availability or approved asset workflow
- AI symbol-name interpretation
- Small-size recognition
- Accessibility naming and redundancy

---

## Release Position

This document establishes the canonical candidate icon family and operational rules.

It remains `Release Candidate` until platform libraries and validation records are complete.
