# マルチエージェント設計

## このワークスペースのエージェント構成

```
Orchestrator（/orchestrate）
├── Business Agent（/business）
│   参照: docs/01_business/ + knowledge/business/
├── Dev Agent（/dev）
│   参照: docs/02_development/ + app/ + knowledge/development/
├── Marketing Agent（/marketing）
│   参照: docs/03_marketing/
└── Operations Agent（/ops）
    参照: docs/04_operations/
```

## 設計原則

- **専門性は commands/ に定義**（プロジェクト共通）
- **データは docs/ に保存**（プロジェクト別）
- 同じエージェントが対象プロジェクトに応じて参照先を切り替える
- 専門性（PERSONA）は各コマンドファイルの「専門性」セクションに後から追記できる

## エージェントの動かし方

```
/dev
→ 「Coron と Speaq どちら？」と会話で判断
→ 該当プロジェクトの docs/02_development/ とコードを参照して作業
```
