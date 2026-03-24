# PC移行手順

## 1. 必須ソフトウェアのインストール

```bash
# Node.js（公式サイトからLTS版をインストール）
# https://nodejs.org/

# Vercel CLI
npm install -g vercel

# Claude Code
npm install -g @anthropic-ai/claude-code
```

## 2. VSCode拡張のインストール

- Claude Code拡張（Anthropic）
- その他使用中の拡張はVSCodeの同期機能で自動移行

## 3. リポジトリのクローン

```bash
# 作業フォルダを作成
mkdir "Claude"
cd "Claude"

# 3リポジトリをクローン
git clone https://github.com/jaipur1103-wq/claude-workspace .
git clone https://github.com/jaipur1103-wq/coron coron
git clone https://github.com/jaipur1103-wq/speaq english-practice
```

## 4. 環境変数の設定（手動コピー必須）

以下のファイルはGitHubに上げていないため手動でコピーする：

### coron/.env.local
```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
ANTHROPIC_API_KEY=
```

### english-practice/.env.local
```
GROQ_API_KEY=
GEMINI_API_KEY=
```

> APIキーの値は旧PCの各 `.env.local` からコピーする。

## 5. 依存パッケージのインストール

```bash
cd coron
npm install

cd ../english-practice
npm install
```

## 6. Vercelの認証

```bash
vercel login
```

## 7. Claude Codeの設定

`.claude/settings.local.json` を旧PCからコピーする（APIキー等が含まれる場合）。

## 8. 動作確認

```bash
# Speaqのローカル起動確認
cd english-practice
npm run dev

# Coronのローカル起動確認
cd ../coron
npm run dev
```

## 注意事項

- `.env.local` は絶対にGitHubにコミットしない
- APIキーは旧PCから安全な方法でコピーする（メール・チャット不可）
- USBメモリか直接の有線接続で移行する
