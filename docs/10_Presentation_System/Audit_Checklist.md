# Presentation Audit Checklist

> Version: 0.9.0  
> Status: Release Candidate  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

---

## Purpose

The Presentation Audit Checklist provides a detailed review for high-risk, system-critical, template, and Golden Deck work.

It is not required in full for every routine artifact.

Review sequence:

```text
Release Gates
  ↓
Risk-based Audit
  ↓
Full Audit
```

---

## Audit Modes

### Risk-based Audit

Select categories related to identified risks.

### Full Audit

Review every category.

Required for:

- Golden Deck validation
- New Template validation
- Stable Component or Pattern promotion
- Executive-critical decisions
- Major external publication
- Regulated or high-stakes content
- Brand OS release validation

---

## Scoring

Use:

```text
2 = Pass
1 = Partial / Exception
0 = Fail
N/A = Not Applicable
```

A high numeric score does not override a P0 failure.

Record:

```yaml
category:
score:
finding:
severity: P0 | P1 | P2
owner:
action:
due:
evidence:
```

---

## 1. Audience

- Is the primary audience explicit?
- Is the decision owner explicit?
- Are secondary audiences intentionally supported?
- Is prior knowledge understood?
- Are concerns and objections known?
- Is vocabulary appropriate?
- Are cultural and language contexts considered?
- Are accessibility needs identified?
- Are viewing conditions known?
- Is available time reflected in density and pacing?

---

## 2. Purpose and Expected Outcome

- Is purpose stated as an audience outcome?
- Is the required decision, alignment, learning, or action explicit?
- Is the success condition measurable or observable?
- Are non-goals visible?
- Does the presentation avoid serving several incompatible purposes?
- Is the artifact classification appropriate?

---

## 3. Governing Message

- Is the Governing Message specific?
- Is it more than a topic?
- Is it relevant to the audience?
- Is it supported?
- Does it govern inclusion and exclusion?
- Does each chapter connect to it?
- Are limitations and uncertainty preserved?

---

## 4. Content Architecture

- Are all relevant sources inventoried?
- Are duplicate sources reconciled?
- Are terms normalized?
- Are time periods and units normalized?
- Are facts, interpretations, assumptions, proposals, and unknowns classified?
- Are evidence gaps visible?
- Is content prioritized as essential, supporting, reference, or remove?
- Has irrelevant content been removed?
- Is confidential content handled correctly?

---

## 5. Evidence and Claims

- Does each material claim have a traceable source?
- Is source quality appropriate?
- Are dates and scope visible?
- Are methods and sample limitations visible?
- Are estimates labeled?
- Are causal claims justified?
- Are forecasts distinguished from actuals?
- Are AI-generated statements identified?
- Are quotes exact and authorized?
- Are contrary findings represented when material?

---

## 6. Narrative Architecture

- Is the entry point appropriate?
- Is the central question, tension, risk, or opportunity clear?
- Does each chapter advance understanding?
- Are transitions logical?
- Does evidence appear before conclusions that require it?
- Are trade-offs visible?
- Does the narrative lead to the expected outcome?
- Is the appendix separated from the primary story?
- Is repetition intentional?

---

## 7. Slide Architecture

- Does every slide have one primary message?
- Does the title represent the whole slide?
- Is the evidence role clear?
- Is the implication visible?
- Is the information relationship explicit?
- Is reading order clear?
- Is density assigned correctly?
- Are sources attached?
- Are notes and alt-text requirements specified?
- Should any slide be split, combined, moved, or removed?

---

## 8. Content and Writing

- Are message-led titles used where appropriate?
- Are topic titles reserved for navigation or neutral framing?
- Is wording concrete and concise?
- Are lists grammatically parallel?
- Are labels stable?
- Are abbreviations defined?
- Are dates unambiguous?
- Are units consistent?
- Is numerical precision justified?
- Are calls to action operational?
- Is inclusive language used?
- Is translation reviewed?
- Are speaker notes complete and safe?
- Is alt text meaningful?

---

## 9. Pattern Selection

- Was each Pattern selected after Slide Architecture?
- Does it solve a recurring communication need?
- Is its maturity status acceptable?
- Are required inputs present?
- Are known limitations relevant?
- Does it preserve the intended narrative role?
- Is a custom Pattern actually necessary?
- Does the Pattern avoid becoming a visual template substitute?

---

## 10. Component Composition

- Does every Component have a semantic job?
- Is one primary Component evident?
- Are supporting Components necessary?
- Are Cards overused?
- Do Components share a coherent hierarchy?
- Are maturity and accessibility statuses visible?
- Are deprecated Components avoided?
- Are platform limitations documented?
- Does composition survive export and conversion?

---

## 11. Layout

- Is the safe area protected?
- Is the grid systematic?
- Are columns selected from information structure?
- Is whitespace meaningful?
- Are related items grouped?
- Are unrelated items separated?
- Are alignment anchors shared?
- Is vertical rhythm coherent?
- Is one dominant composition visible?
- Is visual balance appropriate?
- Are sources attached?
- Does the layout survive aspect-ratio change?

---

## 12. Typography

- Is `TYPE-PRESENTATION-HIERARCHY` applied?
- Is `TYPE-PRESENTATION-MIN-BODY` applied?
- Is `TYPE-PRESENTATION-MIN-CAPTION` applied?
- Are semantic typography roles used?
- Are hierarchy levels limited?
- Are paragraphs readable?
- Are line lengths appropriate?
- Is text left-aligned when scanning requires it?
- Are fallbacks validated?
- Was content restructured before type reduction?
- Are local overrides controlled?

---

## 13. Color

- Are semantic roles selected before raw values?
- Is `COLOR-CONTRAST-NORMAL` applied?
- Is `COLOR-CONTRAST-LARGE` applied?
- Is `COLOR-ACCENT-INVERSE-PROHIBITED` applied?
- Is `COLOR-FOCAL-AREA-GUIDANCE` applied?
- Is `COLOR-NOT-SOLE-CARRIER` applied?
- Does Primary communicate structure?
- Does Accent communicate one focal purpose?
- Are semantic colors used only for their meaning?
- Are charts understandable in grayscale?
- Are invented hues or opacity variants absent?

---

## 14. Data Visualization

- Is the chart type appropriate?
- Is the analytical purpose clear?
- Are scales honest?
- Are units and periods consistent?
- Are direct labels used when useful?
- Is the focal series justified?
- Are comparison series subordinate?
- Are annotations restrained?
- Are sources visible?
- Is a text summary available?
- Are limitations stated?
- Are decorative effects absent?

---

## 15. Tables

- Is a table the correct representation?
- Are headers clear?
- Is sort order meaningful?
- Are numbers aligned?
- Are units visible?
- Are fills restrained?
- Is the key finding visible?
- Is reading order accessible?
- Is the table readable in export?
- Should detail move to a reference artifact?

---

## 16. Images and Quotes

- Does every image have a communication role?
- Is the source and usage right known?
- Is cropping honest?
- Is generated imagery identified?
- Is alt text present?
- Is text contrast protected?
- Are quotes exact?
- Are speaker, role, date, and source visible?
- Are quote edits responsible?
- Is decorative filler removed?

---

## 17. Icons and Diagrams

- Does each icon improve recognition?
- Is one icon family used?
- Are unfamiliar icons labeled?
- Are icons excluded as decorative bullets?
- Do diagrams show direction?
- Are connector meanings clear?
- Are crossings minimized?
- Does meaning survive color and motion removal?
- Is a text summary available for complexity?
- Is provisional Iconography status acknowledged?

---

## 18. Motion

- Does motion clarify sequence or transformation?
- Is essential meaning available without motion?
- Is pacing appropriate?
- Is the audience able to follow?
- Does static export remain coherent?
- Are distracting or vestibular-risk effects avoided?
- Are animations preserved or removed intentionally in conversion?

---

## 19. Accessibility

- Is reading order visually clear?
- Is technical reading order checked where supported?
- Are canonical typography and color rules met?
- Is color-independent meaning preserved?
- Are charts and diagrams summarized?
- Are images described?
- Are links usable?
- Are identified accommodations provided?
- Is live verbal description planned?
- Is self-guided use complete?
- Are platform limitations documented?
- Are exceptions approved?

---

## 20. Platform Adaptation

- Was the target platform identified in the brief?
- Was adaptation performed by recomposition?
- Are fonts available or mapped?
- Are masters or shared styles used?
- Are Components editable?
- Are notes preserved?
- Is alt text preserved?
- Are sources preserved?
- Are links preserved?
- Has PDF export been checked?
- Has cross-platform conversion been checked?
- Are differences documented?

---

## 21. AI Readiness and Traceability

- Did AI reference `PRES-PROCESS-001`?
- Were all stage outputs preserved?
- Are assumptions recorded?
- Are unknowns visible?
- Are source sets recorded?
- Are generated claims distinguishable?
- Are candidate Components and Patterns validated?
- Are canonical Rule IDs referenced?
- Is the model and date recorded where required?
- Has a human approved the output?
- Has AI avoided claiming Active or approved status?

---

## 22. Decision and Action

- Is the decision request explicit?
- Is the owner explicit?
- Is the deadline explicit?
- Are options comparable?
- Are criteria visible?
- Is the recommendation clear?
- Are trade-offs visible?
- Are risks visible?
- Is the consequence of delay visible?
- Are next steps operational?
- Does the artifact support actual action?

---

## 23. Brand Alignment

Does the presentation feel:

- Structured
- Intelligent
- Reliable
- Beautiful
- Minimal
- Sophisticated
- Human-centered
- Future-ready

Does it avoid:

- Decoration without meaning
- Flashiness without purpose
- Trend dependence
- Artificial futurism
- Density caused by lack of editing
- Minimalism that reduces understanding
- Confidence without evidence
- Efficiency at the expense of UX

---

## 24. Governance and Release

- Is version correct?
- Is lifecycle status correct?
- Is Owner a responsible role or person?
- Is Maintainer explicit?
- Are exceptions documented?
- Are approvals traceable?
- Are distribution and confidentiality correct?
- Is the delivered file the approved file?
- Is the archive location recorded?
- Are known limitations recorded?
- Is the artifact eligible for its claimed status?
- Has a Template, Component, or Pattern earned stable status through evidence?

---

## Severity

### P0

Blocks release or creates material risk.

Examples:

- Invented evidence
- Unreadable essential content
- Ambiguous decision
- Accessibility failure
- Incorrect approval status
- Platform conversion changes meaning
- Confidentiality breach

### P1

Material quality or governance issue requiring correction.

### P2

Improvement that does not block controlled release.

---

## Audit Report

```yaml
artifact:
version:
audit_mode: risk-based | full
auditor:
date:
categories_reviewed:
score:
p0_findings:
p1_findings:
p2_findings:
exceptions:
release_decision: approve | approve-with-exception | request-changes
owners:
due_dates:
evidence:
```

---

## Stable Promotion Evidence

To promote a Component, Pattern, Template, or System to stable / Active, attach:

- Implementation link or file
- Platform test record
- Accessibility test record
- Release Gate result
- Full Audit result
- Example
- Known limitations
- Change history
- Brand Director approval
