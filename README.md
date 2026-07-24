# LINKGENT Brand OS

LINKGENT Brand OSは、LINKGENTのブランドシステム、デザインシステム、AI Knowledge Baseを統合管理するSingle Source of Truthです。

単なるブランドガイドではなく、PowerPoint、Web、Figma、Canva、Word、Illustrator、Photoshop、生成AIが共通して参照する基盤として運用します。

## Governance

リポジトリの最上位運用原則は[`CONSTITUTION.md`](./CONSTITUTION.md)に定義しています。

人・AI・接続ツールを問わず、ファイルを作成または更新する前に、必ず同ファイルを参照してください。

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

## Operating Rules

- GitHub上のMarkdownを唯一の正とする
- Brand OS全体との整合性を維持する
- 既存ファイルと関連ファイルを理解してから更新する
- ブランド思想や設計方針を勝手に変更しない
- MarkdownはGitHubへそのままコミットできる品質で作成する
- コミットメッセージにはConventional Commitsを使用する
- 重大な不明点は推測せず、Brand Directorへ確認する

## Roles

### Brand Director

ブランド方針、システム設計、レビュー、優先順位、重要な意思決定を担います。

### Repository Maintainer

関連ファイルの確認、Markdownの作成・更新、整合性確認、改善提案、GitHubへのコミットを担います。
