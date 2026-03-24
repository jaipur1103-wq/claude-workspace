# Claude Code — 使い方・ベストプラクティス

## 起動方法

```bash
# ワークスペースルート（オーケストレーターとして起動）
cd "C:\Users\Shuji Miura\OneDrive\デスクトップ\Claude"
claude --dangerously-skip-permissions

# Coron プロジェクト
cd "C:\Users\Shuji Miura\OneDrive\デスクトップ\Claude\coron"
claude --dangerously-skip-permissions

# Speaq プロジェクト
cd "C:\Users\Shuji Miura\OneDrive\デスクトップ\Claude\english-practice"
claude --dangerously-skip-permissions
```

## CLAUDE.md の役割

- セッション開始時に自動読み込みされる
- プロジェクトのルール・禁止事項・重要コンテキストを記載する
- `@AGENTS.md` で他ファイルを参照読み込みできる

## AGENTS.md の役割

- 各エージェントの役割・参照ドキュメント・担当範囲を定義する
- 自動実行はしない（コンテキストの提供が目的）

## カスタムスラッシュコマンド

`.claude/commands/[name].md` を作成すると `/name` で呼び出せる。
`$ARGUMENTS` で引数を受け取れる。

## このワークスペースのコマンド

| コマンド | 内容 |
|---|---|
| `/orchestrate` | タスクを分析して専門エージェントに振り分け |
| `/business` | Business Agent として起動 |
| `/dev` | Dev Agent として起動 |
| `/marketing` | Marketing Agent として起動 |
| `/ops` | Operations Agent として起動 |
