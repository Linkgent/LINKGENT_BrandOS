# Color System

> Version: 1.0  
> Status: Active  
> Owner: LINKGENT  
> Last Updated: 2026-07-24

---

## Purpose

The LINKGENT Color System defines how color communicates structure, hierarchy, meaning, state, and action across the brand.

It is not a collection of decorative colors. It is an information-design system derived from the Brand Core principle:

> **Structure creates understanding.**

Color must help people understand what matters, how information is organized, what requires attention, and what action is possible.

This document is the canonical source for:

- Color meaning
- Approved color values
- Color hierarchy
- Semantic color roles
- Accessibility and contrast requirements
- Cross-media color behavior
- Color-specific AI generation rules

This document does not define:

- Logo construction or logo-specific color placement, which belong to `02_Visual_Identity.md`
- Platform token syntax, naming conventions, or code serialization, which belong to `05_Design_Tokens.md`
- Component-specific color implementation, which belongs to the relevant Applied System
- General AI behavior outside color selection, which belongs to `13_AI_Generation_Rules.md`

### System Objective

The Color System must remain stable across:

- PowerPoint
- Web
- UI
- Figma
- Canva
- Word and Google Docs
- Illustrator and Photoshop
- Print
- AI-generated presentations, interfaces, documents, and images

The same visual output is not required in every medium. The same meaning, hierarchy, and quality standard are required.

---

## Color Philosophy

### Color Makes Structure Visible

LINKGENT uses color to reveal relationships that already exist in the information.

Color may indicate:

- Hierarchy
- Grouping
- Priority
- Status
- Action
- Navigation
- Comparison
- Focus
- System feedback

Color must not be used to compensate for unclear content, weak hierarchy, or poor layout.

### Color Supports Understanding

The purpose of color is not to make an artifact look more designed. Its purpose is to reduce cognitive burden and improve comprehension.

A successful use of color helps a person answer questions such as:

- What is the main structure?
- What is primary and what is secondary?
- What changed?
- What requires action?
- What is safe, risky, complete, selected, or unavailable?
- What belongs together?

### Beauty Through Restraint

LINKGENT is beautiful, minimal, sophisticated, and calm.

Beauty is created through intentional contrast, disciplined use, meaningful repetition, and sufficient whitespace—not through color quantity.

Neutral colors should carry most surfaces and text. Corporate and semantic colors should appear only where they create meaning.

### Trust Through Consistency

The same meaning should use the same color role across media.

For example:

- Error must not appear red in one artifact and blue in another.
- Accent must not mean action in one screen and decoration in another.
- Primary must not be used randomly when hierarchy is unclear.

Consistent meaning creates predictability. Predictability supports trust.

### Human-Centered Accessibility

Color is only successful when people can perceive and understand it.

Accessibility is not an exception to visual quality. It is part of brand quality.

Color must never be the only carrier of essential meaning.

---

## Design Principles

### 1. Semantics Before Decoration

Choose color from the meaning of the content, not from personal preference or visual novelty.

Use this sequence:

```text
Intent
  ↓
Information Role
  ↓
Semantic Color Role
  ↓
Approved Palette Value
  ↓
Media-Specific Application
```

Do not begin with a HEX code.

### 2. Structure Before Emphasis

Primary color establishes structure and hierarchy.

Accent color creates selective emphasis.

Semantic color communicates system meaning.

Neutral color carries content, surfaces, boundaries, and visual rhythm.

These responsibilities must not be exchanged casually.

### 3. One Color, One Primary Meaning

A color may support several related uses, but it should not communicate contradictory meanings.

Examples:

- Accent may indicate action, focus, or a selected important point.
- Accent must not also indicate warning or failure.
- Error red may indicate destructive or failed states.
- Error red must not be used as a decorative highlight.

### 4. Neutral First

When meaning can be communicated through typography, spacing, layout, or neutral contrast, use those methods first.

Add corporate or semantic color only when it improves understanding.

### 5. Contrast Creates Hierarchy

Hierarchy should be created through controlled differences in:

- Lightness
- Saturation
- Surface depth
- Text contrast
- Border contrast

Do not create hierarchy by introducing unrelated hues.

### 6. Roles Before Raw Values

People and AI should select semantic roles such as `text.primary`, `background.subtle`, or `status.error.strong` before selecting a raw color value.

Raw palette values are implementation primitives. Semantic roles are the decision layer.

Formal token syntax and platform mappings are defined in `05_Design_Tokens.md`.

### 7. Stable System, Flexible Identity

The Color System is not derived from the logo.

The logo may use colors from this system, but the logo does not own or redefine the system.

If the logo changes in the future:

- Logo-specific mappings may change in `02_Visual_Identity.md`.
- Corporate color meaning and semantic roles remain unchanged unless a Brand Director review explicitly changes them.
- Applied systems should continue to reference semantic roles rather than logo artwork.

### 8. Accessible by Default

Approved values do not guarantee an accessible result.

Every foreground and background combination must be evaluated in its actual context, including opacity, size, weight, state, and medium.

### 9. Human and AI Read the Same Rules

Rules must be explicit enough that a designer, developer, editor, or AI system can reach the same decision.

When a rule is uncertain, prefer the most restrained valid option:

```text
Neutral
  → Primary
  → Accent
  → Semantic color
  → New color only after system review
```

---

## Color Architecture

The LINKGENT Color System has three layers.

### Layer 1: Primitive Palette

Primitive colors are approved raw values.

They include:

- Primary scale
- Accent scale
- Neutral scale
- Semantic support colors

Primitive values must not be selected only because they look appropriate.

### Layer 2: Semantic Roles

Semantic roles describe why a color is used.

Examples:

- `text.primary`
- `background.canvas`
- `border.subtle`
- `action.primary`
- `status.warning.strong`
- `data.accent`

Semantic roles are the preferred decision interface for people and AI.

### Layer 3: Applied Mappings

Applied mappings define how roles are used in a specific medium or component.

Examples:

- A PowerPoint section divider
- A Web primary button
- A chart series
- A Word callout
- A Figma component state

Applied mappings belong to the relevant Applied System and must inherit this document.

---

## Corporate Color

Corporate colors express LINKGENT's identity and information philosophy.

They are system anchors, not unrestricted decorative colors.

### Primary

| Role | Value | Meaning |
|---|---:|---|
| Primary | `#173A63` | Structure, hierarchy, intelligence, reliability, trust |

Primary represents the stable logic of the system.

Use Primary for:

- Major structural anchors
- Top-level hierarchy
- Section identity
- High-confidence information
- Navigation and selected structural states
- Brand headings and key framing elements
- Primary dark surfaces with white text

Do not use Primary for:

- Every heading or border
- Decorative blocks without structural meaning
- Success, warning, or error states
- Large areas when a neutral background would communicate more clearly

### Primary Scale

| Role Label | HEX | Intended Use |
|---|---:|---|
| `primary.900` | `#0C2038` | Deep inverse surfaces, high-emphasis dark framing |
| `primary.800` | `#112C4B` | Dark structural surfaces and hover states |
| `primary.700` | `#173A63` | Corporate Primary; core structural color |
| `primary.600` | `#24517D` | Secondary structural emphasis |
| `primary.500` | `#356A98` | Information graphics and medium emphasis |
| `primary.400` | `#5B88B2` | Supporting graphics; non-essential visual encoding |
| `primary.300` | `#8BAAC8` | Soft borders and low-emphasis graphics |
| `primary.200` | `#B9CCE0` | Dividers, information borders, subtle chart elements |
| `primary.100` | `#DCE7F1` | Information surfaces and selected backgrounds |
| `primary.50` | `#F3F7FA` | Very subtle structural background |

`primary.700` is the canonical corporate value. Other steps support hierarchy and state while preserving the same color family.

### Accent

| Role | Value | Meaning |
|---|---:|---|
| Accent | `#29B6E8` | Attention, action, focus, important point, forward movement |

Accent represents directed energy within a stable structure.

Use Accent for:

- Primary action emphasis
- Focus and selection indicators
- A key point that requires attention
- Links and interactive cues using accessible darker steps
- Limited highlights in diagrams and presentations
- A focal data series when comparison is required

Do not use Accent for:

- Large decorative backgrounds
- Body text at the base value
- White text on `#29B6E8`
- General information that is not actionable or important
- Multiple competing focal points
- Warning or error communication

### Accent Scale

| Role Label | HEX | Intended Use |
|---|---:|---|
| `accent.900` | `#063B4E` | High-contrast hover, pressed, or dark accent text |
| `accent.800` | `#075A75` | Strong interactive emphasis |
| `accent.700` | `#087899` | Accessible link, focus, and interactive text |
| `accent.600` | `#0B96BE` | Strong graphics and active controls |
| `accent.500` | `#29B6E8` | Corporate Accent; focal fill and visual emphasis |
| `accent.400` | `#55C7ED` | Supporting accent graphics |
| `accent.300` | `#83D7F2` | Focus on dark surfaces; secondary graphics |
| `accent.200` | `#B4E7F8` | Accent borders and highlights |
| `accent.100` | `#DDF5FC` | Selected and highlighted surfaces |
| `accent.50` | `#F2FBFE` | Minimal accent-tinted background |

`accent.500` is the canonical corporate accent value. For text, links, borders, and focus indicators on light surfaces, prefer `accent.700` or darker.

### Corporate Color Relationship

Primary and Accent have different responsibilities.

```text
Primary = structure and trust
Accent  = attention and action
```

Primary creates the system.

Accent directs movement within the system.

Accent should normally occupy less visual area than Primary. Neutral colors should occupy more visual area than both.

---

## Semantic Color

Semantic colors communicate a state or meaning that must remain consistent across presentation, product, interface, document, and data visualization contexts.

Semantic color is not brand decoration.

### Semantic Families

| Family | Strong | Default | Border | Subtle Surface | Meaning |
|---|---:|---:|---:|---:|---|
| Success | `#1F6B4F` | `#2E8B67` | `#A9D8C4` | `#EAF6F0` | Complete, healthy, approved, positive outcome |
| Warning | `#7A4B00` | `#B87503` | `#F0CF8C` | `#FFF4DD` | Caution, risk, attention required, pending concern |
| Error | `#9B2C2C` | `#C73E3E` | `#E9A5A5` | `#FDECEC` | Failure, destructive action, invalid state, critical issue |
| Information | `#173A63` | `#356A98` | `#B9CCE0` | `#F3F7FA` | Explanation, context, guidance, neutral system message |

### Semantic Role Pattern

Each semantic family may be used through four role levels:

- `strong`: accessible text, high-emphasis icon, or solid status surface
- `default`: indicator, data mark, or medium-emphasis graphic
- `border`: boundary around a semantic surface
- `subtle`: low-intensity background that supports semantic text

Recommended pairings:

| Surface | Foreground |
|---|---|
| Success subtle | Success strong |
| Warning subtle | Warning strong |
| Error subtle | Error strong |
| Information subtle | Primary or Information strong |
| Success strong | White |
| Warning strong | White |
| Error strong | White |
| Primary strong | White |

Do not assume the `default` step supports white text. Use the verified `strong` step for text-bearing solid semantic surfaces.

### Expanded Semantic Use

Semantic color may communicate more than system notifications.

#### Success

Use for:

- Completed milestones
- Approved decisions
- Positive KPI movement
- Healthy system status
- Resolved issues

Do not use for:

- Generic decoration
- Any positive-looking content without a defined positive meaning
- Revenue or growth by default when the context is neutral comparison

#### Warning

Use for:

- Emerging risk
- Dependency concern
- Incomplete requirement
- Decision needed
- Threshold approaching

Do not use for:

- General emphasis
- Every item that deserves attention
- Non-critical highlighted notes

#### Error

Use for:

- Failed state
- Invalid input
- Critical risk
- Destructive action
- Blocked outcome
- Material negative variance when the meaning is explicitly negative

Do not use for:

- Strong opinions
- Decorative urgency
- Negative numbers that are not necessarily bad in context

#### Information

Use for:

- Explanation
- Guidance
- Context
- Neutral status
- System-generated information
- Supporting callouts

Information is structurally aligned with the Primary family because LINKGENT communicates information through trust and hierarchy rather than through an additional unrelated hue.

### Semantic Priority

When multiple semantic states apply, use the state that most directly affects user understanding or action.

Recommended priority:

```text
Error
  ↓
Warning
  ↓
Success
  ↓
Information
```

This is a communication priority, not a visual instruction to increase saturation.

---

## Neutral Color

Neutral colors are the foundation of the LINKGENT visual system.

They carry most text, backgrounds, borders, tables, charts, and layout structure.

### Neutral Scale

| Role Label | HEX | Intended Use |
|---|---:|---|
| `neutral.1000` | `#0B1320` | Primary text, deepest neutral surface |
| `neutral.900` | `#16202C` | Inverse surfaces, strong text |
| `neutral.800` | `#263445` | High-emphasis secondary text |
| `neutral.700` | `#3B4A5A` | Secondary text and labels |
| `neutral.600` | `#566575` | Tertiary text and metadata |
| `neutral.500` | `#73808D` | Non-essential iconography; limited text use |
| `neutral.400` | `#98A2AC` | Disabled and low-emphasis non-essential content |
| `neutral.300` | `#BBC3CA` | Strong dividers and inactive controls |
| `neutral.200` | `#D8DDE2` | Standard borders and separators |
| `neutral.100` | `#ECEFF2` | Subtle surfaces and disabled backgrounds |
| `neutral.50` | `#F6F8FA` | Canvas variation and section background |
| `neutral.0` | `#FFFFFF` | Primary canvas, elevated surface, inverse text |

### Neutral Temperature

LINKGENT neutrals use a restrained blue-gray character rather than a purely mechanical gray.

This supports:

- Visual compatibility with Primary
- Calm and intelligent expression
- Clear hierarchy without excessive hue
- Sophistication across digital and print media

Neutrals must remain neutral in meaning. They must not communicate success, warning, error, or action by themselves.

---

## Functional Color

Functional colors support interaction, navigation, selection, focus, boundaries, disabled states, and overlays.

They are semantic mappings of the approved palette, not additional color families.

| Functional Role | Value | Rule |
|---|---:|---|
| `action.primary.background` | `#173A63` | Default high-confidence primary action |
| `action.primary.foreground` | `#FFFFFF` | Text or icon on Primary action |
| `action.primary.hover` | `#112C4B` | Hover state |
| `action.primary.pressed` | `#0C2038` | Pressed state |
| `action.accent.background` | `#29B6E8` | Focal action when Accent is strategically required |
| `action.accent.foreground` | `#0B1320` | Required dark foreground on Accent base |
| `link.default` | `#087899` | Accessible link on light surfaces |
| `link.hover` | `#063B4E` | Hover and visited-state candidate when context allows |
| `focus.light-surface` | `#087899` | Focus ring on light backgrounds |
| `focus.dark-surface` | `#83D7F2` | Focus ring on dark backgrounds |
| `selection.background` | `#DDF5FC` | Selected or highlighted surface |
| `selection.border` | `#087899` | Selected state boundary |
| `border.default` | `#D8DDE2` | Standard structural border |
| `border.strong` | `#BBC3CA` | Stronger boundary or active grouping |
| `divider` | `#D8DDE2` | Content separation |
| `disabled.background` | `#ECEFF2` | Disabled surface |
| `disabled.foreground` | `#98A2AC` | Disabled non-essential label or icon |
| `overlay` | `#0B1320` at `60%` | Modal or image overlay |
| `scrim` | `#0B1320` at `40%` | Background de-emphasis |

### Functional Rules

- Primary is the default for high-confidence structural actions.
- Accent is reserved for a focal action, active focus, or a deliberately important interaction.
- A screen, slide, or component group should not contain multiple competing Accent actions.
- Hover, pressed, selected, and focus states must be distinguishable without relying only on subtle color shifts.
- Disabled states must remain identifiable, but disabled text is exempt from contrast requirements only when it is truly unavailable and non-essential.
- Focus indicators must not be removed for visual cleanliness.

---

## Background System

Background color communicates layer, grouping, context, and focus.

It must not become decorative striping.

### Core Background Roles

| Background Role | Value | Use |
|---|---:|---|
| `background.canvas` | `#FFFFFF` | Default page, slide, document, or UI canvas |
| `background.subtle` | `#F6F8FA` | Secondary section or low-emphasis grouping |
| `background.structured` | `#F3F7FA` | Primary-tinted structural region |
| `background.elevated` | `#FFFFFF` | Card, modal, floating panel, or elevated content |
| `background.inverse` | `#0C2038` | Strong framing, dark section, inverse composition |
| `background.accent-subtle` | `#F2FBFE` | Limited focal or selected region |
| `background.selected` | `#DDF5FC` | Explicit selected state |
| `background.disabled` | `#ECEFF2` | Disabled control or unavailable region |

### Background Hierarchy

Preferred order:

```text
Canvas
  ↓
Subtle grouping
  ↓
Structured grouping
  ↓
Elevated surface
  ↓
Inverse section only when strong framing is required
```

### Background Rules

- Use white or a light neutral as the default.
- Use tinted backgrounds to clarify grouping, not to fill empty space.
- Do not alternate many background colors to create rhythm.
- Do not place essential text directly over complex photography without a verified solid or controlled overlay.
- Avoid gradients by default.
- When a gradient is functionally justified, use approved colors from the same family and preserve text contrast across the entire area.
- Dark mode is not defined in this version. Do not automatically invert the light system.

---

## Typography Color

Typography color must communicate hierarchy while preserving readability.

### Text Roles

| Text Role | Value | Use |
|---|---:|---|
| `text.primary` | `#0B1320` | Main body, essential information, primary labels |
| `text.secondary` | `#3B4A5A` | Supporting content and secondary labels |
| `text.tertiary` | `#566575` | Metadata and lower-priority supporting text |
| `text.brand` | `#173A63` | Brand heading or structural emphasis |
| `text.link` | `#087899` | Interactive link on a light surface |
| `text.inverse` | `#FFFFFF` | Text on approved dark surfaces |
| `text.on-accent` | `#0B1320` | Text on `accent.500` |
| `text.disabled` | `#98A2AC` | Truly unavailable, non-essential content only |
| `text.success` | `#1F6B4F` | Success meaning |
| `text.warning` | `#7A4B00` | Warning meaning |
| `text.error` | `#9B2C2C` | Error meaning |
| `text.information` | `#173A63` | Informational meaning |

### Typography Rules

- Body text should normally use `text.primary`.
- Use `text.secondary` and `text.tertiary` to reduce emphasis, not to reduce font size alone.
- Do not use `accent.500` for body text or small labels on light backgrounds.
- Do not use light gray for essential information.
- Colored text must have a semantic or structural reason.
- Underlines, icons, weight, or labels should supplement link and status color when needed.
- Large brand headings may use Primary, but not every heading requires brand color.

---

## Data Visualization Color

Data visualization is part of information design and inherits the same semantic responsibilities.

### Default Series Order

Use the following sequence for categorical data when categories do not already have semantic meaning:

1. `primary.700` — `#173A63`
2. `accent.500` — `#29B6E8`
3. `success.default` — `#2E8B67`
4. `warning.default` — `#B87503`
5. `error.default` — `#C73E3E`
6. `neutral.500` — `#73808D`

This order is not a license to use six colors in every chart.

Use the fewest colors required to communicate the comparison.

### Data Rules

- Prefer one highlighted series and neutral comparison series.
- Use semantic colors only when the data carries that meaning.
- Do not automatically color positive numbers green and negative numbers red.
- Do not assign new colors to every category when labels, grouping, position, or line style can clarify the data.
- Limit standard categorical charts to six color families.
- Directly label series where possible.
- Use line style, marker shape, pattern, annotation, or ordering in addition to color.
- Preserve the same category-to-color mapping across related charts.
- Sequential data should use lightness progression within one family.
- Diverging data requires a defined neutral midpoint and explicit meaning for both directions.
- Heatmaps and continuous scales require separate validation and should not be improvised from the corporate palette.

---

## Accessibility

LINKGENT targets WCAG 2.2 Level AA as the minimum accessibility baseline for digital interfaces and applies the same principles to presentations and documents where practical.

### Accessibility Requirements

- Normal text must have a contrast ratio of at least `4.5:1`.
- Large text must have a contrast ratio of at least `3:1`.
- Essential icons, focus indicators, form boundaries, and meaningful non-text graphics must have at least `3:1` contrast against adjacent colors.
- Body text and essential information should aim for `7:1` when practical.
- Color must not be the only means of communicating meaning.
- Status must also use text, iconography, position, pattern, or another perceivable cue.
- Focus state must remain visible.
- Charts must remain understandable for people with common color-vision deficiencies.
- Contrast must be tested in the actual composition, not inferred from palette membership.

### Color Independence

Every essential color-coded message must remain understandable when:

- Viewed in grayscale
- Printed on a low-quality printer
- Seen with reduced saturation
- Viewed by a person with color-vision deficiency
- Projected in a bright room
- Displayed on an uncalibrated screen

### Accessibility and Brand Expression

When accessibility and visual preference conflict, accessibility takes precedence.

Do not reduce contrast to appear more minimal or sophisticated.

---

## Contrast Rules

### Verified Core Pairings

| Foreground | Background | Contrast | Status |
|---|---|---:|---|
| `#0B1320` | `#FFFFFF` | `18.61:1` | Pass AAA |
| `#3B4A5A` | `#FFFFFF` | `9.08:1` | Pass AAA |
| `#566575` | `#FFFFFF` | `5.98:1` | Pass AA |
| `#173A63` | `#FFFFFF` | `11.53:1` | Pass AAA |
| `#FFFFFF` | `#173A63` | `11.53:1` | Pass AAA |
| `#FFFFFF` | `#0C2038` | `16.41:1` | Pass AAA |
| `#FFFFFF` | `#087899` | `5.05:1` | Pass AA |
| `#0B1320` | `#29B6E8` | `7.93:1` | Pass AAA |
| `#FFFFFF` | `#1F6B4F` | `6.41:1` | Pass AA |
| `#FFFFFF` | `#7A4B00` | `7.41:1` | Pass AAA |
| `#FFFFFF` | `#9B2C2C` | `7.53:1` | Pass AAA |
| `#FFFFFF` | `#29B6E8` | `2.35:1` | Fail for text |

### Required Pairing Decisions

- Use white text on `primary.700`, `primary.800`, or `primary.900`.
- Use `neutral.1000` text on `accent.500`.
- Use `accent.700` or darker for links and text on light backgrounds.
- Use semantic `strong` colors for solid status surfaces that contain white text.
- Use semantic `strong` text on semantic `subtle` surfaces.
- Do not use `neutral.500` or lighter for essential body text on white without a verified exception.

### Contrast Testing

Contrast must be recalculated when:

- Opacity is applied
- A gradient is used
- Text overlaps photography or illustration
- A color is converted for print
- A theme changes
- A component changes state
- Anti-aliasing or projection conditions materially reduce legibility

Palette approval does not replace composition testing.

---

## Print Rule

The canonical corporate values are currently defined in sRGB because the approved colors were established as HEX values.

Print output must be produced through a controlled color-management process.

### Provisional Process CMYK References

| Color | sRGB | Provisional CMYK |
|---|---:|---:|
| Primary | `#173A63` | `C77 M41 Y0 K61` |
| Accent | `#29B6E8` | `C82 M22 Y0 K9` |

These CMYK values are conversion references, not universal print specifications.

Final values depend on:

- Printing process
- Paper stock
- Coated or uncoated profile
- Press condition
- Ink limit
- Output intent
- Printer calibration

### Print Requirements

- Use an appropriate ICC profile supplied by the printer or production partner.
- Confirm critical corporate colors with a contract proof or physical proof when color accuracy matters.
- Preserve the semantic distinction between Primary, Accent, Neutral, and status colors after conversion.
- Do not alter the system-wide digital palette to compensate for one printer or paper stock.
- Store print-specific conversions as implementation mappings, not as replacements for the canonical sRGB values.
- Use `K100` for small neutral black text and fine lines unless the production specification requires otherwise.
- Do not use four-color rich black for small body text.
- Avoid small reversed white text on Accent.
- Check thin borders and pale background fills for disappearance in print.
- Validate grayscale output when documents may be printed without color.

### Spot Color

No official spot-color specification is defined in this version.

A spot-color mapping may be approved after the logo and production requirements are finalized.

---

## Digital Rule

### Canonical Digital Values

- sRGB HEX values in this document are the current canonical digital values.
- RGB values should be generated directly from the canonical HEX values.
- Do not modify permanent colors through arbitrary opacity, blend mode, or filter effects.
- Use an approved scale step instead of creating an untracked lighter or darker variation.

### Digital Usage

- Use semantic roles rather than hardcoded HEX values in components and templates.
- Preserve color meaning across tools even when token syntax differs.
- Test colors on common display conditions and in light, bright, and low-quality environments.
- Use color profiles correctly when exporting raster assets.
- Avoid unnecessary gradients, glow, neon effects, and uncontrolled transparency.
- Do not increase saturation to make AI-generated output appear more futuristic.
- Future-ready expression should come from clarity, precision, and intelligent structure.

### Theme Handling

This version defines a light-first system.

A complete dark theme is not yet approved.

Until a dark theme is defined:

- Use `background.inverse` only as a controlled section or component context.
- Do not auto-invert colors.
- Do not assume light palette values map directly to dark surfaces.
- Validate every inverse foreground, border, focus, and semantic state independently.

---

## Presentation Rule

Presentation color must improve narrative structure and comprehension.

### Presentation Hierarchy

- Neutral backgrounds should dominate the slide system.
- Primary should define section structure, key framing, and trusted hierarchy.
- Accent should identify the main point, action, or focal data series.
- Semantic colors should appear only when their meaning is present.
- A slide should normally have one dominant focal color decision.

### Presentation Application

Use Primary for:

- Section dividers
- Main structural headings
- Key frames
- High-level process anchors
- Table headers when strong hierarchy is required

Use Accent for:

- A single key number
- A selected step
- A primary action or recommendation
- A highlighted data series
- A critical connection in a diagram

Use neutrals for:

- Body text
- Supporting labels
- Comparison series
- Tables
- Card surfaces
- Secondary diagrams

### Presentation Constraints

- Accent should generally remain below approximately `10%` of the visible slide area.
- The percentage is guidance, not a mechanical target. Meaning takes precedence.
- Do not use a different color for every slide section.
- Do not fill every card with a colored background.
- Do not use pale text that may disappear under projection.
- Verify contrast under presentation-room conditions.
- Use direct labels and annotations in charts.
- Preserve color meaning across the entire deck.
- Tables should use hierarchy, spacing, and borders before multiple fills.

Detailed component and template mappings belong to `10_Presentation_System/`.

---

## Web Rule

Web color must support understanding, interaction, state, and accessibility.

### Web Application

- Use Primary for structural navigation, trusted hierarchy, and default primary actions.
- Use Accent for focal actions, selected emphasis, and focus cues.
- Use `accent.700` or darker for links on light surfaces.
- Use semantic status colors only for their defined meanings.
- Use neutral surfaces and borders to create most component structure.
- Use role-based tokens instead of raw HEX values in component code.

### Interaction States

Every interactive component must define:

- Default
- Hover
- Pressed
- Focus
- Selected, when applicable
- Disabled, when applicable
- Error, when applicable

State changes must not rely on color alone.

Use at least one additional cue such as:

- Border change
- Underline
- Icon
- Shape
- Weight
- Label
- Position

### Web Constraints

- Do not use `accent.500` with white text.
- Do not remove focus rings.
- Do not make disabled content look interactive.
- Do not use low-contrast placeholder text as a substitute for labels.
- Do not hardcode component colors when a semantic role exists.
- Do not assign brand color to every interactive element.
- Do not introduce a new hue for a local component without system review.

Detailed component behavior belongs to `11_Web_System.md`.

---

## AI Generation Rule

AI must treat this document as a decision system, not as a palette suggestion.

### Required AI Decision Sequence

Before generating a presentation, Web page, UI, document, diagram, or image, AI must:

1. Identify the communication purpose.
2. Identify information hierarchy.
3. Classify each color-bearing element by role.
4. Select the corresponding semantic role.
5. Map the role to an approved value.
6. Validate foreground and background contrast.
7. Verify that color is not the only carrier of meaning.
8. Check consistency across the complete artifact.

### AI Role Selection

AI should use the following default priority:

```text
Neutral for content and surfaces
Primary for structure and hierarchy
Accent for one deliberate focal purpose
Semantic color for explicit state or meaning
```

### AI Generation Requirements

AI must:

- Use approved palette values only unless explicitly instructed to create a proposed extension.
- Distinguish corporate, semantic, neutral, and functional roles.
- Preserve the same meaning for the same role across an artifact.
- Use semantic role names in its internal or generated specifications where possible.
- Prefer neutral comparison elements and one highlighted element in charts.
- Use text, labels, icons, shapes, or patterns in addition to semantic color.
- Use `#0B1320` rather than white on `#29B6E8`.
- Use `#087899` or darker for accent-colored text on light surfaces.
- Validate contrast after applying opacity, overlays, gradients, or imagery.
- Report exceptions when a requested composition cannot meet the rules.

### AI Generation Prohibitions

AI must not:

- Invent additional brand colors for variety.
- Derive the Color System from a generated or unfinished logo.
- Treat Accent as a general-purpose decoration color.
- Use neon, rainbow, or high-saturation palettes to represent AI or the future.
- Apply semantic red, yellow, or green without the corresponding meaning.
- Use color alone to distinguish chart categories or status.
- Create untracked tints by lowering opacity over arbitrary backgrounds.
- Recolor people, skin, natural materials, or documentary imagery merely to force brand colors.
- Generate low-contrast text because it appears minimal.

### AI-Generated Presentations

AI should:

- Begin with neutral surfaces.
- Use Primary to make narrative structure visible.
- Use Accent for the principal takeaway or action.
- Limit categorical chart colors.
- Keep the same series color across slides.
- Avoid decorative color bands without informational function.

### AI-Generated Web and UI

AI should:

- Define semantic color roles before component styling.
- Generate all relevant interaction states.
- Use role-based variables or tokens rather than repeating HEX values.
- Validate text, icon, focus, and control-boundary contrast.
- Avoid using the corporate Accent as the default for every button.

### AI-Generated Images and Visuals

AI should:

- Use corporate color as an environmental cue, lighting accent, object detail, or compositional anchor when appropriate.
- Keep natural subjects credible and human-centered.
- Avoid forcing the entire image into monochromatic corporate blue.
- Preserve usable negative space and contrast when text will be added later.
- Treat brand color presence as controlled direction, not a mandatory filter.

### AI Output Traceability

When practical, AI-generated design specifications should include:

- Color role used
- HEX value used
- Foreground/background pairing
- Contrast result for essential text and controls
- Any exception or proposed extension

---

## Do

- Use color to clarify hierarchy, grouping, state, and action.
- Begin with neutral surfaces and text.
- Use Primary for structure and trust.
- Use Accent sparingly for attention and action.
- Use semantic colors only for their defined meanings.
- Select semantic roles before raw values.
- Use approved scale steps instead of arbitrary tints.
- Maintain consistent meaning across media.
- Test actual foreground/background combinations.
- Pair color with text, iconography, shape, pattern, or position.
- Preserve accessible contrast under realistic viewing conditions.
- Keep logo-specific decisions separate from the Color System.
- Document proposed extensions before implementation.

---

## Don't

- Do not use color as decoration without meaning.
- Do not use Accent everywhere.
- Do not place white text on `#29B6E8`.
- Do not use pale gray for essential body text.
- Do not use red, yellow, or green without semantic intent.
- Do not create a new hue for each category, section, card, or slide.
- Do not derive the system from an unfinished logo.
- Do not hardcode HEX values where semantic roles should be used.
- Do not create permanent variants through arbitrary opacity.
- Do not rely on color alone for status or comparison.
- Do not assume a palette value is accessible in every composition.
- Do not auto-invert the light system to create dark mode.
- Do not use gradients, glow, or neon effects to signal innovation.
- Do not sacrifice understanding for visual impact.

---

## Future Improvements

The following items are planned extensions. They are not approved rules until added to the relevant canonical document.

### 1. Logo Color Mapping

After the logo is finalized:

- Define logo-specific color combinations in `02_Visual_Identity.md`.
- Confirm whether Primary and Accent are used in the logo.
- Preserve the independence of system semantics from logo artwork.

### 2. Design Token Implementation

In `05_Design_Tokens.md`:

- Define formal global and semantic token names.
- Define Figma variable collections and modes.
- Define CSS, JSON, PowerPoint, Canva, and document mappings.
- Define deprecation and migration rules.

### 3. Dark Theme

Create a complete dark-theme model with independently validated:

- Background layers
- Text hierarchy
- Borders
- Focus states
- Interaction states
- Semantic states
- Data visualization mappings

Do not create dark mode through automatic inversion.

### 4. Perceptual Color Authoring

Evaluate a perceptually uniform authoring model such as OKLCH for future palette maintenance while preserving stable sRGB fallbacks and existing semantic meaning.

### 5. Wide-Gamut Support

Evaluate Display-P3 or other wide-gamut values for supported media without creating inconsistent brand appearance on standard sRGB devices.

### 6. Print Production Standards

After real production testing:

- Approve coated and uncoated CMYK mappings.
- Define spot-color equivalents if needed.
- Record proofing standards and acceptable tolerances.
- Validate office-printer and grayscale fallbacks.

### 7. Extended Data Visualization

Define dedicated systems for:

- Sequential scales
- Diverging scales
- Heatmaps
- Dense categorical data
- Accessible chart patterns
- Dark-background charts

### 8. Automated Validation

Implement automated checks for:

- Contrast
- Unapproved HEX values
- Semantic misuse
- Token drift
- Theme coverage
- AI-generated artifact compliance

### 9. Accessibility Validation

Continue testing with:

- Color-vision-deficiency simulation
- Real projection environments
- Office printers
- Low-quality displays
- User evaluation
- Future accessibility standards

### 10. System Review

Review this Color System when any of the following changes materially:

- Brand strategy
- Corporate identity
- Product portfolio
- Accessibility requirements
- Core media environment
- Printing requirements
- Theme strategy
- Data visualization needs

The stable default is extension, not replacement.

---

## Reference Basis

This Color System is independently designed for LINKGENT and informed by established practices found in systems such as:

- Adobe Spectrum
- Google Material Design
- IBM Carbon Design System
- Microsoft Fluent
- Atlassian Design System
- WCAG 2.2

External systems are references, not authorities over LINKGENT Brand Core.

When external practices conflict with LINKGENT's principles, the following precedence applies:

1. `CONSTITUTION.md`
2. `01_Brand_Core.md`
3. This Color System
4. Applied Systems
5. External references

The defining LINKGENT principle remains:

> **Structure creates understanding.**
