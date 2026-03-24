# デプロイ手順

## 共通手順（Coron・Speaq）

```bash
npm run build          # ビルドエラーチェック（必須）
vercel --prod          # 本番デプロイ
git add -A
git commit -m "Deploy: [変更内容]"
git push origin main   # Coron
# git push origin master  # Speaq
```

## 注意事項

- **順序厳守**: vercel --prod → git push
- **ビルド確認必須**: エラーがある状態でデプロイしない
- `.env.local` は絶対にコミットしない（Vercel ダッシュボードで管理）

## 環境変数の管理場所

- Vercel ダッシュボード → プロジェクト → Settings → Environment Variables
- ローカルは `.env.local`（Git 管理外）
