# Git ワークフロー

## このワークスペースの Git 構成（3リポジトリ）

```
Claude/（claude-workspace）← knowledge/ .claude/commands/ CLAUDE.md AGENTS.md のみ管理
├── .gitignore（coron/ english-practice/ を除外）
│
coron/（jaipur1103-wq/coron）← 独立リポジトリ
english-practice/（jaipur1103-wq/speaq）← 独立リポジトリ
```

## コミット手順

### ワークスペースルート（claude-workspace）

```bash
cd "C:\Users\Shuji Miura\OneDrive\デスクトップ\Claude"
git add CLAUDE.md AGENTS.md .claude/commands/ knowledge/
git commit -m "Update workspace: [変更内容]"
git push origin main
```

### Coron

```bash
cd coron
git add -A
git commit -m "[変更内容]"
git push origin main
```

### Speaq

```bash
cd english-practice
git add -A
git commit -m "[変更内容]"
git push origin master
```

## デプロイルール（全プロジェクト共通・例外なし）

1. 実装完了後は必ず以下の順で行う：
   ```
   npm run build  （エラーがないか確認）
   vercel --prod  （本番デプロイ）
   git add
   git commit
   git push
   ```
2. **コミット・Pushなしで作業を終了してはいけない**
3. `.env.local` は絶対にコミットしない

## 注意事項

- Coron は `main` ブランチ、Speaq は `master` ブランチ
- `.env.local` は絶対にコミットしない
- デプロイは `vercel --prod` → `git push` の順を毎回厳守する
