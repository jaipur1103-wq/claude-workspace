# ブランチ戦略

## 基本方針

| ブランチ | 用途 |
|---|---|
| `main` / `master` | 本番・デプロイ済みコード |
| `feature/[機能名]` | 新機能開発 |
| `fix/[バグ名]` | バグ修正 |

## 現在のブランチ

- Coron: `main`
- Speaq: `master`

## マージルール

- `main/master` への直接 push は OK（小規模プロジェクトのため）
- デプロイ前に必ず `npm run build` でビルドエラーを確認する
