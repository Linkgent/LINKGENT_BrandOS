# LINKGENT Brand OS Constitution

## 1. Purpose

この文書は、LINKGENT Brand OSを構成するすべてのブランド知識に共通する最上位原則を定義します。

LINKGENT Brand OSは、単なるブランドガイドラインではありません。

ブランドの思想、言語、視覚表現、デザイン判断、媒体別ルール、再利用可能なテンプレート、AIによる生成判断を、ひとつの知識体系として接続するためのBrand Knowledge Systemです。

本Constitutionの目的は、個別の制作物やツールが変わっても、LINKGENTらしさを一貫して理解・判断・再現できる状態を維持することです。

## 2. Constitutional Role

この文書は、個別の色、フォント、レイアウト、コンポーネント、テンプレートを直接定義するものではありません。

本Constitutionが定義するのは、以下です。

- Brand OSが何を正とするか
- ブランド知識をどのような階層で管理するか
- 上位概念を下位システムへどのように継承するか
- ファイル間の矛盾をどのように扱うか
- 人とAIがブランド知識をどのように解釈するか
- 新しい媒体・ツール・表現をどのようにBrand OSへ接続するか

Mission、Vision、Value、Personality、Tone & Voiceなどのブランド固有定義は、[`docs/01_Brand_Core.md`](./docs/01_Brand_Core.md)を正本とします。

## 3. Definition of Brand OS

LINKGENT Brand OSは、以下を統合する唯一のブランド知識基盤です。

- Brand System
- Design System
- Content and Communication Principles
- Channel-specific Systems
- Reusable Templates
- AI Knowledge Base
- Generation and Quality Rules

PowerPoint、Web、Figma、Canva、Word、Illustrator、Photoshop、生成AIなどは、それぞれ独立したブランドルールを持つのではなく、Brand OSの知識を媒体に応じて継承・適用します。

## 4. Single Source of Truth

GitHub上のMarkdownを、LINKGENT Brand OSにおける唯一の正とします。

ブランドに関する判断が、チャット、口頭、ローカルファイル、デザインデータ、過去の制作物のみに存在する場合、それはまだ正式なBrand OSではありません。

恒久的に参照すべき判断は、適切な正本ファイルへ反映されて初めてBrand OSの知識となります。

外部ツール上のスタイル、コンポーネント、テンプレート、プロンプトは、GitHub上の定義を実装した派生物として扱います。

## 5. Knowledge Architecture

Brand OSの知識は、以下の階層で構成します。

### Level 0: Constitution

Brand OS全体に共通する最上位原則、知識階層、継承、解釈、矛盾解消の基準を定義します。

- `CONSTITUTION.md`

### Level 1: Brand Core

LINKGENTが何者であり、何を目指し、どのように振る舞うかを定義します。

- Mission
- Vision
- Value
- Personality
- Tone & Voice
- Brand Promise
- Brand Story
- Design Philosophy

Canonical source:

- `docs/01_Brand_Core.md`

### Level 2: Brand Foundations

ブランド表現を構成する共通基盤を定義します。

- Visual Identity
- Color
- Typography
- Design Tokens
- Iconography
- Photography
- Illustration
- Layout

Canonical sources:

- `docs/02_Visual_Identity.md`
- `docs/03_Color_System.md`
- `docs/04_Typography.md`
- `docs/05_Design_Tokens.md`
- `docs/06_Iconography.md`
- `docs/07_Photography.md`
- `docs/08_Illustration.md`
- `docs/09_Layout_System.md`

### Level 3: Applied Systems

共通基盤を特定の媒体・制作環境へ適用するルールを定義します。

- Presentation System
- Web System
- Document System

Canonical sources:

- `docs/10_Presentation_System/`
- `docs/11_Web_System.md`
- `docs/12_Document_System.md`

### Level 4: AI Generation Rules

AIがBrand OSを読み取り、判断し、生成し、検証するときの共通ルールを定義します。

Canonical source:

- `docs/13_AI_Generation_Rules.md`

媒体固有のAI生成ルールは、各Applied Systemの中で共通ルールを拡張します。

### Level 5: Templates

Brand OSの判断を、再利用可能な実務形式として具体化します。

Canonical location:

- `templates/`

テンプレートは新しいブランド原則を定義する場所ではありません。上位のBrand Core、Brand Foundations、Applied Systemsを実装した参照例です。

### Level 6: Generated Artifacts

プレゼンテーション、Webページ、文書、画像、デザインデータなどの成果物です。

成果物はBrand OSの適用結果であり、Brand OSそのものではありません。

## 6. Precedence of Knowledge

ブランド知識が競合する場合、以下の優先順位を適用します。

1. `CONSTITUTION.md`
2. `docs/01_Brand_Core.md`
3. 共通のBrand Foundations
4. 媒体別のApplied Systems
5. `docs/13_AI_Generation_Rules.md`および媒体固有のAI生成ルール
6. `templates/`
7. 過去の成果物・実装データ

同一階層内では、対象をより具体的に定義する正本ファイルを優先します。ただし、具体的な定義が上位原則と矛盾する場合は、上位原則を優先します。

一時的な指示や個別案件の要望は、その案件では有効でも、自動的にBrand OS全体の定義にはなりません。

## 7. Core Knowledge Principles

### 7.1 Intent Before Expression

見た目や表現手段を決める前に、目的、対象者、伝えるべき内容、期待する行動を明確にします。

ブランド表現は、意図を価値へ変換するための手段です。

### 7.2 System Before Instance

単一の制作物だけを最適化するのではなく、再現性、拡張性、他媒体との整合性を持つ仕組みとして判断します。

例外を作る場合は、なぜ例外が必要かを説明できなければなりません。

### 7.3 Semantics Before Decoration

色、余白、タイポグラフィ、アイコン、図版、コンポーネントは、意味や情報構造を明確にするために使用します。

装飾を目的として、情報階層や理解を損なってはいけません。

### 7.4 Consistency Without Uniformity

すべての媒体を同じ見た目に固定することを、一貫性とは呼びません。

ブランドの思想、意味、品質基準を共有しながら、媒体特性、利用文脈、ユーザー行動に応じて適切に表現を変えます。

### 7.5 Accessibility Is Brand Quality

可読性、視認性、理解可能性、操作可能性は、追加要件ではなくブランド品質の一部です。

美しさを理由に、情報アクセスを損なってはいけません。

### 7.6 Human and AI Parity

Brand OSは、人だけでなくAIも同じ意味で解釈できる必要があります。

定義は、曖昧な感覚語だけに依存せず、目的、条件、適用範囲、禁止事項、例外、参照先を明示します。

### 7.7 Traceable Decisions

重要なブランド判断は、どの上位原則から導かれたかを追跡できる状態にします。

定義、派生ルール、テンプレート、成果物の関係を切断してはいけません。

### 7.8 Living System, Stable Core

Brand OSは固定された完成品ではなく、事業、技術、媒体、利用状況の変化に応じて進化する知識体系です。

ただし、変化のたびにBrand Coreや最上位原則を安易に書き換えてはいけません。拡張で対応できるものと、憲法改定が必要なものを区別します。

## 8. Inheritance and Extension

下位システムは、上位システムを継承します。

- Applied SystemsはBrand CoreとBrand Foundationsを継承する
- AI Generation RulesはBrand Core、Brand Foundations、Applied Systemsを解釈する
- Templatesは上位ルールを具体的な形式へ実装する
- Generated Artifactsは適切なテンプレートとルールを利用する

下位ファイルは、上位ファイルの内容を無断で再定義してはいけません。

媒体固有の条件により追加ルールが必要な場合は、上位ルールを否定するのではなく、適用条件を限定した拡張として定義します。

## 9. Canonical Ownership

各ブランド知識には、ひとつのCanonical Ownerを設定します。

同じ定義を複数ファイルへ完全に複製するのではなく、正本をひとつに定め、他のファイルから参照します。

例:

- ブランド人格は`01_Brand_Core.md`
- 色の意味と利用基準は`03_Color_System.md`
- 文字サイズや階層は`04_Typography.md`
- 共通スペーシング値は`05_Design_Tokens.md`
- PowerPointでの余白適用は`10_Presentation_System/Layout.md`
- AI共通の解釈規則は`13_AI_Generation_Rules.md`

ファイル間で同じ概念を扱う場合は、以下を明確にします。

- どのファイルが定義元か
- どのファイルが適用・拡張を担当するか
- どの条件で例外が認められるか

## 10. Brand Knowledge States

AIおよびメンテナーは、ブランド知識を以下の状態に区別します。

### Defined

正本ファイルに明示されている確定知識。

### Derived

複数の確定知識から論理的に導ける判断。根拠となるファイルを説明できる必要があります。

### Proposed

Brand OS改善のための提案。正式に採用され、正本へ反映されるまでは確定知識として扱いません。

### Unknown

Brand OS内に根拠がなく、推測が必要な状態。

重大な判断がUnknownの場合、AIはもっともらしいルールを捏造してはいけません。

## 11. AI Interpretation Principles

AIはBrand OSを利用するとき、以下を守ります。

- 作業対象だけでなく、上位のBrand Coreと関連する共通ルールを確認する
- 明示された定義と、AIによる推論を区別する
- 未定義事項を既存ルールのように断定しない
- ブランド思想を一般的なデザイントレンドで上書きしない
- 媒体固有のルールをBrand OS全体の原則へ昇格させない
- 過去の成果物だけを根拠に新しいブランドルールを作らない
- 生成時には適用した主要ルールを追跡できる状態にする
- 矛盾や重大な不足がある場合は、Brand Directorへ判断を求める

## 12. Evolution of the Brand OS

Brand OSの変更は、以下の3種類に分類します。

### Interpretation

既存の定義を変更せず、適用方法や具体例を明確にする変更。

### Extension

新しい媒体、コンポーネント、テンプレート、AI利用方法などを追加する変更。上位原則を継承している必要があります。

### Amendment

Brand Core、知識階層、最上位原則などを変更する変更。

AmendmentはBrand OS全体へ影響するため、Brand Directorによる明示的な判断を必要とします。

## 13. Role of the Brand Director

Brand Directorは、Brand OSの方向性と最終的な意味を統治します。

主な責任は以下です。

- Brand Coreの承認と改定
- ブランド知識間の重大な矛盾の解決
- 新しい原則をBrand OSへ採用するかの判断
- 表現品質と事業価値の両面からのレビュー
- Interpretation、Extension、Amendmentの境界判断

AIおよびメンテナーは、Brand Directorの判断を再現可能な知識としてBrand OSへ構造化します。

## 14. Constitutional Compliance

Brand OSに準拠した定義・テンプレート・成果物は、以下を満たします。

- Brand Coreとのつながりを説明できる
- 正本となるルールを特定できる
- 関連ファイルと矛盾していない
- 情報構造と表現の意図が一致している
- 媒体特性を考慮しながら、ブランドの意味を保持している
- 人とAIの双方が再利用できる
- 未定義事項を確定ルールとして偽装していない
- 将来の拡張を妨げる不必要な固定化をしていない

## 15. Constitutional Principle

LINKGENT Brand OSは、ブランド表現を固定するための規則集ではありません。

ブランドの思想を、異なる媒体、異なる人、異なるAIが、同じ意味と品質で判断・再現できるようにするための知識基盤です。

すべての定義、システム、テンプレート、成果物は、この目的に従います。
