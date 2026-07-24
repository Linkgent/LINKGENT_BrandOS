# Golden Deck Validation

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

Golden Decks prove that the Presentation System can produce consistent, usable, accessible, and cross-platform outcomes.

Documentation alone does not qualify the system for `1.0.0 / Active`.

---

## Required Golden Decks

### GD-01 — Live Decision Deck

```yaml
consumption_mode: live
session_mode: decision
artifact_role: working
expected_density: low-to-medium
primary_platform: powerpoint
```

Must validate:

- Governing Message clarity
- Decision framing
- Options and trade-offs
- Live pacing
- Projection readability
- Presenter dependence
- Release Gate completion

### GD-02 — UX / Research Read-ahead

```yaml
consumption_mode: self_guided
session_mode: presentation
artifact_role: read_ahead
expected_density: medium-to-high
primary_platform: powerpoint-or-google-slides
```

Must validate:

- Evidence traceability
- Message-led titles
- Research finding structure
- Source and footnote behavior
- High-density readability
- Independent comprehension
- Release Gate and risk-based Audit completion

### GD-03 — Cross-platform Reference Deck

```yaml
consumption_mode: hybrid
session_mode: presentation
artifact_role: reference
expected_density: medium
primary_platform: powerpoint
required_conversion:
  - google-slides
  - pdf
```

Must validate:

- Typography substitution
- Layout drift
- Token mapping
- Component and Pattern survival
- Source preservation
- Alt text and reading order
- Editability after conversion
- Full Audit completion

---

## Validation Record

Create one record per platform and version.

```yaml
golden_deck_id:
version:
system_version:
date:
reviewer:
source_platform:
target_platforms:
release_gate_result: pass | conditional | fail
audit_level: fast | risk-based | full
audit_result:
accessibility_status:
component_results:
pattern_results:
typography_failures:
color_failures:
layout_failures:
conversion_issues:
ai_interpretation_failures:
exceptions:
known_limitations:
required_changes:
retest_date:
```

---

## Promotion Criteria

Presentation System may move to `1.0.0 / Active` only when:

- All three Golden Decks exist as editable artifacts.
- Each passes mandatory Release Gates.
- GD-02 passes a risk-based Audit.
- GD-03 passes a Full Audit.
- Critical accessibility failures are resolved.
- Platform conversion limitations are documented.
- Candidate Components and Patterns used by the decks have validation records.
- No unresolved P0 governance contradiction remains.

---

## Failure Handling

Classify failures as:

```text
Content failure
Process failure
Pattern failure
Component failure
Token failure
Platform failure
AI interpretation failure
Documentation failure
```

Update the canonical owner rather than adding local workarounds to a Golden Deck.
