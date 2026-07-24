# Presentation Review Checklist

> Version: 1.0.0  
> Status: Draft — Git Ready  
> Owner: LINKGENT Brand OS  
> Last Updated: 2026-07-24

---

## Purpose

This checklist reviews whether a LINKGENT presentation is logically sound, understandable, persuasive, visually disciplined, accessible, AI-ready, and consistent with Brand OS.

Review from the top of the Presentation Pyramid downward. Do not begin with visual polish.

```text
Brand
  ↓
Audience and Purpose
  ↓
Information Architecture
  ↓
Story
  ↓
Layout
  ↓
Typography
  ↓
Color
  ↓
Decoration
```

A failure in a higher layer cannot be repaired by a lower layer.

---

## Canonical References

Review this checklist together with:

1. [`../../CONSTITUTION.md`](../../CONSTITUTION.md)
2. [`../01_Brand_Core.md`](../01_Brand_Core.md)
3. [`../03_Color_System.md`](../03_Color_System.md)
4. [`../04_Typography.md`](../04_Typography.md)
5. [`README.md`](./README.md)
6. [`Thinking.md`](./Thinking.md)
7. [`Layout.md`](./Layout.md)
8. [`Components.md`](./Components.md)
9. [`Templates.md`](./Templates.md)
10. [`AI_Generation.md`](./AI_Generation.md)

This file reviews Presentation-specific application. It does not redefine canonical Brand Foundations.

---

## How to Use

Use this checklist:

- Before high-fidelity design
- After the first complete draft
- Before stakeholder review
- After platform conversion
- Before export or delivery
- After AI generation
- Before a template is approved for reuse

### Review Status

| Status | Meaning |
|---|---|
| Pass | Requirement is satisfied |
| Revise | Improvement is required before release |
| Blocker | Presentation must not be released |
| N/A | Requirement does not apply; the reason is recorded |

---

## Release Gates

A presentation is not release-ready when:

- Any Blocker remains
- Audience, purpose, or expected action is undefined
- Material claims are unsupported, fabricated, or misleading
- The story does not lead to the intended decision or outcome
- Essential text is below the approved minimum size
- Essential meaning depends only on color, icon, or animation
- Contrast fails
- Data visualization is distorted
- Brand OS conflicts remain unresolved
- Confidential or restricted information is exposed incorrectly

---

# 1. Audience

- [ ] The primary audience is explicitly defined.
- [ ] The audience's existing knowledge is understood.
- [ ] The audience's priorities, concerns, and likely objections are reflected.
- [ ] The audience's decision authority is clear.
- [ ] The presentation context is defined: live, self-guided, decision, workshop, reference, or hybrid.
- [ ] Viewing conditions, available time, and attention constraints are considered.
- [ ] Language and terminology match the audience.
- [ ] Accessibility needs are considered.
- [ ] The deck is organized for the audience, not the creator's work process.

### Blocker Conditions

- [ ] The audience is described only as a broad role with no decision context.
- [ ] The presentation assumes knowledge essential to understanding.
- [ ] The audience cannot identify why the content matters to them.

---

# 2. Purpose and Expected Action

- [ ] The presentation has one primary purpose.
- [ ] The purpose is written as a specific audience outcome.
- [ ] The expected decision, action, alignment, or understanding is explicit.
- [ ] The opening establishes relevance.
- [ ] The closing requests or confirms the intended outcome.
- [ ] Secondary objectives do not compete with the primary purpose.
- [ ] Every major section supports the purpose.

### Purpose Statement

```text
After this presentation, [audience] should understand / believe / decide / do [specific outcome].
```

### Blocker Conditions

- [ ] The deck has no clear outcome.
- [ ] The requested decision is missing or ambiguous.
- [ ] The presentation is an information archive presented as a decision tool.

---

# 3. Governing Message

- [ ] One governing message is defined.
- [ ] The message is relevant to the audience.
- [ ] The message is specific and defensible.
- [ ] The message is consequential or actionable.
- [ ] Supporting messages form a clear hierarchy.
- [ ] The deck can be summarized in three to seven sentences.
- [ ] The governing message is reinforced in the summary or closing.

### Blocker Conditions

- [ ] The deck contains several unrelated main messages.
- [ ] The conclusion changes across slides without explanation.
- [ ] The governing message is stronger than the evidence supports.

---

# 4. Logic and Evidence

- [ ] Facts, observations, interpretations, assumptions, forecasts, and recommendations are distinguishable.
- [ ] Claims are supported by appropriate evidence.
- [ ] Evidence is relevant to the audience's decision.
- [ ] Sources are shown when needed.
- [ ] Units, dates, time periods, samples, and definitions are clear.
- [ ] Limitations and uncertainty are disclosed when material.
- [ ] Correlation is not presented as causation without evidence.
- [ ] The presentation does not overstate certainty.
- [ ] Counterevidence and material trade-offs are not hidden.
- [ ] Recommendations follow logically from the evidence.

### Blocker Conditions

- [ ] Data, quotes, sources, or outcomes are fabricated.
- [ ] Evidence is materially distorted.
- [ ] Assumptions are presented as verified facts.
- [ ] The recommendation is disconnected from the diagnosed problem.

---

# 5. Information Architecture

- [ ] Only information required for the purpose is included in the main narrative.
- [ ] Related information is grouped.
- [ ] Primary, supporting, contextual, and reference information are distinct.
- [ ] Labels describe meaning clearly.
- [ ] Relationships are explicit: comparison, cause, hierarchy, flow, sequence, or time.
- [ ] Duplicate content is removed.
- [ ] Detail is moved to an appendix, notes, or reference layer when appropriate.
- [ ] The structure remains understandable without color or decoration.
- [ ] Source-document order has not been copied mechanically.
- [ ] The information architecture reduces cognitive burden without removing necessary nuance.

### Blocker Conditions

- [ ] Necessary context is missing.
- [ ] Information groups overlap or contradict one another.
- [ ] The audience must infer the relationship between major elements.

---

# 6. Story

- [ ] The story has a clear starting state and intended ending state.
- [ ] The sequence supports how the audience needs to understand the topic.
- [ ] Every chapter answers a meaningful audience question.
- [ ] Every slide connects to the slide before and after it.
- [ ] Transitions between major ideas are clear.
- [ ] The story contains only necessary steps.
- [ ] The recommendation or conclusion appears after sufficient evidence.
- [ ] The presentation ends with an implication, decision, or action.
- [ ] The story remains coherent without relying on visual effects.

### Blocker Conditions

- [ ] Slides can be reordered without changing meaning because no story exists.
- [ ] The deck reaches a conclusion before establishing the problem or evidence.
- [ ] The ending does not resolve the purpose established at the beginning.

---

# 7. One Slide, One Message

For every slide:

- [ ] The sentence “This slide shows that…” can be completed clearly.
- [ ] The title reflects the primary message when appropriate.
- [ ] All elements support the same conclusion.
- [ ] Supporting information is visually subordinate.
- [ ] Independent claims have been split into separate slides.
- [ ] Topic titles are used only when their navigation role is intentional.
- [ ] The message is understandable within a few seconds.

### Blocker Conditions

- [ ] A slide contains multiple independent messages.
- [ ] The title and body communicate different conclusions.
- [ ] The audience must read every word to identify the point.

---

# 8. Information Density

- [ ] Density is appropriate for live, self-guided, or hybrid use.
- [ ] The message is processed before the detail.
- [ ] The number of concepts is controlled.
- [ ] Major visual groups are limited and clearly prioritized.
- [ ] Long paragraphs are edited, structured, or split.
- [ ] High-density slides use explicit labels and stable alignment.
- [ ] Reference detail is separated from decision-driving content.
- [ ] No text is reduced below the Typography System minimum to fit content.
- [ ] The slide remains understandable at realistic viewing size.

### Density Repair Order

1. Remove irrelevant content.
2. Rewrite for clarity.
3. Group related information.
4. Convert relationships into diagrams or comparisons.
5. Move reference detail.
6. Split the slide.
7. Rebuild the story.

### Blocker Conditions

- [ ] Essential content is unreadable.
- [ ] More than one reading path appears primary.
- [ ] Density prevents the audience from identifying the message.

---

# 9. Diagram and Comparison

- [ ] Diagrams represent real relationships.
- [ ] Direction, hierarchy, or sequence is unambiguous.
- [ ] Every connector has meaning.
- [ ] Shapes have consistent semantic roles.
- [ ] Comparison dimensions are defined before styling.
- [ ] Compared units, scales, periods, and levels of detail are equivalent.
- [ ] The decisive difference is highlighted.
- [ ] The conclusion is stated.
- [ ] Bullet points have not simply been placed inside decorative boxes.

### Blocker Conditions

- [ ] The diagram implies a relationship that does not exist.
- [ ] The comparison uses unequal scales or criteria without disclosure.
- [ ] Visual size or position materially exaggerates a difference.

---

# 10. Layout

Review against [`Layout.md`](./Layout.md).

- [ ] Essential content is inside the safe area.
- [ ] The grid is consistent and supports the message.
- [ ] Every element aligns to a meaningful anchor.
- [ ] Related elements are closer than unrelated elements.
- [ ] Whitespace communicates grouping and focus.
- [ ] One dominant focal region is clear.
- [ ] Column count matches content equivalence and density.
- [ ] Reading order is discoverable.
- [ ] Titles, content, captions, and sources are spatially connected.
- [ ] Asymmetry is intentional and anchored.
- [ ] The slide remains structured when borders, fills, and color are removed.
- [ ] Layout has been rebuilt, not stretched, after aspect-ratio conversion.
- [ ] The deck has rhythm without forced uniformity.

### Blocker Conditions

- [ ] Essential content is too close to the canvas edge.
- [ ] Multiple elements compete for first attention.
- [ ] The reading order is ambiguous.
- [ ] Layout depends on editing-view zoom to remain readable.

---

# 11. Whitespace and Visual Balance

- [ ] Empty space supports focus, grouping, pause, or rhythm.
- [ ] Whitespace is distributed intentionally rather than used as leftover space.
- [ ] Visual weight is balanced around meaningful anchors.
- [ ] Dense and sparse regions support the message.
- [ ] The composition has one clear center of gravity.
- [ ] Cards and containers are not used only to fill space.
- [ ] Symmetry or asymmetry reflects the information relationship.
- [ ] The slide remains calm without becoming empty or weak.

### Blocker Conditions

- [ ] Whitespace separates information that should be understood together.
- [ ] The slide feels visually unstable or unintentionally lopsided.
- [ ] Decorative objects are used to correct an unresolved balance problem.

---

# 12. Components

Review against [`Components.md`](./Components.md).

- [ ] Every component has a semantic role.
- [ ] The primary component matches the information relationship.
- [ ] Supporting components are necessary.
- [ ] Component variants are selected by meaning, not appearance.
- [ ] Cards group genuinely related content.
- [ ] Callouts contain information that deserves interruption or emphasis.
- [ ] Tables support precise lookup or comparison.
- [ ] Charts answer an analytical question.
- [ ] Timelines represent chronology.
- [ ] Roadmaps represent planned progression.
- [ ] Flows represent movement or transfer.
- [ ] Processes represent ordered action.
- [ ] Metrics include context, unit, and implication.
- [ ] Components remain editable when editability is required.

### Blocker Conditions

- [ ] A component implies the wrong relationship.
- [ ] Decorative containers replace information architecture.
- [ ] Unapproved variants create contradictory meanings.

---

# 13. Templates

Review against [`Templates.md`](./Templates.md).

- [ ] The template matches the slide's story role.
- [ ] The template supports the message rather than forcing content into slots.
- [ ] The slide remains understandable when template styling is removed.
- [ ] Repeated templates preserve consistency without creating monotony.
- [ ] Template adaptation preserves semantic regions.
- [ ] A new template is introduced only when existing patterns cannot express the required story role.

### Blocker Conditions

- [ ] The template determines the story.
- [ ] Content was added or removed only to fill a template.
- [ ] Template use creates a false comparison, hierarchy, or sequence.

---

# 14. Typography

Review against [`../04_Typography.md`](../04_Typography.md).

- [ ] Typography reveals hierarchy before the audience reads every word.
- [ ] Semantic typography roles are used.
- [ ] A maximum of three visible hierarchy levels is used per slide.
- [ ] BIZ UDPゴシック is used for Japanese when supported.
- [ ] Inter is used for Latin text and numbers when supported.
- [ ] Approved fallbacks are used where required.
- [ ] Display, H1, H2, Body Large, Body, and Caption are used according to meaning.
- [ ] Presentation Body is not below `16 pt` in the current PowerPoint baseline.
- [ ] Presentation Caption is not below `11 pt` in the current PowerPoint baseline.
- [ ] Equivalent perceived hierarchy is preserved in other platforms.
- [ ] Long centered paragraphs are avoided.
- [ ] Line height and vertical rhythm support reading.
- [ ] Emphasis uses structure, hierarchy, weight, spacing, and then color.
- [ ] Text is rewritten or split before size is reduced.

### Blocker Conditions

- [ ] Essential text is below the approved minimum.
- [ ] Caption styling is used for primary information.
- [ ] Typography hierarchy contradicts content hierarchy.
- [ ] Text is distorted, compressed, or clipped.

---

# 15. Color

Review against [`../03_Color_System.md`](../03_Color_System.md).

- [ ] Neutral surfaces dominate.
- [ ] Primary is used for structure, trust, and hierarchy.
- [ ] Accent is used for one deliberate focal purpose.
- [ ] Accent generally remains below approximately `10%` of visible slide area.
- [ ] Semantic status colors are used only for their defined meaning.
- [ ] The same role uses the same color meaning across the deck.
- [ ] `#0B1320` is used instead of white text on `#29B6E8`.
- [ ] `#087899` or darker is used for accent-colored text on light surfaces.
- [ ] Contrast is tested in the actual composition.
- [ ] Normal text targets at least `4.5:1` contrast.
- [ ] Large text and meaningful non-text graphics target at least `3:1` contrast.
- [ ] Color is not the only carrier of meaning.
- [ ] Charts remain understandable in grayscale and common color-vision-deficiency conditions.
- [ ] Projection and low-quality display conditions are considered.
- [ ] No arbitrary tints, gradients, glow, neon, or unapproved colors are used.

### Blocker Conditions

- [ ] Essential text fails contrast.
- [ ] White text appears on `#29B6E8`.
- [ ] Semantic red, amber, or green is used decoratively.
- [ ] Color alone communicates status, category, or selection.

---

# 16. Icons

- [ ] Material Symbols Outlined is used as the default family.
- [ ] One icon family and style is used consistently.
- [ ] Icons support recognition or scanning.
- [ ] Ambiguous icons have labels.
- [ ] Stroke and optical size feel consistent.
- [ ] Icons align optically with text and containers.
- [ ] Neutral or Primary is used by default.
- [ ] Accent is limited to a focal icon.
- [ ] Semantic color is used only for explicit status meaning.
- [ ] Icons are not stretched or distorted.
- [ ] Emoji and mixed icon families are not used as substitutes.

### Blocker Conditions

- [ ] An icon is the only carrier of essential meaning and is ambiguous.
- [ ] Mixed icon styles materially reduce consistency or comprehension.

---

# 17. Images and Quotes

- [ ] Every image has a defined role: evidence, demonstration, context, human story, or conceptual framing.
- [ ] Images are credible, relevant, and high enough resolution.
- [ ] Aspect ratio is preserved.
- [ ] Cropping does not change source meaning.
- [ ] Human subjects are represented respectfully.
- [ ] AI-generated imagery is not presented as documentary evidence.
- [ ] Text over images has verified contrast.
- [ ] Essential text does not overlap faces or complex detail.
- [ ] Rights, sources, and attribution are included when required.
- [ ] Quotes are exact and attributed.
- [ ] Quote context is sufficient to avoid misrepresentation.

### Blocker Conditions

- [ ] Fabricated imagery or quotations are presented as evidence.
- [ ] Image use violates confidentiality, rights, or human dignity.
- [ ] Text over imagery is unreadable.

---

# 18. Charts and Data

- [ ] The chart type matches the analytical question.
- [ ] The takeaway is stated.
- [ ] Units, scale, baseline, and time range are clear.
- [ ] Data is accurate and sourced.
- [ ] Actual, forecast, and target values are distinguishable.
- [ ] Neutral comparison series and one focal series are used where appropriate.
- [ ] Series meanings remain consistent across slides.
- [ ] Direct labels are used where practical.
- [ ] Legends, gridlines, and decoration are removed when unnecessary.
- [ ] Scales and proportions are truthful.
- [ ] Tables align comparable values.
- [ ] Precision is appropriate.
- [ ] Sources and methodology remain attached to the visual.

### Blocker Conditions

- [ ] Data is fabricated or materially inaccurate.
- [ ] An axis or visual proportion is misleading.
- [ ] A chart uses 3D effects that distort perception.
- [ ] Semantic colors are used as arbitrary data categories.

---

# 19. Persuasiveness and Decision Support

- [ ] The presentation makes the audience's problem or decision explicit.
- [ ] The evidence is sufficient for the requested level of commitment.
- [ ] Trade-offs and risks are visible.
- [ ] Alternatives are evaluated using stated criteria.
- [ ] The recommendation is specific.
- [ ] The value and implications are clear.
- [ ] The next action has an owner or decision point when appropriate.
- [ ] Persuasion comes from reasoning, not visual pressure.
- [ ] The presentation preserves trust even when evidence is incomplete.

---

# 20. Beauty and Brand Personality

- [ ] The presentation feels Structured.
- [ ] The presentation feels Intelligent.
- [ ] The presentation feels Reliable.
- [ ] The presentation feels Beautiful.
- [ ] The presentation feels Minimal without removing necessary meaning.
- [ ] The presentation feels Sophisticated without visual excess.
- [ ] The presentation feels Human-centered.
- [ ] The presentation feels Future-ready through clarity and precision.
- [ ] Beauty emerges from purpose, hierarchy, rhythm, and restraint.
- [ ] Visual expression does not compete with comprehension.
- [ ] The deck avoids trend-driven or artificially futuristic styling.

---

# 21. Accessibility

- [ ] Essential content is readable under realistic viewing conditions.
- [ ] Minimum typography sizes are preserved.
- [ ] Contrast is verified.
- [ ] Color is not the only carrier of meaning.
- [ ] Reading order is logical.
- [ ] Charts and diagrams have direct labels or descriptions.
- [ ] Images have alternative descriptions in accessible outputs where supported.
- [ ] Motion and animation are not required for essential understanding.
- [ ] Grayscale output remains understandable.
- [ ] Bright-room projection has been considered.
- [ ] Exported PDF preserves text and reading order where technically possible.
- [ ] Accessibility requirements take precedence over visual preference.

---

# 22. Cross-Platform Quality

- [ ] The presentation has been checked in the target platform.
- [ ] Font substitution has been reviewed.
- [ ] Text wrapping and clipping have been reviewed.
- [ ] Image crops and masks are stable.
- [ ] Connectors and diagram relationships remain correct.
- [ ] Charts, labels, and tables remain editable when required.
- [ ] Safe area is preserved.
- [ ] Aspect-ratio adaptation has been rebuilt, not stretched.
- [ ] Exported PDF or image output matches the intended hierarchy.
- [ ] Essential meaning does not depend on a platform-only effect.
- [ ] The same semantic intent is preserved across tool implementations.

---

# 23. AI Ready

Review against [`AI_Generation.md`](./AI_Generation.md).

- [ ] Audience, purpose, and expected action are documented.
- [ ] The governing message is documented.
- [ ] A slide plan exists for AI-generated or highly reusable decks.
- [ ] Slides have stable IDs when appropriate.
- [ ] Object and layer names are semantic where supported.
- [ ] Typography roles are used instead of arbitrary numeric instructions.
- [ ] Color roles are used instead of raw-value-only instructions.
- [ ] Components and templates are identified semantically.
- [ ] Sources and assumptions are traceable.
- [ ] Defined, Derived, Proposed, and Unknown knowledge states are distinguished.
- [ ] Exceptions are documented.
- [ ] AI-generated imagery and content are identifiable when required.
- [ ] The deck can be edited by another person or AI without reverse-engineering its logic.
- [ ] Review results are recorded for important reusable assets.

### Blocker Conditions

- [ ] AI-generated claims, data, quotes, or sources are unverified.
- [ ] AI output cannot be traced to source material for material claims.
- [ ] The generated deck violates Brand OS without reporting the conflict.

---

# 24. Brand OS Alignment

- [ ] `CONSTITUTION.md` has been respected.
- [ ] `01_Brand_Core.md` principles are preserved.
- [ ] Color uses the canonical Color System.
- [ ] Typography uses the canonical Typography System.
- [ ] Presentation-specific rules do not redefine Brand Foundations.
- [ ] The deck follows Structure First.
- [ ] The deck follows UX Before UI.
- [ ] The deck follows Beauty Through Purpose.
- [ ] The deck follows Human × AI Collaboration.
- [ ] The deck functions as a reusable system rather than an isolated artifact when reuse is intended.
- [ ] Communication completes the journey from thinking to value.
- [ ] Any approved exception includes scope, rationale, owner, and review date.

---

## Scoring Model

Use the score only after Blockers are resolved.

| Score | Meaning |
|---:|---|
| 0 | Missing or materially incorrect |
| 1 | Weak; major revision required |
| 2 | Acceptable; targeted revision recommended |
| 3 | Strong; meets LINKGENT standard |

| Category | Score |
|---|---:|
| Audience and Purpose | /3 |
| Governing Message | /3 |
| Logic and Evidence | /3 |
| Information Architecture | /3 |
| Story | /3 |
| One Slide, One Message | /3 |
| Density | /3 |
| Layout and Whitespace | /3 |
| Components and Templates | /3 |
| Typography | /3 |
| Color | /3 |
| Icons, Images, and Data | /3 |
| Persuasiveness | /3 |
| Accessibility | /3 |
| Brand Personality | /3 |
| AI Readiness | /3 |
| Brand OS Alignment | /3 |
| **Total** | **/51** |

### Recommended Release Threshold

- No Blockers
- No category scored `0`
- Audience and Purpose, Logic and Evidence, Story, Accessibility, and Brand OS Alignment must each score `3`
- Total score should normally be at least `43/51`

A score does not replace judgment. A presentation may still require revision when a high-risk issue is not captured numerically.

---

## Final Three-Second Test

For every slide, ask:

- [ ] Can the audience identify the primary message within three seconds?
- [ ] Can they identify the supporting structure without reading every word?
- [ ] Can they tell why the slide matters in the larger story?

If not, revise the highest failing layer first.

---

## Final Release Statement

Complete before delivery:

```text
Audience:
Purpose:
Expected Action:
Governing Message:
Delivery Mode:
Target Platform:
Reviewer:
Review Date:
Open Exceptions:
Release Status: Approved / Revise / Blocked
```

---

## Core Principle

> **Review the quality of the thinking before reviewing the quality of the styling.**
