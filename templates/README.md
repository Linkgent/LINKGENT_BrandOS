# LINKGENT Brand OS Templates

## Purpose

`/templates`は、LINKGENT Brand OSで定義されたブランド判断を、再利用可能な実務形式として提供するためのディレクトリです。

ここに配置するテンプレートは、Brand OSの原則を置き換えたり、新しいブランドルールを独自に定義したりするものではありません。

テンプレートは、Brand Core、Brand Foundations、Applied Systems、AI Generation Rulesを具体的な制作形式へ実装した参照資産です。

## Position in the Brand OS

テンプレートは、以下の知識階層を継承します。

1. [`../CONSTITUTION.md`](../CONSTITUTION.md)
2. `../docs/01_Brand_Core.md`
3. 関連するBrand Foundations
4. 関連するApplied System
5. `../docs/13_AI_Generation_Rules.md`および媒体固有のAI生成ルール
6. 本ディレクトリ内のテンプレート

上位ルールとテンプレートが矛盾する場合は、上位ルールを優先します。

## Scope

将来的に、以下のような再利用可能資産を管理します。

- PowerPointテンプレート
- Word・Google Docs用テンプレート
- Web・UIのスターター構成
- Figma・Canva向けテンプレート
- Illustrator・Photoshop向け制作テンプレート
- AI生成用の構造化プロンプトまたは入力テンプレート
- 品質確認やレビューに使用するテンプレート

実際に追加するディレクトリやファイル形式は、Brand OSの成熟度と実務上の必要性に応じて定義します。

## Inclusion Criteria

`/templates`へ追加する資産は、以下を満たす必要があります。

- 繰り返し利用する明確な用途がある
- 対応する正本ルールを特定できる
- Brand Coreおよび関連システムと矛盾しない
- 単一案件だけに依存しすぎていない
- 利用者が目的、適用範囲、編集可能範囲を理解できる
- 人とAIの双方が再利用できる構造になっている
- バージョンや更新理由を追跡できる

## Template Principles

### Templates Implement Rules

テンプレートはルールの実装です。

色、文字、余白、コンポーネント、構成、表現方針を独自判断で固定せず、対応するBrand OS文書を参照します。

### Templates Are Starting Points

テンプレートは完成品ではなく、目的に応じた制作の出発点です。

内容や媒体特性に応じた調整は認めますが、上位ルールと情報設計の意図を損なってはいけません。

### Structure Before Decoration

再利用性を高めるため、テンプレートでは見た目だけでなく、情報階層、役割、編集単位、差し替え条件を明確にします。

### Medium-Aware Consistency

異なるツールのテンプレートを完全に同一の見た目へ固定しません。

各媒体の制約と利用文脈に合わせながら、ブランドの意味と品質基準を維持します。

## Required Documentation

各テンプレートまたはテンプレート群には、必要に応じて以下を記載します。

- Purpose
- Intended Users
- Supported Tools
- Source Rules
- Structure
- Editable Areas
- Fixed Areas
- Usage
- Do
- Don't
- Accessibility Notes
- AI Usage Notes
- Version

## Naming Guidance

テンプレート名は、ツール名だけでなく用途が分かる名前にします。

推奨例:

```text
presentation/
  proposal/
  business-review/

document/
  report/
  letterhead/

web/
  landing-page/
  dashboard/

ai/
  presentation-brief.md
  image-generation-brief.md
```

上記は将来構成の例であり、現時点での確定ディレクトリではありません。

## Current Status

現在、`/templates`には本READMEのみを配置しています。

個別テンプレートは、対応するBrand OS文書と利用要件が確定したものから順次追加します。
