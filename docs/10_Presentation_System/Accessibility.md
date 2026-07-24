# Presentation Accessibility

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

Presentation Accessibility defines how LINKGENT applies accessible communication requirements to presentations across live delivery, self-guided use, export, conversion, and archive.

Accessibility is Brand Quality.

It is not an optional compliance layer added after visual design.

---

## Canonical Dependencies

Apply:

- `TYPE-PRESENTATION-MIN-BODY`
- `TYPE-PRESENTATION-MIN-CAPTION`
- `TYPE-PRESENTATION-HIERARCHY`
- `COLOR-CONTRAST-NORMAL`
- `COLOR-CONTRAST-LARGE`
- `COLOR-ACCENT-INVERSE-PROHIBITED`
- `COLOR-NOT-SOLE-CARRIER`

Canonical values remain in:

- [`../04_Typography.md`](../04_Typography.md)
- [`../03_Color_System.md`](../03_Color_System.md)

This file does not duplicate numeric values.

---

## Accessibility Dimensions

A presentation must be:

- Perceivable
- Understandable
- Navigable
- Operable where interactive
- Robust across formats
- Usable in the real delivery environment

---

## Reading Order

Reading order must be:

- Visually clear
- Technically ordered where the platform supports it
- Preserved in PDF or exported form where possible
- Understandable without animation
- Consistent with the semantic Slide Specification

Check:

- Title first when appropriate
- Primary message before supporting detail
- Labels attached to objects
- Sources after the content they support
- Decorative elements excluded from assistive reading order where supported

---

## Typography

Apply canonical typography rules.

Do not reduce type to fit content.

When content does not fit:

1. Edit
2. Restructure
3. Split
4. Move supporting detail
5. Change density or artifact role

Do not make Caption carry primary meaning.

Avoid:

- Long centered paragraphs
- Excessively narrow columns
- Low-contrast text
- Text over complex imagery
- Decorative outlines
- Compressed or stretched type

---

## Color and Contrast

Apply canonical Color rules.

Color must not be the only carrier of:

- Status
- Category
- Selection
- Priority
- Change
- Error
- Recommendation
- Data-series identity

Pair color with:

- Text
- Direct label
- Shape
- Pattern
- Position
- Icon
- Line style

Validate in the actual composition, not from palette approval alone.

---

## Grayscale and Reduced Color

Essential meaning must remain understandable when:

- Printed in grayscale
- Viewed with reduced saturation
- Projected in a bright room
- Seen on an uncalibrated display
- Viewed by people with common color-vision differences

Use direct labels and redundant cues.

---

## Charts

Charts must include:

- A clear purpose
- A message-led title where appropriate
- Visible units
- Direct labels or an understandable legend
- Source
- Text summary or alt text
- Non-color cues when several series matter
- Material limitations

Do not use:

- 3D effects
- Decorative gradients
- Unlabeled axes
- Color-only distinction
- Tiny source text
- Motion-only revelation

---

## Tables

Tables must:

- Use clear row and column headers
- Preserve logical reading order
- Use consistent alignment
- Avoid merged cells when they harm reading
- Use text or symbols in addition to color
- Provide a summary for the principal finding
- Remain readable after export

A dense table may require a separate reference artifact.

---

## Images

Images require:

- A defined communication role
- Meaningful alt text when non-decorative
- Source and rights information
- Non-misleading crop
- Sufficient text contrast if overlaid
- Clear identification when AI-generated

Decorative images should be marked decorative where supported.

Do not use generated imagery as evidence of a real person, place, event, product, or outcome.

---

## Diagrams

Diagrams require:

- Explicit direction
- Clear labels
- Understandable connector meaning
- Logical grouping
- A text summary for complex structures
- Meaning that survives removal of color and motion

Avoid connector crossings and ambiguous arrows.

---

## Motion and Animation

Motion may:

- Reveal sequence
- Support explanation
- Clarify transformation
- Preserve orientation

Motion must not:

- Carry essential meaning alone
- Flash or distract
- Remove audience control in self-guided artifacts
- Create unnecessary vestibular discomfort
- Break PDF or static export meaning

Provide a meaningful static state.

---

## Live Delivery

For live presentations:

- Confirm projection readability.
- Consider room size and viewing distance.
- Do not depend on subtle contrast.
- Describe important visual evidence verbally.
- Read critical text when necessary.
- Provide accessible copies before or after the session.
- State how questions and participation will work.
- Account for captions, interpretation, and assistive listening when required.
- Avoid rapid slide changes that prevent comprehension.

---

## Self-guided Delivery

A self-guided artifact must:

- Be understandable without narration
- Include context and transitions
- Preserve sources
- Explain abbreviations
- Include alt text or text summaries
- Use navigable structure
- Avoid hidden essential notes
- Identify version and owner

---

## Hybrid Delivery

A hybrid artifact must support live pacing without becoming incomplete when read independently.

Use:

- Concise visible message
- Complete labels
- Sufficient context
- Speaker notes for optional depth
- Appendix or linked evidence
- Explicit decision and action

---

## Speaker Notes

Speaker notes should support, not replace, accessible visible meaning.

Notes may include:

- Verbal descriptions
- Facilitation instructions
- Transition cues
- Source detail
- Timing
- Accessibility accommodations

Check that confidential notes are not exported accidentally.

---

## Alt Text

Alt text should communicate meaning and purpose.

### Image

Describe what the audience needs to understand, not every visual detail.

### Chart

Include:

- Main trend
- Focal comparison
- Important exception
- Relevant limitation

### Diagram

Include:

- Main structure
- Direction
- Relationship
- Outcome

Do not begin every alt text entry with “Image of” unless it creates value.

---

## Language and Cognition

Use:

- Clear sentence structure
- Consistent terminology
- Defined abbreviations
- Parallel lists
- Visible chunking
- Explicit transitions
- Concrete calls to action

Avoid:

- Unexplained jargon
- Metaphors that obscure meaning
- Overly dense screens
- Several competing reading paths
- Complex visuals without summaries

---

## Platform Validation

Record:

```yaml
platform:
version:
reading_order_checked:
alt_text_checked:
contrast_checked:
font_substitution_checked:
keyboard_navigation_checked:
pdf_export_checked:
notes_checked:
known_limitations:
tested_by:
tested_on:
```

Not every platform supports the same accessibility metadata. Limitations must be documented, not hidden.

---

## Accessible Export

Before export:

- Verify fonts
- Verify reading order
- Verify alt text
- Verify links
- Verify source legibility
- Verify page titles or bookmarks where supported
- Verify color and grayscale behavior
- Verify notes are included or excluded intentionally
- Verify no essential content is clipped
- Verify language metadata where supported

---

## Exceptions

An accessibility exception requires:

```yaml
rule:
barrier:
affected_users:
reason:
alternative_access:
mitigation:
owner:
approver:
expiry:
```

Aesthetic preference is not a valid reason.

---

## Accessibility Status

Use:

```text
not-reviewed
partial
verified
exception
```

`verified` requires actual testing in the intended platform and output format.

---

## Release Requirement

An artifact fails release when:

- Essential meaning depends only on color.
- Reading order is ambiguous.
- Canonical type or contrast requirements are not met.
- Important visuals lack an accessible text equivalent.
- The exported artifact loses essential content.
- A known barrier has no documented alternative.
- Accessibility needs identified in the brief are unmet.

Use [`Release_Gates.md`](./Release_Gates.md).
