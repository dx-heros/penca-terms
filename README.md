# penca-terms

Penca（スタッフアプリ）の App Store 審査提出用に、利用規約・プライバシーポリシー・サポートページを GitHub Pages で公開するためのリポジトリです。

## ページ構成

| ファイル | 用途 | URL（公開後） |
|---|---|---|
| `index.html` | トップ（各ページへのリンク） | `https://dx-heros.github.io/penca-terms/` |
| `terms.html` | 利用規約 | `https://dx-heros.github.io/penca-terms/terms.html` |
| `privacy.html` | プライバシーポリシー | `https://dx-heros.github.io/penca-terms/privacy.html` |
| `support.html` | サポート・お問い合わせ | `https://dx-heros.github.io/penca-terms/support.html` |
| `style.css` | 共通スタイル | — |

## GitHub Pages の公開手順

1. GitHub の `dx-heros` 組織（または個人アカウント）配下に、`penca-terms` という名前の **public** リポジトリを作成する。
2. このディレクトリの中身をすべて push する。

   ```bash
   cd /Users/been10t/Projects/penca-terms
   git init
   git add .
   git commit -m "initial: terms / privacy / support pages for App Store review"
   git branch -M main
   git remote add origin git@github.com:dx-heros/penca-terms.git
   git push -u origin main
   ```

3. GitHub のリポジトリページで **Settings → Pages** を開く。
4. **Source** を `Deploy from a branch`、**Branch** を `main` / `/ (root)` に設定して保存。
5. 数十秒〜数分後に `https://dx-heros.github.io/penca-terms/` で公開される。

### カスタムドメイン（任意）

`dx-heros.com` のサブドメイン（例: `terms.dx-heros.com`）を使いたい場合：

1. リポジトリ直下に `CNAME` ファイルを作成し、中身を `terms.dx-heros.com` の 1 行のみにする。
2. ドメインの DNS に CNAME レコードを追加：
   - ホスト名: `terms`
   - 値: `dx-heros.github.io`
3. **Settings → Pages → Custom domain** に `terms.dx-heros.com` を入力。
4. **Enforce HTTPS** にチェック（証明書発行に数分〜1時間ほどかかる場合あり）。

## App Store 審査での使い方

App Store Connect の以下フィールドに、それぞれの URL を入力します。

- **App Privacy Policy URL** → `…/privacy.html`
- **License Agreement / Terms of Use URL**（任意） → `…/terms.html`
- **Support URL** → `…/support.html`
- **Marketing URL**（任意） → `…/`（トップ）

## メンテナンス

各ファイル冒頭の「最終更新日」と本文中の事業者名・連絡先は、内容を更新したら必ず合わせて変更してください。
