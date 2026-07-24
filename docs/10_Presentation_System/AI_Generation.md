# AI Presentation Generation

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

AI Presentation Generation defines how AI should reason, specify, generate, adapt, and validate LINKGENT presentations.

AI must follow the same communication hierarchy as a human designer.

```text
AI Presentation Generation
≠ text placed into slide templates
```

AI must reference the canonical process `PRES-PROCESS-001` in [`Thinking.md`](./Thinking.md). This file does not define an alternative order.

---

## Inheritance

AI must read:

1. [`../../CONSTITUTION.md`](../../CONSTITUTION.md)
2. [`../01_Brand_Core.md`](../01_Brand_Core.md)
3. [`../03_Color_System.md`](../03_Color_System.md)
4. [`../04_Typography.md`](../04_Typography.md)
5. `../05_Design_Tokens.md` when active
6. `../06_Iconography.md` when active
7. [`README.md`](./README.md)
8. [`Thinking.md`](./Thinking.md)
9. [`Content.md`](./Content.md)
10. [`Accessibility.md`](./Accessibility.md)
11. [`Layout.md`](./Layout.md)
12. [`Components.md`](./Components.md)
13. [`Patterns.md`](./Patterns.md)
14. [`Release_Gates.md`](./Release_Gates.md)
15. [`Audit_Checklist.md`](./Audit_Checklist.md) when required
16. `../13_AI_Generation_Rules.md` when active

AI must not create independent brand rules when a canonical source exists.

---

## Human Responsibility

AI may:

- Analyze the audience
- Inventory and classify content
- Normalize terminology
- Identify evidence gaps
- Propose a Governing Message
- Build Narrative Architecture alternatives
- Specify slides
- Recommend Patterns and Components
- Generate editable artifacts
- Adapt between platforms
- Review logic, density, accessibility, and consistency

Humans retain responsibility for:

- Final purpose
- Strategic judgment
- Ethical judgment
- Evidence validity
- Confidentiality
- Legal and regulatory claims
- Decision ownership
- Brand approval
- Publication
- Delivery

AI output is proposed until an authorized human approves it.

---

## Input Contract

Before generation, AI must establish a Presentation Brief.

```yaml
audience:
  primary:
  decision_owner:
  secondary:
  knowledge_level:
purpose:
expected_outcome:
governing_message_status: unknown | proposed | approved
consumption_mode: live | self_guided | hybrid
session_mode: presentation | decision | workshop
artifact_role: working | read_ahead | reference | archive
available_time:
source_content:
evidence_requirements:
language:
localization:
accessibility_needs:
confidentiality:
output_platform:
aspect_ratio:
delivery_environment:
required_editability:
deadline:
approver:
```

The three classification axes must remain separate.

Do not use a single mixed `presentation_mode` field.

---

## Missing Information

AI should:

1. Infer only low-risk operational details.
2. Record every assumption.
3. Mark unresolved content as Unknown.
4. Stop generation of claims that would require invented evidence.
5. Ask for human resolution when the decision materially affects accuracy, ethics, accessibility, confidentiality, or approval.

AI must not invent:

- Data
- Sources
- Quotes
- Customer statements
- Research findings
- Financial values
- Dates
- Legal claims
- Approved decisions
- Performance outcomes

---

## Canonical Stage Outputs

AI executes `PRES-PROCESS-001`.

### Audience

Output:

```yaml
audience_profile:
decision_context:
known_concerns:
accessibility_needs:
delivery_conditions:
```

### Purpose and Expected Outcome

Output:

```yaml
purpose:
expected_outcome:
decision_or_action:
success_condition:
non_goals:
```

### Governing Message

Output:

```yaml
governing_message:
status:
supporting_claims:
required_evidence:
main_implication:
```

### Content Architecture

Output:

```yaml
content_inventory:
terminology_map:
evidence_map:
content_states:
priority_map:
unknowns:
removed_content:
```

### Narrative Architecture

Output:

```yaml
story_spine:
chapter_messages:
transition_logic:
claim_evidence_implication_action_map:
```

### Slide Architecture

Output one specification per slide.

```yaml
slide_id:
story_role:
purpose:
message:
message_type:
content_state:
evidence:
implication:
information_relationship:
density:
pattern:
primary_component:
supporting_components:
reading_order:
source_requirement:
alt_text_requirement:
speaker_note_requirement:
status:
```

### Representation / Pattern

Use namespaces from [`Patterns.md`](./Patterns.md).

Preferred:

```text
Presentation/Pattern/Comparison
```

Avoid:

```text
two blue boxes
```

### Component Composition

Use namespaces from [`Components.md`](./Components.md).

Preferred:

```text
Presentation/Component/Metric
```

AI should use one primary component and add supporting components only when semantically necessary.

### Layout

Apply [`Layout.md`](./Layout.md). AI must not select layout for visual variety.

### Typography

Apply:

- `TYPE-PRESENTATION-HIERARCHY`
- `TYPE-PRESENTATION-MIN-BODY`
- `TYPE-PRESENTATION-MIN-CAPTION`

Canonical values remain in [`../04_Typography.md`](../04_Typography.md).

AI must not copy or invent numeric typography values when a canonical rule exists.

### Color

Apply:

- `COLOR-CONTRAST-NORMAL`
- `COLOR-CONTRAST-LARGE`
- `COLOR-ACCENT-INVERSE-PROHIBITED`
- `COLOR-FOCAL-AREA-GUIDANCE`
- `COLOR-NOT-SOLE-CARRIER`

Canonical values and roles remain in [`../03_Color_System.md`](../03_Color_System.md).

AI must not copy raw color values into slide specifications unless a platform implementation explicitly requires resolved values.

### Imagery and Motion

AI must classify imagery as:

- Evidence
- Demonstration
- Context
- Human story
- Conceptual framing

AI-generated imagery must be labeled and must not be presented as factual evidence.

Motion must not carry essential meaning by itself.

### Validation

AI must run the Fast Gate in [`Release_Gates.md`](./Release_Gates.md).

AI must escalate to [`Audit_Checklist.md`](./Audit_Checklist.md) based on risk.

### Delivery

AI must output:

```yaml
delivery_platform:
version:
status:
owner:
approver:
distribution:
accessibility_accommodations:
source_record:
archive_location:
known_exceptions:
```

---

## Content Generation

Apply [`Content.md`](./Content.md).

AI should:

- Draft a message-led title where appropriate.
- Keep terminology stable.
- Separate facts, interpretations, assumptions, proposals, and unknowns.
- Use parallel grammar in lists.
- Normalize dates, units, and numerical precision.
- Create traceable source notes.
- Produce meaningful speaker notes.
- Produce alt text or chart summaries.
- Preserve material limitations.

AI must not create confident language that exceeds the evidence.

---

## Pattern and Component Status

AI must read maturity metadata.

AI may use:

- `stable` by default
- `candidate` in controlled work with validation
- `draft` only when explicitly requested
- `deprecated` only for migration

Because version `0.9.0` components and patterns are candidates, AI must mark their use as requiring validation.

---

## Platform Adaptation

AI adaptation order:

1. Preserve Governing Message.
2. Preserve content integrity.
3. Preserve Narrative Architecture.
4. Preserve Slide Architecture and reading order.
5. Preserve sources and accessibility.
6. Recompose Layout.
7. Map Typography and Color through canonical roles.
8. Validate editability.
9. Run conversion testing.
10. Record differences and exceptions.

AI must not adapt by scaling every object uniformly.

### PowerPoint

Prefer editable native objects, master layouts, theme mappings, and structured reading order.

### Google Slides

Check font substitution, grouping, alignment, speaker notes, and PDF export.

### Keynote

Check type metrics, master behavior, animation removal, and export.

### Canva

Check brand styles, editability, text reflow, and flattened objects.

### Figma Slides

Check components, shared styles, constraints, reading order, and export.

### Gamma and AI Tools

Treat output as provisional. Check invented content, layout drift, source loss, and editability.

---

## Design Token Use

When `05_Design_Tokens.md` is active:

```text
Semantic role
  ↓
Design token
  ↓
Platform mapping
  ↓
Rendered value
```

AI must not hardcode values when an approved semantic token exists.

Until then, use semantic names and canonical rule IDs.

---

## Traceability

AI-generated work should preserve:

```yaml
generation_system:
model:
generation_date:
source_set:
assumptions:
unknowns:
canonical_rules:
patterns:
components:
platform:
validation_result:
exceptions:
human_approver:
```

Traceability may be stored in metadata, notes, an accompanying specification, or version record.

---

## Validation Strategy

### Fast Gate

Required for every artifact.

### Risk-based Audit

Required when risk is elevated by:

- Executive decision
- External publication
- Accessibility need
- Legal, medical, financial, or regulatory content
- High-density evidence
- Multi-platform conversion
- AI-generated evidence or imagery
- Sensitive or confidential information

### Full Audit

Required for:

- Golden Decks
- Templates
- New Components or Patterns
- Major public artifacts
- System release validation

---

## AI Failure Conditions

AI must stop or flag the artifact when:

- Audience is unresolved.
- Purpose and expected outcome conflict.
- Governing Message is unsupported.
- Evidence is missing for a material claim.
- Content states are hidden.
- Reading order is ambiguous.
- Canonical typography or color rules cannot be met.
- Accessibility requirements cannot be met.
- Platform conversion destroys meaning.
- Confidential information may be exposed.
- The requested output implies approval that has not occurred.

---

## Prohibited AI Behavior

AI must not:

- Start from Layout or a Template
- Recreate a competing process sequence
- Invent data or sources
- Convert Unknown into apparent fact
- Use visual polish to imply evidence
- Create new brand colors for variety
- Invent typography values
- Use icons as decorative bullets
- Present generated images as documentary evidence
- Depend on motion for essential meaning
- Mark a candidate Component or Pattern stable
- Mark the system Active without required validation
- Skip human approval
