# LINKGENT Brand OS Repository Constitution

## Status

This document is the governing constitution for the `Linkgent/LINKGENT_BrandOS` repository.

All maintainers, contributors, AI assistants, and connected tools must treat this file as the highest-priority operational guidance for repository changes, unless an explicit repository owner instruction overrides it.

## Mission

Maintain and evolve LINKGENT Brand OS as the single source of truth for LINKGENT's brand system, design system, and AI knowledge base.

This repository is not merely a brand guideline. It is the shared operating system referenced by:

- PowerPoint
- Web
- Figma
- Canva
- Word
- Illustrator
- Photoshop
- Generative AI

## Core Principles

1. **Single Source of Truth**  
   GitHub-hosted Markdown in this repository is the authoritative source.

2. **System Consistency First**  
   Prioritize consistency across the entire Brand OS over optimization of a single file.

3. **Do Not Rewrite the Brand Arbitrarily**  
   Do not change LINKGENT's brand philosophy, terminology, design principles, or system architecture without an explicit instruction.

4. **Understand Before Editing**  
   Review the target file and all materially related files before creating or updating content.

5. **Human- and AI-Readable Structure**  
   Maintain content that is clear, structured, searchable, and reusable by both people and AI systems.

6. **Tool-Agnostic Rules**  
   Define principles at the Brand OS level whenever possible. Tool-specific rules should extend shared principles rather than contradict them.

7. **GitHub-Ready Quality**  
   Markdown must be complete, internally consistent, readable in GitHub, and ready to commit without additional cleanup.

## Repository Structure

```text
LINKGENT_BrandOS/
│
├── README.md
│   └── リポジトリ全体の概要・目的・構成・運用ルール
│
├── CONSTITUTION.md
│   └── AI・メンテナー向けの最上位運用原則
│
├── .github/
│   └── copilot-instructions.md
│       └── GitHub CopilotがCONSTITUTION.mdを参照するための入口
│
└── docs/
    │
    ├── 01_Brand_Core.md
    │   └── Mission / Vision / Value / Personality / Tone & Voice
    │
    ├── 02_Visual_Identity.md
    │   └── ロゴ・VI・ブランド表現の基本方針
    │
    ├── 03_Color_System.md
    │   └── Corporate Color / Semantic Color / 印刷・デジタル利用ルール
    │
    ├── 04_Typography.md
    │   └── フォント・階層・スケール・利用ルール
    │
    ├── 05_Design_Tokens.md
    │   └── Color / Spacing / Radius / Shadow / Stroke / Grid
    │
    ├── 06_Iconography.md
    │   └── Material Symbols Outlinedの利用ルール
    │
    ├── 07_Photography.md
    │   └── 写真・撮影・AI生成写真のルール
    │
    ├── 08_Illustration.md
    │   └── イラストのスタイル・利用・禁止事項
    │
    ├── 09_Layout_System.md
    │   └── Grid / Alignment / Whitespace / Container
    │
    ├── 10_Presentation_System/
    │   │
    │   ├── README.md
    │   │   └── Presentation Systemの目的・全体構成・参照順
    │   │
    │   ├── Thinking.md
    │   │   └── Presentation Thinking / Audience First /
    │   │       Information Architecture / Information Density
    │   │
    │   ├── Layout.md
    │   │   └── PowerPointのグリッド・余白・整列・情報配置
    │   │
    │   ├── Components.md
    │   │   └── Title / Card / Callout / Table / Chart /
    │   │       Timeline / KPI / Process / Comparison
    │   │
    │   ├── Templates.md
    │   │   └── 表紙・課題・提案・比較・ロードマップ・まとめ等
    │   │
    │   ├── AI_Generation.md
    │   │   └── AIがPowerPointを生成するときの判断・生成ルール
    │   │
    │   └── Checklist.md
    │       └── 生成後・納品前の品質確認
    │
    ├── 11_Web_System.md
    │   └── Webでのブランド・UI・コンポーネント利用ルール
    │
    ├── 12_Document_System.md
    │   └── Word・Google Docs・帳票・名刺等の文書ルール
    │
    └── 13_AI_Generation_Rules.md
        └── 複数AI・制作ツール共通のブランド生成ルール
```

## Change Rules

- Confirm the existing repository structure before creating a file.
- Read the target file before updating it.
- Review related files when terminology, tokens, visual rules, layouts, components, or AI behavior may overlap.
- Preserve established naming, hierarchy, and terminology.
- Do not duplicate rules across files without a clear ownership boundary.
- Prefer references between files over conflicting repeated definitions.
- State assumptions explicitly when minor interpretation is unavoidable.
- Ask the Brand Director when an unresolved question could materially change the system.
- Use Conventional Commits.
- Write commit messages that make the reason for the change understandable.

## Conventional Commit Guidance

Use one of the following patterns as appropriate:

```text
docs: add color system

docs(presentation): update layout rules

fix(docs): resolve conflicting typography definitions

refactor(brand-os): consolidate duplicated AI guidance

chore(repo): add repository maintenance instructions
```

## Standard Workflow

When the Brand Director requests a file creation or update:

1. Inspect the repository structure.
2. Read the target file if it exists.
3. Read materially related Brand OS files.
4. Identify dependencies, overlaps, and conflicts.
5. Create or update Markdown at GitHub-ready quality.
6. Verify consistency with the full Brand OS.
7. Commit the change using Conventional Commits.
8. Report what changed, why, and any remaining decisions.

## Role Model

### Brand Director

The repository owner acts as Brand Director and is responsible for:

- brand direction
- system-level review
- approving major conceptual changes
- resolving ambiguous design decisions
- prioritizing improvements

### Repository Maintainer

The dedicated maintainer or AI assistant is responsible for:

- inspecting related files
- maintaining structural consistency
- drafting and editing Markdown
- identifying conflicts and missing definitions
- proposing improvements without silently changing philosophy
- committing approved work to GitHub

## Conflict Resolution

When rules conflict, apply the following priority order:

1. Explicit instruction from the Brand Director for the current task
2. This `CONSTITUTION.md`
3. Repository-level definitions in `README.md`
4. Cross-system rules in `docs/`
5. Tool-specific guidance

Do not resolve material contradictions silently. Surface them before changing the governing definition.

## Definition of Done

A repository change is complete only when:

- the target content is accurate and complete
- related files remain consistent
- terminology and hierarchy are preserved
- Markdown renders correctly on GitHub
- humans and AI can understand the rule
- the commit message follows Conventional Commits
- the change reason is traceable
