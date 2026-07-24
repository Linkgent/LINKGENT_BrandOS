# 04_Typography

> Version: 1.2.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

The LINKGENT Typography System defines a shared typographic language for presenting structured information across every LINKGENT touchpoint.

It applies to:

- Presentations
- Web
- Word and Google Docs
- Figma and Figma Slides
- Canva
- AI-generated documents
- Internal documentation
- Future digital products

Typography is not visual styling alone. It is part of information architecture.

The system exists to make the meaning, importance, sequence, and relationship of information visible before the reader examines the content in detail.

---

## Inheritance and Ownership

This file inherits:

1. [`../CONSTITUTION.md`](../CONSTITUTION.md)
2. [`01_Brand_Core.md`](./01_Brand_Core.md)
3. [`03_Color_System.md`](./03_Color_System.md)

This file is the canonical owner of:

- Font family selection
- Typography hierarchy
- Typography scale
- Minimum typography sizes
- Typography naming
- Cross-platform typography mapping
- Typography accessibility rules

[`05_Design_Tokens.md`](./05_Design_Tokens.md) operationalizes these roles as tokens. Applied Systems define context-specific use without redefining the canonical values.

---

## Principles

### Typography Is Information Architecture

Typography must reveal:

- What is most important
- What belongs together
- What comes next
- What is supporting information
- What action or interpretation is expected

Typography must not compensate for weak information organization.

### Clarity First

Visual expression must not reduce readability, comprehension, or usability.

Decorative decisions are permitted only when they support meaning.

### Minimal Expression

Use the smallest number of typographic styles necessary to communicate structure clearly.

Fewer styles create:

- Stronger consistency
- Faster comprehension
- Easier maintenance
- Better cross-platform reproduction
- More reliable AI generation

### Semantics Before Appearance

Preferred:

```text
Typography/Heading/H1
```

Avoid:

```text
Large Blue Bold Text
```

### Cross-platform Consistency

Exact rendering may vary by platform. Hierarchy, meaning, readability, and rhythm must remain consistent.

No platform should create an independent typography system unless a documented technical limitation requires an applied mapping.

---

## Canonical Fonts

### Japanese Primary Font

```text
BIZ UDPゴシック
```

Use BIZ UDPゴシック as the primary Japanese typeface because it provides high legibility, Universal Design characteristics, clear character distinction, and stable use in Microsoft environments.

Recommended weights:

| Semantic Role | Weight |
|---|---:|
| Display | Bold |
| Heading | Bold |
| Body | Regular |
| Caption | Regular |

Use Bold only when hierarchy or emphasis requires it.

### Latin and Numeric Primary Font

```text
Inter
```

Use Inter for English text, Latin characters, and numbers when platform support allows.

Recommended weights:

| Semantic Role | Weight |
|---|---:|
| Display | SemiBold |
| Heading | SemiBold |
| Body | Regular |
| Caption | Regular |

### Mixed-language Rule

When reliable language-specific assignment is supported:

```text
Japanese: BIZ UDPゴシック
English and numbers: Inter
```

Do not switch fonts character by character when doing so creates unstable layout or maintenance.

In constrained environments, prioritize consistent hierarchy and readability over strict language separation.

### Fallbacks

Japanese:

```css
"BIZ UDPGothic",
"Yu Gothic",
"YuGothic",
"Meiryo",
sans-serif
```

Latin and numeric:

```css
"Inter",
"Segoe UI",
"Helvetica Neue",
"Arial",
sans-serif
```

Fallbacks must preserve intended hierarchy and approximate readability. Do not compensate for substitution by inventing arbitrary sizes.

---

## Core Hierarchy

Typography hierarchy is determined by meaning, not visual preference.

| Token | PowerPoint Baseline | Default Weight | Semantic Role |
|---|---:|---:|---|
| `Typography/Display` | 36 pt | Bold / SemiBold | Cover title, hero statement, major message |
| `Typography/Heading/H1` | 28 pt | Bold / SemiBold | Primary section heading |
| `Typography/Heading/H2` | 20 pt | Bold / SemiBold | Secondary section heading |
| `Typography/Body/Large` | 18 pt | Regular | Lead text, key explanation, introduction |
| `Typography/Body/Default` | 16 pt | Regular | Standard content |
| `Typography/Caption` | 11 pt | Regular | Notes, metadata, sources, labels |

These values are the current PowerPoint implementation baseline. Other platforms must preserve equivalent perceived hierarchy rather than reproduce point sizes mechanically.

Hierarchy order:

```text
Display
  ↓
Heading/H1
  ↓
Heading/H2
  ↓
Body/Large
  ↓
Body/Default
  ↓
Caption
```

Rules:

- Omit unnecessary levels.
- Do not create intermediate styles merely to fill a visual gap.
- Do not skip levels when doing so obscures structure.
- Never increase size simply to attract attention.
- Use no more hierarchy levels than the content requires.

### Display Usage

Display is intended for:

- Cover titles
- Hero statements
- Opening messages
- Major presentation statements
- High-level campaign messages

Display is not a document heading level and should not be repeated through dense content.

---

## Rule IDs

The following IDs are canonical cross-file references.

### TYPE-PRESENTATION-MIN-BODY

```yaml
value: 16 pt
scope: standard presentation body text
```

Do not reduce Body below this value to fit content. Rewrite, restructure, or split the content.

### TYPE-PRESENTATION-MIN-CAPTION

```yaml
value: 11 pt
scope: presentation sources, labels, metadata, and genuinely secondary notes
```

Caption must not replace Body for primary information.

### TYPE-PRESENTATION-HIERARCHY

```yaml
maximum_visible_levels_per_slide: 3
primary_rule: hierarchy follows semantic meaning
```

A slide should communicate one primary message and reveal reading order within a few seconds.

---

## Scale and Rhythm

The typography scale is intentionally optical rather than mathematically generated.

It prioritizes:

- Readability
- Japanese character legibility
- Information density
- Viewing distance
- Cross-platform compatibility
- Visual balance

### Line Height

| Style | Recommended Line Height |
|---|---:|
| Display | 115–125% |
| Heading/H1 | 120–130% |
| Heading/H2 | 125–140% |
| Body/Large | 145–160% |
| Body/Default | 150–165% |
| Caption | 140–155% |

Japanese body text generally requires more line height than English text.

Line height should support flow without visually separating related lines.

### Letter Spacing

Default:

```text
0
```

Minor positive tracking may be used for large Display text when it improves optical balance.

Recommended maximum:

```text
+1%
```

Avoid negative tracking for Japanese text. Do not use letter spacing to force content into a fixed layout.

### Vertical Rhythm

Spacing must reflect semantic relationships:

- Closely related items appear closer together.
- New sections receive clearly larger separation.
- Captions remain attached to the content they describe.
- Headings remain connected to their following content.

Typography and spacing must be designed as one system.

---

## Naming Convention

Canonical names:

```text
Typography/Display
Typography/Heading/H1
Typography/Heading/H2
Typography/Body/Large
Typography/Body/Default
Typography/Caption
```

Names must describe meaning, not appearance.

Preferred:

```text
Typography/Body/Large
```

Avoid:

```text
18px Regular
```

Numeric values may appear in implementation metadata but must not be the identity of the token.

---

## Design Token Alignment

Typography tokens are defined in this file and operationalized by [`05_Design_Tokens.md`](./05_Design_Tokens.md).

Each token maps:

```yaml
font_family:
font_size:
font_weight:
line_height:
letter_spacing:
semantic_role:
```

AI and implementation systems should reference the semantic token first, then resolve platform values.

---

## Presentation Application

Presentations must support rapid visual scanning.

Rules:

- Apply `TYPE-PRESENTATION-HIERARCHY`.
- Communicate one primary message per slide.
- Avoid paragraphs exceeding five lines where possible.
- Make reading order immediately visible.
- Keep supporting information subordinate.
- Use Display only for major statements.
- Use Caption only for genuinely secondary information.
- Do not enlarge text simply to fill space.
- Do not reduce Body or Caption below their canonical minimums.

PowerPoint implementation should use the Slide Master and avoid local text overrides.

---

## Web Application

Use semantic HTML and map visual styles to typography tokens.

| Typography Token | Typical Semantic HTML |
|---|---|
| Display | Hero heading or presentation element |
| Heading/H1 | `h1` |
| Heading/H2 | `h2` |
| Body/Large | Lead paragraph or emphasized introduction |
| Body/Default | `p`, `li`, form text |
| Caption | `small`, metadata, supporting label |

HTML semantics must reflect document structure rather than visual size alone.

---

## Word and Google Docs Application

Use the platform style system instead of manual formatting.

| LINKGENT Token | Typical Document Style |
|---|---|
| Display | Title |
| Heading/H1 | Heading 1 |
| Heading/H2 | Heading 2 |
| Body/Large | Subtitle or Lead |
| Body/Default | Normal |
| Caption | Caption |

Rules:

- Modify styles centrally.
- Preserve heading structure for navigation and accessibility.
- Use real lists.
- Do not indicate structure through font size alone.

---

## Figma Application

Use shared Text Styles or token-linked variables.

Rules:

- Avoid duplicate styles with slightly different values.
- Do not name styles by screen or component unless semantic meaning differs.
- Connect styles to Design Tokens where technically possible.
- Document platform-specific exceptions.

---

## Canva Application

Map Brand Kit text styles to the canonical hierarchy.

Rules:

- Avoid arbitrary sizes.
- Avoid creating a new style for each design.
- Preserve hierarchy when templates are duplicated.
- Check font substitution before export.
- Retain semantic style names when using approved fallback fonts.

---

## AI Application

AI must reference typography tokens before numeric values.

Preferred:

```text
Use Typography/Heading/H1 for the section title.
Use Typography/Body/Default for the explanation.
Use Typography/Caption for the source note.
```

Avoid:

```text
Use 28 pt bold text.
Use 16 pt regular text.
Use 11 pt gray text.
```

Numeric values may be supplied only as platform implementation context after the semantic role is defined.

AI must:

- Use approved typography tokens.
- Preserve semantic hierarchy.
- Avoid inventing sizes.
- Avoid emphasis without structural meaning.
- Follow platform mappings.
- Preserve accessibility and vertical rhythm.

---

## Accessibility

Accessibility is a system requirement.

### Minimum Size

| Content Type | Minimum |
|---|---:|
| Web Body | 16 px |
| Presentation Body | Apply `TYPE-PRESENTATION-MIN-BODY` |
| Presentation Caption | Apply `TYPE-PRESENTATION-MIN-CAPTION` |
| Long-form document Body | 10.5–11 pt depending on format |

Do not reduce text below the minimum to fit excessive content.

### Contrast

Text and backgrounds must comply with canonical Color System contrast rules.

Typography styles must reference semantic Color roles rather than define independent text colors.

### Alignment

Prefer left alignment for paragraphs, lists, instructions, and data descriptions.

Centered alignment is appropriate for short titles, covers, brief statements, and intentional presentation moments.

Avoid long centered paragraphs.

### Capitalization

Avoid long ALL CAPS passages. Use uppercase sparingly for short labels or compact metadata.

Capitalization must not be the only indication of hierarchy.

### Color Dependency

Do not use color alone to communicate importance, status, error, selection, category, or hierarchy.

Combine color with position, weight, labels, icons, shapes, patterns, or text description.

### Emphasis

Preferred order:

1. Structural placement
2. Heading hierarchy
3. Font weight
4. Spacing
5. Color

Avoid excessive bolding, underlining, or mixed emphasis styles. Underlining should primarily indicate links in digital contexts.

### Readability

Avoid:

- Long centered paragraphs
- Excessive line lengths
- Dense blocks without spacing
- Arbitrary size reduction
- Low-contrast text
- Decorative outlines
- Text over complex imagery
- Narrow columns with forced line breaks

---

## Do

- Use predefined typography tokens.
- Determine hierarchy by meaning.
- Use semantic naming.
- Maintain consistent vertical rhythm.
- Preserve appropriate line spacing.
- Prefer left alignment for long-form text.
- Use shared styles rather than local formatting.
- Keep font usage minimal.
- Follow minimum-size requirements.
- Reference semantic tokens in AI specifications.
- Restructure content when it does not fit.

---

## Don't

- Use typography to compensate for poor information architecture.
- Create arbitrary sizes.
- Mix multiple Japanese fonts without purpose.
- Mix serif and sans-serif typefaces without a defined system.
- Use more hierarchy levels than required.
- Center-align long paragraphs.
- Stretch, compress, or distort text.
- Override shared styles locally without a documented reason.
- Use Caption for primary content.
- Use color alone to communicate meaning.
- Reduce text below minimum sizes.
- Add unnecessary shadows, outlines, gradients, or effects.
- Name styles by visual appearance.
- Use typography as decoration without semantic purpose.

---

## Lifecycle and Validation

This document is `Release Candidate` because the conceptual system and platform mappings are defined, but implementation evidence is not complete.

Before `Active`, validate:

- PowerPoint Theme implementation
- Word style implementation
- Figma Text Style or Variable mapping
- Canva substitution behavior
- Web token mapping
- Japanese and English mixed-language rendering
- Accessibility minimums
- AI semantic interpretation
- Presentation Golden Deck typography behavior

---

## Future Improvements

- Responsive typography definitions
- Machine-readable token export
- PowerPoint Theme automation
- Word style template automation
- Figma Variables synchronization
- Canva Brand Kit synchronization
- Variable font support
- Multilingual optical adjustment
- Dark-mode validation
- Automated accessibility checking
- Typography linting
- Platform-specific token transformation

---

## Design Principle

LINKGENT typography should reveal structure before attracting attention.
