# Presentation Release Gates

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

Release Gates define the minimum quality conditions that every LINKGENT presentation must pass before delivery.

This is the Fast Gate.

Use [`Audit_Checklist.md`](./Audit_Checklist.md) for risk-based or full audits.

---

## Result States

Each gate receives:

```text
Pass
Fail
Exception
Not Applicable
```

An Exception requires:

```yaml
gate:
reason:
risk:
mitigation:
owner:
approver:
expiry:
```

A presentation cannot be released with an unresolved Fail.

---

## Gate 1: Audience

- [ ] The primary audience is explicit.
- [ ] The decision owner is identified when relevant.
- [ ] Audience knowledge, concerns, and accessibility needs have been considered.

**Fail condition:** The artifact is designed for an undefined or contradictory audience.

---

## Gate 2: Purpose and Outcome

- [ ] The purpose is stated as an audience outcome.
- [ ] The intended decision, alignment, learning, or action is explicit.
- [ ] Success and non-goals are understood.

**Fail condition:** Success is defined only as producing or presenting a deck.

---

## Gate 3: Governing Message

- [ ] The Governing Message is explicit.
- [ ] It is more specific than the topic.
- [ ] It is supported by available evidence.
- [ ] The complete deck supports, qualifies, or operationalizes it.

**Fail condition:** The deck has no coherent primary conclusion.

---

## Gate 4: Content Architecture

- [ ] Sources have been inventoried.
- [ ] Facts, interpretations, assumptions, proposals, and unknowns are distinguishable.
- [ ] Material evidence gaps are visible.
- [ ] Duplicated and irrelevant content has been removed.

**Fail condition:** Material claims depend on invented, missing, or hidden evidence.

---

## Gate 5: Narrative Architecture

- [ ] Chapter order follows a clear reasoning sequence.
- [ ] Transitions explain why the next section follows.
- [ ] The narrative leads toward the intended outcome.

**Fail condition:** The deck is only a collection of categorized slides.

---

## Gate 6: Slide Architecture

- [ ] Every slide has one primary message, question, decision, or instruction.
- [ ] Reading order is explicit.
- [ ] Evidence and implication are connected.
- [ ] Density is appropriate to the artifact context.

**Fail condition:** A slide contains several independent conclusions or ambiguous reading paths.

---

## Gate 7: Patterns and Components

- [ ] Patterns were selected from communication need.
- [ ] Components have semantic jobs.
- [ ] Candidate maturity has been acknowledged and validated.
- [ ] Deprecated items are not used for new work.

**Fail condition:** Layout or card composition substitutes for information structure.

---

## Gate 8: Content Quality

- [ ] Analytical slides use message-led titles where appropriate.
- [ ] Terminology, labels, grammar, dates, units, and numerical precision are consistent.
- [ ] Quotes and sources are verified.
- [ ] Calls to action identify actor, action, and timing.

**Fail condition:** Wording is ambiguous, misleading, or unsupported.

---

## Gate 9: Layout

- [ ] Safe area is preserved.
- [ ] Alignment and grouping are systematic.
- [ ] Whitespace reflects semantic relationships.
- [ ] The focal point and reading order are immediate.
- [ ] Platform adaptation is a recomposition, not mechanical scaling.

**Fail condition:** Meaning depends on arbitrary placement or unreadable density.

---

## Gate 10: Typography

- [ ] `TYPE-PRESENTATION-HIERARCHY` is applied.
- [ ] `TYPE-PRESENTATION-MIN-BODY` is applied.
- [ ] `TYPE-PRESENTATION-MIN-CAPTION` is applied.
- [ ] Content was restructured before typography was reduced.

**Fail condition:** Canonical typography requirements are violated.

---

## Gate 11: Color

- [ ] Canonical semantic color roles are used.
- [ ] `COLOR-CONTRAST-NORMAL` and `COLOR-CONTRAST-LARGE` are applied.
- [ ] `COLOR-ACCENT-INVERSE-PROHIBITED` is applied.
- [ ] `COLOR-FOCAL-AREA-GUIDANCE` is applied.
- [ ] `COLOR-NOT-SOLE-CARRIER` is applied.

**Fail condition:** Color meaning, contrast, or accessibility conflicts with the Color System.

---

## Gate 12: Images, Icons, and Motion

- [ ] Every image has a communication role.
- [ ] Generated imagery is identified and not presented as factual evidence.
- [ ] Icons improve recognition and are not decorative bullets.
- [ ] Motion is optional for understanding.

**Fail condition:** Visual media misleads, distracts, or carries essential meaning alone.

---

## Gate 13: Accessibility

- [ ] Reading order is clear.
- [ ] Essential visuals have text equivalents.
- [ ] Grayscale and reduced-color meaning is preserved.
- [ ] Identified accessibility needs are met.
- [ ] Exported formats have been checked.

**Fail condition:** A known barrier remains without an approved alternative.

---

## Gate 14: Sources and Traceability

- [ ] Material claims, charts, quotes, and images have traceable sources.
- [ ] Version, owner, status, and approval are recoverable.
- [ ] AI assumptions and unknowns are recorded when AI is used.

**Fail condition:** The audience cannot distinguish verified content from proposed or generated content.

---

## Gate 15: Platform and Export

- [ ] The artifact has been checked in the delivery platform.
- [ ] Font substitution has been reviewed.
- [ ] No essential content is clipped or reflowed incorrectly.
- [ ] PDF or distributed export has been reviewed.
- [ ] Editability matches the intended workflow.

**Fail condition:** Conversion or export changes meaning.

---

## Gate 16: Decision and Action

- [ ] The required decision or action is visible.
- [ ] Owner and timing are clear.
- [ ] Trade-offs and risks are not hidden.
- [ ] Next steps are operational.

**Fail condition:** The deck ends without a usable outcome.

---

## Gate 17: Brand Alignment

- [ ] The artifact feels Structured, Intelligent, Reliable, Beautiful, Minimal, Sophisticated, Human-centered, and Future-ready.
- [ ] Brand expression follows purpose.
- [ ] The deck is not trend-driven, decorative, or artificially futuristic.

**Fail condition:** Visual expression contradicts Brand Core.

---

## Gate 18: Approval

- [ ] The correct human owner has reviewed the artifact.
- [ ] Exceptions are approved and documented.
- [ ] The release status is accurate.
- [ ] Distribution and confidentiality are appropriate.

**Fail condition:** The artifact appears approved when it is not.

---

## Gate 19: Delivery Readiness

- [ ] Presenter, distribution, notes, accommodations, and archive location are prepared.
- [ ] Links and files are accessible to the intended audience.
- [ ] The delivered version matches the approved version.

**Fail condition:** The artifact cannot be used as intended.

---

## Gate 20: Final Comprehension Test

Ask:

```text
Can the intended audience understand what matters,
why it matters,
what evidence supports it,
and what should happen next?
```

- [ ] Yes

**Fail condition:** The answer is No or depends on explaining away the artifact's structure.

---

## Escalation to Audit

Use [`Audit_Checklist.md`](./Audit_Checklist.md) when:

- Any gate receives Exception.
- The artifact is executive-critical.
- The artifact is externally published.
- The content is regulated or high stakes.
- The deck is high-density.
- Accessibility needs are material.
- The artifact moves across platforms.
- AI generated significant content or visuals.
- A new Component or Pattern is being validated.
- The artifact is a Golden Deck or Template.

---

## Release Record

```yaml
artifact:
version:
status:
audience:
purpose:
consumption_mode:
session_mode:
artifact_role:
gate_result:
failed_gates:
exceptions:
audit_required:
reviewed_by:
approved_by:
release_date:
delivery_format:
archive_location:
```
