# LINKGENT Brand OS

LINKGENT Brand OSは、LINKGENTのブランドシステム、デザインシステム、AI Knowledge Baseを統合管理するSingle Source of Truthです。

単なるブランドガイドではなく、PowerPoint、Web、Figma、Canva、Word、Illustrator、Photoshop、生成AIが共通して参照するブランド知識基盤として運用します。

## Repository Philosophy

### Brand OS, Not Brand Guidelines

このリポジトリの目的は、完成したルールを一覧化することではありません。

LINKGENTの思想から、情報設計、視覚表現、媒体別の適用、AIによる生成判断までを、相互に接続されたひとつのシステムとして管理することです。

### Decisions Before Deliverables

Brand OSが管理する中心対象は、個々の制作物ではなく、制作物を生み出すための判断基準です。

プレゼンテーション、Webページ、文書、画像、テンプレートなどの成果物は、Brand OSを適用した結果として扱います。

### One Meaning Across Many Tools

すべてのツールで同じ見た目を再現することではなく、異なる媒体や制作環境でも、同じブランド思想、意味、品質基準を維持することを目指します。

各ツール固有のルールは、共通のBrand CoreとBrand Foundationsを継承します。

### Human- and AI-Readable by Design

Brand OSは、人とAIが同じ知識を参照し、同じ根拠から判断できるように設計します。

曖昧な感覚だけに依存せず、目的、意味、適用範囲、条件、禁止事項、例外、参照関係を明示します。

### Living System, Stable Core

Brand OSは、事業、技術、媒体、制作環境の変化に応じて進化します。

一方で、Brand Coreや最上位原則を安易に変更せず、安定した中核の上に新しいシステムやテンプレートを拡張します。

### GitHub as the Knowledge Base

ブランドに関する恒久的な判断は、GitHub上の正本ファイルへ反映されて初めてBrand OSの正式な知識となります。

チャット、口頭、ローカルデータ、制作ツール上の設定は、正本へ反映されるまでは補助情報または派生実装として扱います。

## Governance

Brand OS全体の最上位原則、知識階層、継承、解釈、矛盾解消の基準は、[`CONSTITUTION.md`](./CONSTITUTION.md)に定義しています。

人・AI・接続ツールを問わず、ブランド知識を作成、更新、解釈、生成する前に、必ず同ファイルを参照してください。

リポジトリ操作やコミットに関する実務ルールは、本READMEおよび[`.github/copilot-instructions.md`](./.github/copilot-instructions.md)で補完します。

## Repository Structure

```text
LINKGENT_BrandOS/
│
├── README.md
│   └── リポジトリ全体の概要・思想・構成・運用ルール
│
├── CONSTITUTION.md
│   └── Brand OS全体の最上位原則・知識階層・解釈基準
│
├── .github/
│   └── copilot-instructions.md
│       └── GitHub CopilotおよびAIメンテナー向けの作業指示
│
├── templates/
│   ├── README.md
│   │   └── 再利用可能な実装テンプレートの目的・配置・管理ルール
│   └── presentation/
│       └── Presentation Systemを実装した媒体別テンプレート資産
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
    │   └── アイコンの意味・スタイル・アクセシビリティ・利用ルール
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
    │   │   └── Presentation Systemの目的・全体構成・ガバナンス・参照順
    │   │
    │   ├── Thinking.md
    │   │   └── Canonical Process / Content Architecture /
    │   │       Narrative Architecture / Slide Architecture
    │   │
    │   ├── Content.md
    │   │   └── タイトル・本文・数値・出典・脚注・引用・翻訳・Alt Text
    │   │
    │   ├── Layout.md
    │   │   └── Cross-platform presentation layout, grid, safe area,
    │   │       alignment, whitespace, density, and spatial rules
    │   │
    │   ├── Components.md
    │   │   └── Presentation内で再利用するsemantic componentと成熟度管理
    │   │
    │   ├── Patterns.md
    │   │   └── Problem / Insight / Decision / Comparison / Process等の
    │   │       Communication Pattern
    │   │
    │   ├── AI_Generation.md
    │   │   └── AI reasoning, specification, generation, adaptation,
    │   │       traceability, and validation across presentation platforms
    │   │
    │   ├── Accessibility.md
    │   │   └── 閲覧・登壇・変換・書き出しを含むPresentation accessibility
    │   │
    │   ├── Release_Gates.md
    │   │   └── すべての成果物に適用する必須リリースゲート
    │   │
    │   └── Audit_Checklist.md
    │       └── Risk-based Audit / Full Auditの詳細基準
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

## Knowledge Hierarchy

Brand OSの知識は、以下の順で継承されます。

1. Constitution
2. Brand Core
3. Brand Foundations
4. Applied Systems
5. AI Generation Rules
6. Templates
7. Generated Artifacts

下位の定義は上位の知識を継承し、矛盾させてはいけません。詳細な優先順位と解釈基準は[`CONSTITUTION.md`](./CONSTITUTION.md)を参照してください。

## Knowledge Lifecycle

Brand OSのドキュメントは、以下のLifecycleを使用します。

```text
Draft
  ↓
In Review
  ↓
Release Candidate
  ↓
Active
  ↓
Deprecated
  ↓
Archived
```

- **Draft**：作成中であり、正式レビュー前
- **In Review**：構造化されたレビュー中
- **Release Candidate**：思想と定義は完成しているが、実装・検証が未完了
- **Active**：承認・実装・検証が完了し、通常運用できる正本
- **Deprecated**：新規利用を停止し、移行期間中
- **Archived**：履歴として保存し、運用上は参照しない

`Git Ready`はLifecycleではなく、リポジトリ作業上の状態であるためStatusには使用しません。

## Ownership

- **Owner**：意味・方針・承認に責任を持つ役割または責任者
- **Maintainer**：正本の更新、整合性確認、履歴管理を担う役割または責任者

`LINKGENT Brand OS`のような知識体系そのものをOwnerとして指定しません。

## Operating Rules

- GitHub上のMarkdownを唯一の正とする
- Brand OS全体との整合性を維持する
- 既存ファイルと関連ファイルを理解してから更新する
- ブランド思想や設計方針を勝手に変更しない
- 同じ定義を複数ファイルへ無秩序に重複させない
- MarkdownはGitHubへそのままコミットできる品質で作成する
- コミットメッセージにはConventional Commitsを使用する
- 重大な不明点は推測せず、Brand Directorへ確認する

## Roles

### Brand Director

ブランド方針、システム設計、レビュー、優先順位、重要な意思決定を担います。

### Repository Maintainer

関連ファイルの確認、Markdownの作成・更新、整合性確認、改善提案、GitHubへのコミットを担います。
