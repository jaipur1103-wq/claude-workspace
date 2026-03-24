# /orchestrate — タスク振り分けコマンド

$ARGUMENTS に記載されたタスクを分析し、最適な専門エージェントに振り分けます。

## 手順

1. タスクの対象プロジェクトを特定する（Coron / Speaq / 両方 / 不明）
2. タスクのドメインを判断する
3. 対応するエージェントと参照先を宣言する
4. そのエージェントとして作業を開始する

## 判断基準

| キーワード | エージェント |
|---|---|
| 戦略, 市場, 収益, ペルソナ, 競合 | `/business` |
| 実装, コード, バグ, API, デプロイ, ビルド | `/dev` |
| LP, SNS, ブランド, PR, コピー | `/marketing` |
| KPI, フィードバック, タスク, 進捗 | `/ops` |
| 複数ドメイン | 必要なエージェントを順番に起動 |

## 使用例

```
/orchestrate Coronのロードマップを作りたい
→ Dev Agent として作業します
→ 参照: coron/docs/02_development/ROADMAP.md

/orchestrate SpeaqのSNS戦略を考えたい
→ Marketing Agent として作業します
→ 参照: english-practice/docs/03_marketing/sns-strategy.md
```
