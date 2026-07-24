# 05_Design_Tokens

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

The LINKGENT Design Token System is the implementation interface between Brand OS meaning and platform-specific values.

It allows humans, AI, design tools, presentation software, and code to apply the same semantic decisions without creating independent visual systems.

```text
Brand meaning
  ↓
Semantic role
  ↓
Design token
  ↓
Platform mapping
  ↓
Rendered value
```

Design tokens are not a replacement for Brand Core, Color, Typography, or Applied Systems. They operationalize those canonical sources.

---

## Inheritance

This file inherits:

1. [`../CONSTITUTION.md`](../CONSTITUTION.md)
2. [`01_Brand_Core.md`](./01_Brand_Core.md)
3. [`03_Color_System.md`](./03_Color_System.md)
4. [`04_Typography.md`](./04_Typography.md)
5. [`09_Layout_System.md`](./09_Layout_System.md) when active

Canonical ownership remains with the source that defines meaning:

- Color meaning and approved values: `03_Color_System.md`
- Typography meaning and approved values: `04_Typography.md`
- Shared layout meaning: `09_Layout_System.md`
- Presentation-specific application: `10_Presentation_System/`

This file owns token architecture, naming, aliasing, platform mapping, and token lifecycle.

---

## Principles

### Semantics Before Values

Use semantic names in production decisions.

Preferred:

```text
color.text.primary
space.content.gap
radius.component.default
```

Avoid:

```text
navy
16px-gap
rounded-card
```

### Primitive, Semantic, Applied

LINKGENT tokens use three layers.

```text
Primitive
  ↓
Semantic
  ↓
Applied
```

| Layer | Purpose | Example |
|---|---|---|
| Primitive | Stable raw value inventory | `color.blue.800` |
| Semantic | Meaning independent of surface | `color.structure.primary` |
| Applied | Context-specific implementation | `presentation.color.section-anchor` |

Applied tokens may alias semantic tokens. They must not redefine Brand OS-wide meaning.

### One Meaning, Multiple Platforms

The same token may map differently where platform units or rendering differ. The semantic outcome must remain consistent.

### Controlled Expansion

Do not add a token because one artifact needs a convenient value. Add a token only when the role is reusable, explainable, and governed.

---

## Token Naming

Canonical format:

```text
category.role.variant.state
```

Examples:

```text
color.text.primary
color.background.canvas
space.layout.section
stroke.divider.subtle
presentation.space.safe-area
```

Rules:

- Use lowercase kebab-case or dot notation consistently in exported systems.
- Name meaning, not appearance.
- Do not encode a platform in a semantic token.
- Use platform prefixes only in implementation mappings.
- Do not encode arbitrary numbers in semantic names.
- Use states only when behavior changes meaningfully.

---

## Token Lifecycle

Tokens use:

```text
draft → candidate → stable → deprecated → archived
```

| Status | Meaning |
|---|---|
| `draft` | Proposed; incomplete or untested |
| `candidate` | Defined and available for controlled use |
| `stable` | Validated in required platforms and approved for normal use |
| `deprecated` | Existing use supported temporarily; no new use |
| `archived` | Historical only |

Current token set status:

```yaml
status: candidate
```

No token becomes `stable` solely because it is documented.

---

## Token Contract

Every token or token group must define:

```yaml
name:
layer: primitive | semantic | applied
purpose:
canonical_source:
status: draft | candidate | stable | deprecated | archived
value_or_alias:
platform_mappings:
accessibility_constraints:
introduced_in:
replaced_by:
known_limitations:
```

---

## Color Tokens

Color values and accessibility decisions are canonical in [`03_Color_System.md`](./03_Color_System.md).

### Semantic Roles

```text
color.background.canvas
color.background.surface
color.background.subtle
color.text.primary
color.text.secondary
color.text.inverse
color.structure.primary
color.emphasis.focal
color.border.default
color.border.strong
color.state.success
color.state.warning
color.state.error
color.state.info
```

### Applied Presentation Roles

```text
presentation.color.canvas
presentation.color.section-anchor
presentation.color.primary-message
presentation.color.focal-data
presentation.color.supporting-data
presentation.color.divider
presentation.color.source-text
```

Presentation mappings must comply with canonical Color Rule IDs, including:

- `COLOR-CONTRAST-NORMAL`
- `COLOR-CONTRAST-LARGE`
- `COLOR-ACCENT-INVERSE-PROHIBITED`
- `COLOR-FOCAL-AREA-GUIDANCE`
- `COLOR-NOT-SOLE-CARRIER`

Raw color values must not be copied into downstream Applied System files when a canonical token exists.

---

## Typography Tokens

Typography values and hierarchy are canonical in [`04_Typography.md`](./04_Typography.md).

```text
typography.display
typography.heading.h1
typography.heading.h2
typography.body.large
typography.body.default
typography.caption
```

Each typography token includes:

```yaml
font_family:
font_size:
font_weight:
line_height:
letter_spacing:
semantic_role:
```

Presentation implementations must comply with:

- `TYPE-PRESENTATION-MIN-BODY`
- `TYPE-PRESENTATION-MIN-CAPTION`
- `TYPE-PRESENTATION-HIERARCHY`

Do not create local typography tokens to make overflowing content fit.

---

## Spacing Tokens

Spacing creates relationship, rhythm, and cognitive grouping.

### Primitive Scale

The initial candidate scale uses a 4-unit foundation:

| Token | Value | Typical Use |
|---|---:|---|
| `space.0` | 0 | No separation |
| `space.1` | 4 | Micro separation |
| `space.2` | 8 | Tight internal gap |
| `space.3` | 12 | Compact component gap |
| `space.4` | 16 | Default internal gap |
| `space.5` | 24 | Related group separation |
| `space.6` | 32 | Component separation |
| `space.7` | 48 | Section separation |
| `space.8` | 64 | Major structural separation |
| `space.9` | 96 | Large composition separation |

Values are implementation primitives. Applied Systems should reference semantic roles.

### Semantic Spacing

```text
space.inline.tight
space.inline.default
space.content.compact
space.content.default
space.content.relaxed
space.section.default
space.section.major
space.layout.safe
```

### Presentation Spacing

```text
presentation.space.safe-area
presentation.space.title-to-content
presentation.space.component-gap
presentation.space.section-gap
presentation.space.caption-gap
```

Presentation spacing is proportional to the canvas and may map to platform-specific units. [`10_Presentation_System/Layout.md`](./10_Presentation_System/Layout.md) owns presentation application.

---

## Radius Tokens

Radius must not be used to create arbitrary visual variety.

| Token | Candidate Role |
|---|---|
| `radius.none` | Tables, structural dividers, strict containers |
| `radius.small` | Compact controls or labels |
| `radius.default` | Standard cards and callouts |
| `radius.large` | Large contained surfaces only |
| `radius.pill` | Status labels and compact tags only |

Semantic aliases:

```text
radius.component.default
radius.component.compact
radius.label.pill
```

Rules:

- Use the smallest radius that supports the component purpose.
- Do not mix several radii on one surface without semantic reason.
- Do not use radius as a substitute for grouping or hierarchy.

---

## Stroke Tokens

```text
stroke.none
stroke.hairline
stroke.default
stroke.strong
```

Semantic aliases:

```text
stroke.divider.subtle
stroke.container.default
stroke.focus.strong
stroke.data.emphasis
```

Stroke width must remain visible after export, projection, and platform conversion.

---

## Shadow Tokens

LINKGENT uses shadows sparingly.

```text
shadow.none
shadow.surface.subtle
shadow.overlay.default
```

Rules:

- Default to `shadow.none` in presentations.
- Use shadow only when it clarifies elevation or separation.
- Do not use glow, neon, or dramatic soft shadows as futuristic decoration.
- Do not combine shadow and border unless both serve distinct purposes.

---

## Grid and Layout Tokens

Common semantic roles:

```text
layout.column.count
layout.gutter.default
layout.margin.default
layout.container.max
layout.safe-area
```

Presentation applied roles:

```text
presentation.grid.columns
presentation.grid.gutter
presentation.grid.safe-area
presentation.layout.content-width
presentation.layout.vertical-rhythm
```

The Presentation System owns the applied behavior; this file owns token structure.

---

## Motion Tokens

Motion must communicate state, sequence, causality, or focus.

```text
motion.duration.instant
motion.duration.fast
motion.duration.default
motion.duration.slow
motion.easing.standard
motion.easing.enter
motion.easing.exit
```

Presentation rule:

- Use motion only when it improves understanding.
- Provide a no-motion equivalent.
- Avoid motion that changes reading order unpredictably.
- Do not use motion as proof of technical sophistication.

---

## Platform Mapping

### PowerPoint

Map semantic tokens into:

- Theme colors
- Theme fonts
- Slide Master placeholders
- Shape styles
- Table styles
- Chart series styles

### Google Slides

Map into:

- Theme colors
- Theme fonts
- Master layouts
- Reusable copied components

### Keynote

Map into:

- Master slides
- Paragraph styles
- Shape styles
- Chart styles

### Canva

Map into:

- Brand Kit colors
- Brand fonts
- Approved templates
- Locked and editable component groups

### Figma and Figma Slides

Map into:

- Variables
- Text styles
- Effect styles
- Component properties
- Modes when semantic context changes

### AI Systems

AI must use semantic token names and Rule IDs in specifications. Raw values may be rendered only at the implementation stage.

Preferred:

```text
Use presentation.color.section-anchor.
```

Avoid:

```text
Use a dark blue rectangle.
```

---

## Source Format

The future machine-readable source should follow Design Tokens Community Group-compatible concepts where practical.

Candidate structure:

```json
{
  "color": {
    "text": {
      "primary": {
        "$type": "color",
        "$value": "{color.neutral.900}",
        "$description": "Primary readable content"
      }
    }
  }
}
```

Markdown remains the governance source until a machine-readable token package is approved.

---

## Validation

Before `1.0.0 / Active`, validate:

- Color alias accuracy
- Typography alias accuracy
- Presentation platform mappings
- Export behavior
- AI semantic interpretation
- Token naming consistency
- Accessibility constraints
- Deprecated token migration

---

## Release Position

This document is suitable for controlled use as a token architecture and candidate mapping source.

It remains `Release Candidate` until:

- A machine-readable token source is created
- At least PowerPoint, Figma, and one additional platform are mapped
- Presentation Golden Deck validation is completed
- Token drift checks are established
