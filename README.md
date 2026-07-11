# CRYSTAL NEON

「水晶」と「ネオン」をテーマにした、黒ベース・水色ハイライトの静的サイトテンプレートです。
GitHub Pages でそのまま公開できる構成になっています。

## 特徴

- 漆黒の背景に浮かぶ多面体クリスタルと、水色ネオンの発光表現
- Canvas によるパーティクル背景（`prefers-reduced-motion` 対応）
- スクロール連動のフェードインアニメーション
- レスポンシブ対応（モバイル用ハンバーガーナビ）
- 依存パッケージなし、ビルド不要のプレーン HTML/CSS/JS

## 構成

```
.
├── index.html          # トップページ
├── 404.html            # 404 エラーページ
├── assets/
│   ├── css/style.css   # スタイル一式
│   ├── js/main.js      # ナビ・スクロール演出・パーティクル背景
│   └── img/            # 画像用（現在は空）
└── README.md
```

## ローカルで確認する

ビルド不要です。任意の静的サーバーで配信してください。

```bash
# 例: Python
python -m http.server 8000

# 例: Node (npx)
npx serve .
```

`http://localhost:8000` にアクセスして確認できます。

## GitHub Pages への公開

このリポジトリが `<username>.github.io` という名前であれば、`main` ブランチに push するだけで
`https://<username>.github.io/` として公開されます。

別名のリポジトリの場合は、GitHub の **Settings → Pages** で公開ブランチ（`main` など）と
ルートディレクトリ（`/`）を指定してください。

```bash
git init
git add .
git commit -m "feat: initial crystal neon site"
git branch -M main
git remote add origin <このリポジトリのURL>
git push -u origin main
```

## カスタマイズ

- 配色: [assets/css/style.css](assets/css/style.css) 冒頭の `:root` 内 CSS 変数（`--bg` / `--cyan` など）を変更
- テキスト・リンク: [index.html](index.html) 内の各セクションを編集
- Works セクションのサムネイル色: `.work-thumb` の `style="--hue:190"` を数値変更

## ライセンス

特に指定がない場合は自由に改変・利用してください。
