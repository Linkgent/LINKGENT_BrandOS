# 04_Typography

> Version: 1.1.0  
> Status: Draft — Git Ready  
> Owner: LINKGENT Brand OS  
> Last Updated: 2026-07-24

---

# Purpose

The LINKGENT Typography System defines a shared typographic language for presenting structured information across every LINKGENT touchpoint.

This system is designed for consistent use across:

- Presentation
- Web
- Word
- Figma
- Canva
- AI-generated documents
- Internal documentation
- Future digital products

Typography at LINKGENT is not treated as visual styling alone.

It is part of the information architecture.

The system exists to make the meaning, importance, sequence, and relationship of information visible before the reader examines the content in detail.

This specification ensures that typography remains:

- Structured
- Readable
- Accessible
- Consistent
- Scalable
- Cross-platform
- AI-readable

Rather than optimizing typography for a single application, this document establishes a platform-independent Typography System that can be referenced by people, design tools, code, and AI.

---

# Philosophy

## Typography Is Information Architecture

Typography is part of information architecture.

It should not merely display content; it should reveal structure.

Readers should understand the organization of information before reading the content itself.

Typography should clarify:

- What is most important
- What belongs together
- What comes next
- What is supporting information
- What action or interpretation is expected

Typography should never be used as a substitute for clear thinking or proper information organization.

---

## Clarity First

Typography exists to communicate.

Visual expression must never reduce readability, comprehension, or usability.

Decorative decisions should only be introduced when they support meaning.

---

## Information Hierarchy

The structure of information should be visible before individual sentences are read.

Size, weight, spacing, position, and alignment should guide the reader naturally through the content.

Hierarchy should communicate meaning rather than visual preference.

---

## Minimal Expression

Use the smallest number of typographic styles necessary to communicate structure clearly.

Fewer styles create:

- Stronger consistency
- Faster comprehension
- Easier maintenance
- Better cross-platform reproduction
- More reliable AI generation

Variation should be intentional, not decorative.

---

## Human and AI Readability

Typography definitions must be understandable by both humans and AI systems.

Style names should represent semantic roles rather than visual appearance.

Preferred:

```text
Typography/Heading/H1
```

Avoid:

```text
Large Blue Bold Text
```

Semantic naming allows the same typographic intent to be implemented consistently across different applications and output formats.

---

## Cross-Platform Consistency

The Typography System should remain recognizable across:

- Windows
- macOS
- Browsers
- Microsoft Office
- Figma
- Canva
- AI-generated outputs
- Future LINKGENT applications

Exact rendering may vary by platform, but hierarchy, meaning, and visual rhythm must remain consistent.

No platform should create an independent typography system unless a documented technical limitation requires it.

---

# Font

## Japanese Primary Font

```text
BIZ UDPゴシック
```

BIZ UDPゴシック is the primary Japanese typeface for LINKGENT.

It is selected because it provides:

- High legibility
- Universal Design principles
- Strong readability at small sizes
- Stable use in Microsoft environments
- Clear distinction between similar characters
- Appropriate neutrality for business communication

### Recommended Weights

| Semantic Role | Weight |
|---|---:|
| Display | Bold |
| Heading | Bold |
| Body | Regular |
| Caption | Regular |

Use Bold only when hierarchy or emphasis requires it.

Avoid using multiple weights without a defined semantic purpose.

---

## Latin and Numeric Primary Font

```text
Inter
```

Inter is the primary typeface for English text, Latin characters, and numbers when platform support allows.

It is selected because it is:

- Modern
- Neutral
- Highly readable
- Optimized for digital interfaces
- Suitable for numerical information
- Widely supported in design and web environments

### Recommended Weights

| Semantic Role | Weight |
|---|---:|
| Display | SemiBold |
| Heading | SemiBold |
| Body | Regular |
| Caption | Regular |

---

## Mixed-Language Rule

When Japanese and English appear together:

```text
Japanese: BIZ UDPゴシック
English and numbers: Inter
```

Use language-specific font assignment only when the application supports it reliably.

Do not manually switch fonts character by character when doing so creates unstable layout, inconsistent spacing, or difficult maintenance.

In environments where mixed-font control is limited, prioritize consistency and readability over strict font separation.

---

## Fallback Fonts

### Japanese

```css
"BIZ UDPGothic",
"Yu Gothic",
"YuGothic",
"Meiryo",
sans-serif
```

### Latin and Numeric

```css
"Inter",
"Segoe UI",
"Helvetica Neue",
"Arial",
sans-serif
```

Fallback fonts should preserve the intended hierarchy and approximate readability of the primary typefaces.

When a primary font is unavailable, do not compensate by changing arbitrary font sizes.

---

# Hierarchy

Typography hierarchy is determined by meaning, not by visual preference.

Never increase font size simply to attract attention.

Hierarchy should communicate:

- Information importance
- Content relationships
- Reading order
- Section boundaries
- Supporting context

Typography must not be used as decoration without semantic meaning.

---

## Core Hierarchy

The LINKGENT Typography System uses the following primary levels.

| Token | PowerPoint Size | Default Weight | Semantic Role |
|---|---:|---:|---|
| Display | 36 pt | Bold / SemiBold | Cover title, hero statement, major message |
| H1 | 28 pt | Bold / SemiBold | Primary section heading |
| H2 | 20 pt | Bold / SemiBold | Secondary section heading |
| Body Large | 18 pt | Regular | Lead text, key explanation, introductory statement |
| Body | 16 pt | Regular | Standard content |
| Caption | 11 pt | Regular | Notes, metadata, sources, labels |

These values are the current PowerPoint implementation baseline.

Equivalent values for other platforms should preserve the same semantic hierarchy rather than reproduce point sizes mechanically.

---

## Hierarchy Order

The standard hierarchy is:

```text
Display
↓
H1
↓
H2
↓
Body Large
↓
Body
↓
Caption
```

Hierarchy levels may be omitted when they are unnecessary.

Do not introduce an intermediate style merely to fill a visual gap.

Avoid skipping semantic levels when doing so makes the information structure unclear.

---

## Display Usage

`Display` replaces the previous `H0` naming.

Display is intended for:

- Cover titles
- Hero statements
- Opening messages
- Major presentation statements
- High-level campaign messages

Display is not a document heading level.

It should be used selectively and should not appear repeatedly within dense content.

---

# Scale

The LINKGENT typography scale is intentionally optical rather than mathematical.

The chosen sizes prioritize:

- Visual balance
- Readability
- Information density
- Platform compatibility
- Japanese character legibility
- Presentation viewing distance

The scale does not depend on a fixed mathematical ratio.

Numeric ratios are implementation details and should not override visual judgment or semantic meaning.

When adapting typography to another platform, preserve the perceived hierarchy rather than calculating every size from a single base value.

---

## Line Height

Recommended line heights:

| Style | Recommended Line Height |
|---|---:|
| Display | 115–125% |
| H1 | 120–130% |
| H2 | 125–140% |
| Body Large | 145–160% |
| Body | 150–165% |
| Caption | 140–155% |

Japanese body text generally requires more line height than English text.

Line height should support reading flow without visually separating lines into unrelated blocks.

---

## Letter Spacing

Default letter spacing:

```text
0
```

Minor positive tracking may be used for large Display text when it improves optical balance.

Recommended maximum:

```text
+1%
```

Avoid negative tracking for Japanese text.

Do not use letter spacing to force text into a fixed layout.

---

## Vertical Rhythm

Typography must work together with spacing.

Headings, paragraphs, captions, and supporting elements should follow a consistent vertical rhythm.

Spacing should reflect semantic relationships:

- Closely related items should appear closer together
- New sections should have clearly larger separation
- Captions should remain visually attached to the content they describe
- Headings should not appear detached from their following content

Typography and spacing must be designed as one system.

---

# Naming Convention

Typography styles must use semantic, predictable, and cross-platform names.

The recommended hierarchy is:

```text
Typography/
├── Display
├── Heading/
│   ├── H1
│   └── H2
├── Body/
│   ├── Large
│   └── Default
└── Caption
```

Recommended flattened names for tools that do not support nested naming:

```text
Typography/Display
Typography/Heading/H1
Typography/Heading/H2
Typography/Body/Large
Typography/Body/Default
Typography/Caption
```

---

## Naming Principles

Typography names should describe meaning, not appearance.

Preferred:

```text
Typography/Body/Large
```

Avoid:

```text
18px Regular
```

Preferred:

```text
Typography/Heading/H1
```

Avoid:

```text
Big Bold Title
```

Numeric values may be included in implementation metadata, but they should not be the primary identity of a typography token.

---

## Design Token Alignment

Typography naming should align with Design Tokens.

Example conceptual token structure:

```json
{
  "typography": {
    "display": {},
    "heading": {
      "h1": {},
      "h2": {}
    },
    "body": {
      "large": {},
      "default": {}
    },
    "caption": {}
  }
}
```

Typography tokens represent semantic meaning.

Font family, size, weight, line height, and letter spacing are implementation properties of those tokens.

---

# Usage

## Presentation Rule

Presentations must use typography to support rapid visual scanning.

Core rules:

- Use a maximum of three hierarchy levels per slide
- Communicate one primary message per slide
- Avoid paragraphs exceeding five lines
- Use typography to make the reading order immediately visible
- Keep supporting information visually subordinate
- Avoid filling empty space by enlarging text without semantic reason
- Use Display only for major statements
- Use Caption only for genuinely secondary information

Typography should help viewers understand the slide structure within a few seconds.

A presentation should not require the audience to read every word before understanding its message.

---

## PowerPoint

PowerPoint should use the official typography hierarchy without arbitrary font sizes.

Recommended mapping:

| Token | Size |
|---|---:|
| Display | 36 pt |
| H1 | 28 pt |
| H2 | 20 pt |
| Body Large | 18 pt |
| Body | 16 pt |
| Caption | 11 pt |

Rules:

- Use the Slide Master whenever possible
- Avoid local text overrides
- Use one Typography System per presentation
- Maintain a maximum of three visible hierarchy levels per slide
- Do not use Caption as a replacement for Body
- Do not reduce Body below the defined minimum simply to fit content
- Rewrite or restructure overflowing content instead

---

## Web

Use semantic HTML and map visual styles to typography tokens.

Recommended mapping:

| Typography Token | Semantic HTML |
|---|---|
| Display | Hero heading or presentation element |
| H1 | `h1` |
| H2 | `h2` |
| Body Large | Lead paragraph or emphasized introduction |
| Body | `p`, `li`, form text |
| Caption | `small`, metadata, supporting label |

Semantic HTML must not be selected solely to reproduce a visual size.

Heading tags should reflect the actual document structure.

Visual typography tokens and HTML semantics should support each other without becoming interchangeable.

---

## Word

Use Word’s built-in style system instead of manual formatting.

Recommended mapping:

| LINKGENT Token | Word Style |
|---|---|
| Display | Title |
| H1 | Heading 1 |
| H2 | Heading 2 |
| Body Large | Subtitle or custom Lead style |
| Body | Normal |
| Caption | Caption |

Rules:

- Modify styles centrally
- Avoid manual formatting of individual paragraphs
- Preserve heading structure for navigation and accessibility
- Use real lists rather than manually typed symbols
- Do not use font size alone to indicate document structure

---

## Figma

Typography must be implemented as shared Text Styles or Variables-supported tokens.

Recommended names:

```text
Typography/Display
Typography/Heading/H1
Typography/Heading/H2
Typography/Body/Large
Typography/Body/Default
Typography/Caption
```

Rules:

- Use shared styles rather than local formatting
- Avoid duplicate styles with slightly different values
- Do not name styles by screen or component unless the semantic role differs
- Connect typography styles to Design Tokens where technically possible
- Document platform-specific exceptions

---

## Canva

Create Canva Brand Kit text styles that correspond to the official hierarchy.

Rules:

- Use the approved font hierarchy
- Avoid arbitrary font sizes
- Avoid creating a new style for each design
- Use Display selectively
- Preserve hierarchy when templates are duplicated
- Check font substitution before export

When Inter or BIZ UDPゴシック is unavailable, use the approved fallback font and retain the semantic style name.

---

## AI Generation

AI should always reference typography tokens before considering numeric values.

Tokens represent semantic meaning, while numeric values are implementation details.

Preferred prompt instruction:

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

Numeric values may be supplied as implementation context after the semantic token has been defined.

Example:

```text
Apply Typography/Heading/H1.
In PowerPoint, this token is implemented as 28 pt Bold.
```

AI-generated outputs should:

- Use only approved typography tokens
- Preserve semantic hierarchy
- Avoid inventing new font sizes
- Avoid using visual emphasis without structural meaning
- Follow platform-specific implementations
- Maintain accessibility requirements
- Preserve vertical rhythm

---

# Accessibility

Typography must remain accessible across all LINKGENT outputs.

Accessibility is a system requirement, not an optional adjustment.

---

## Minimum Size

Recommended minimum sizes:

| Content Type | Minimum |
|---|---:|
| Web Body | 16 px |
| Presentation Body | 16 pt |
| Presentation Caption | 11 pt |
| Long-form document Body | 10.5–11 pt, depending on format |

Do not reduce text below the defined minimum to fit excessive content.

Edit, shorten, split, or restructure the content instead.

---

## Contrast

Text and background combinations should meet WCAG AA contrast requirements.

As a general target:

- Normal text: minimum 4.5:1
- Large text: minimum 3:1

Typography tokens should reference approved semantic colors from the LINKGENT Color System.

Do not define text colors independently within typography styles unless required by the platform.

---

## Alignment

Prefer left alignment for:

- Paragraphs
- Lists
- Long explanations
- Instructions
- Data descriptions

Centered alignment may be used for:

- Short titles
- Cover messages
- Brief statements
- Intentional presentation moments

Avoid long centered paragraphs.

Centered text reduces scanning efficiency and creates inconsistent reading anchors.

---

## Capitalization

Avoid long passages written in ALL CAPS.

ALL CAPS may be used sparingly for:

- Short labels
- Small interface categories
- Compact metadata

Do not use capitalization as the only indication of hierarchy.

---

## Color Dependency

Do not use color alone to communicate:

- Importance
- Status
- Error
- Selection
- Category
- Hierarchy

Combine color with at least one additional signal, such as:

- Position
- Weight
- Label
- Icon
- Shape
- Pattern
- Text description

---

## Emphasis

Use emphasis sparingly.

Preferred emphasis methods:

1. Structural placement
2. Heading hierarchy
3. Font weight
4. Spacing
5. Color

Avoid excessive bolding, underlining, or mixed emphasis styles.

Underlining should primarily indicate links in digital environments.

---

## Readability

Avoid:

- Long centered paragraphs
- Excessively long line lengths
- Dense blocks without spacing
- Arbitrary font-size reduction
- Low-contrast text
- Decorative outlines
- Text over complex imagery
- Narrow text columns with forced line breaks

Typography should support scanning, comprehension, and sustained reading.

---

# Do

- Use predefined typography tokens
- Determine hierarchy by meaning
- Keep typography consistent across platforms
- Use semantic naming
- Maintain consistent vertical rhythm
- Preserve generous line spacing
- Prefer left alignment for long-form text
- Use shared styles instead of local formatting
- Keep font usage minimal
- Follow minimum-size requirements
- Use typography together with spacing
- Map typography to Design Tokens
- Reference semantic tokens in AI prompts
- Restructure content when it does not fit

---

# Don't

- Use typography to compensate for poor information architecture
- Increase font size simply to attract attention
- Create arbitrary font sizes
- Mix multiple Japanese fonts without purpose
- Mix serif and sans-serif typefaces without a defined system
- Use more hierarchy levels than the content requires
- Center-align long paragraphs
- Stretch, compress, or distort text
- Override shared text styles locally
- Use Caption for primary content
- Use color alone to communicate meaning
- Reduce text below the minimum size to fit content
- Add unnecessary shadows, outlines, gradients, or effects
- Name styles according to visual appearance
- Use typography as decoration without semantic purpose

---

# Future Improvements

Future versions of the LINKGENT Typography System may include:

- Responsive typography definitions
- Cross-platform Token Export
- CSS and JSON token generation
- PowerPoint Theme Automation
- Word Style Template Automation
- Figma Variables synchronization
- Canva Brand Kit synchronization
- Variable font support
- Multilingual typography rules
- Japanese and English optical adjustment rules
- Dark-mode typography validation
- Automated accessibility checking
- AI-readable typography metadata
- Automated typography linting
- Platform-specific token transformation
- Integration with presentation-generation systems
- Integration with document-generation systems

The long-term objective is to define typography once and distribute it consistently across every platform.

---

## Design Principles Summary

LINKGENT typography should always be:

- Structured
- Intelligent
- Reliable
- Minimal
- Accessible
- Cross-platform
- AI-readable

Typography should reveal structure before attracting attention.
