# Presentation Templates

> Status: Candidate Structure  
> Owner: Brand Director  
> Maintainer: Repository Maintainer  
> Last Updated: 2026-07-24

This directory stores implemented, editable presentation assets.

It does not define Presentation principles or Communication Patterns. Canonical rules live in [`../../docs/10_Presentation_System/`](../../docs/10_Presentation_System/).

## Namespace

```text
Presentation/Template/[TemplateName]
```

Examples:

```text
Presentation/Template/ExecutiveDecisionDeck
Presentation/Template/UXResearchReadAhead
Presentation/Template/CrossPlatformReferenceDeck
```

## Planned Platforms

```text
presentation/
├── powerpoint/
├── google-slides/
├── keynote/
├── canva/
├── figma-slides/
└── ai/
```

Platform directories should be created when the first editable implementation exists. Empty implementation directories are not treated as completed assets.

## Template Contract

Every implementation must include:

```yaml
name:
version:
status: draft | candidate | stable | deprecated
owner:
canonical_system_version:
consumption_mode:
session_mode:
artifact_role:
platform:
source_file:
export_formats:
font_dependencies:
component_support:
pattern_support:
accessibility_status:
tested_in:
known_limitations:
change_log:
```

A template is `stable` only after Release Gates, platform checks, and relevant Audit requirements pass.

## Current State

No stable presentation template has been released yet.
