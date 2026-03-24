# Claude Workspace — オーケストレーター

このディレクトリはマルチプロジェクト・ドメイン専門エージェントのワークスペースです。
ここから Claude Code を起動した場合、**Orchestrator** として動作します。

## プロジェクト一覧

| プロジェクト | ディレクトリ | GitHub |
|---|---|---|
| Coron（がん患者向けアプリ） | `./coron/` | https://github.com/jaipur1103-wq/coron |
| Speaq（英語練習アプリ） | `./english-practice/` | https://github.com/jaipur1103-wq/speaq |

## エージェント構成

詳細は `AGENTS.md` を参照。

| コマンド | 専門領域 | 参照先 |
|---|---|---|
| `/orchestrate` | タスク分析・振り分け | AGENTS.md |
| `/business` | 戦略・市場・収益 | docs/01_business/ |
| `/design` | UI/UX・デザインシステム | docs/02_design/ |
| `/dev` | 実装・API・インフラ | docs/03_development/ + app/ |
| `/marketing` | LP・SNS・ブランディング | docs/04_marketing/ |
| `/ops` | KPI・フィードバック・タスク | docs/05_operations/ |
| `/legal` | プライバシー・利用規約 | docs/06_legal/ |

## ナレッジベース

プロジェクト横断の汎用知識は `./knowledge/` に格納。

## Git 構成

- このリポジトリ（claude-workspace）: CLAUDE.md, AGENTS.md, .claude/commands/, knowledge/ のみ管理
- `coron/` と `english-practice/` は独立した Git リポジトリ（.gitignore で除外）
