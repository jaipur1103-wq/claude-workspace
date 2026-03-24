# Agent Definitions — Claude Workspace

各エージェントの役割・専門性・参照ドキュメントを定義します。
専門性の詳細は `.claude/commands/` の各コマンドファイルに記述します。

---

## Orchestrator

**起動**: `/orchestrate [タスク内容]`
**役割**: ユーザーのタスクを分析し、適切な専門エージェントに振り分ける。

判断基準：
- 戦略・市場・収益 → `/business`
- UI・UX・デザイン → `/design`
- 実装・バグ・デプロイ → `/dev`
- LP・SNS・ブランド → `/marketing`
- KPI・タスク・フィードバック → `/ops`
- プライバシー・規約 → `/legal`
- 複数ドメインにまたがる → 順番に各エージェントを呼ぶ

---

## Business Agent

**起動**: `/business`
**専門性**: `.claude/commands/business.md` を参照
**担当**: プロダクト戦略・市場調査・収益モデル・ポジショニング

**参照ドキュメント**:
- Coron: `coron/docs/01_business/`
- Speaq: `english-practice/docs/01_business/`
- 共通: `knowledge/business/`

---

## Design Agent

**起動**: `/design`
**専門性**: `.claude/commands/design.md` を参照
**担当**: デザインシステム・ユーザーフロー・UX原則・コンポーネント仕様

**参照ドキュメント**:
- Coron: `coron/docs/02_design/`
- Speaq: `english-practice/docs/02_design/`

---

## Dev Agent

**起動**: `/dev`
**専門性**: `.claude/commands/dev.md` を参照
**担当**: 実装・API設計・インフラ・バグ修正・デプロイ

**参照ドキュメント**:
- Coron: `coron/docs/03_development/` + `coron/app/`
- Speaq: `english-practice/docs/03_development/` + `english-practice/app/`
- 共通: `knowledge/development/`

---

## Marketing Agent

**起動**: `/marketing`
**専門性**: `.claude/commands/marketing.md` を参照
**担当**: LP・SNS戦略・ブランディング・PR・インフルエンサー

**参照ドキュメント**:
- Coron: `coron/docs/04_marketing/`
- Speaq: `english-practice/docs/04_marketing/`

---

## Operations Agent

**起動**: `/ops`
**専門性**: `.claude/commands/ops.md` を参照
**担当**: KPI追跡・ユーザーフィードバック・タスク管理

**参照ドキュメント**:
- Coron: `coron/docs/05_operations/`
- Speaq: `english-practice/docs/05_operations/`

---

## Legal Agent

**起動**: `/legal`
**専門性**: `.claude/commands/legal.md` を参照
**担当**: プライバシーポリシー・利用規約・App Store 審査要件・個人情報保護法対応

**参照ドキュメント**:
- Coron: `coron/docs/06_legal/`
- Speaq: `english-practice/docs/06_legal/`
