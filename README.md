# coding-agent-settings

コーディングエージェント向けのスキル・エージェント定義のベースです。

各プロジェクトにコピーして使い、そのプロジェクトに合わせて育てていくことを前提としています。

## 内容

### エージェント

| 名前 | 説明 |
|---|---|
| [code-review](agents/code-review.agent.md) | バグ・ロジック、セキュリティ、パフォーマンス、コード品質の観点でコードレビューを行う |

### スキル

#### 基本

どのプロジェクトでも使うことを想定したスキルです。

| 名前 | 説明 |
|---|---|
| [implementation-workflow](skills/implementation-workflow/SKILL.md) | 要件確認から調査、設計、実装、検証、仕上げまでの実装フロー |
| [unit-test](skills/unit-test/SKILL.md) | Arrange/Act/Assert 構造でのユニットテスト作成 |
| [git-commit](skills/git-commit/SKILL.md) | Conventional Commits 形式での安全なコミット |

#### オプション

必要なプロジェクトでのみ使うスキルです。

| 名前 | 説明 |
|---|---|
| [text-diagram](skills/text-diagram/SKILL.md) | 全角/半角混在を考慮したテキストでの図・表の描画 |

## 使い方

1. `agents/` と、基本スキルおよび必要なオプションスキルを、利用するエージェントが読み込む場所へコピーする
   - 例: Claude Code なら `.claude/agents/`, `.claude/skills/`
   - 例: GitHub Copilot なら `.github/agents/`, `.github/skills/`
2. プロジェクトの規約・構成に合わせて内容を調整する
3. 運用しながら改善する

## 運用方針

各ファイルには「必要時に更新する」というルールを入れています。
作業を通じて反復的に有効な改善点が見つかったら、コピー先のファイルを更新し、プロジェクトに即したものにしていきます。

プロジェクトを問わず有効な改善は、このリポジトリにも反映します。

## ライセンス

[MIT License](LICENSE)
