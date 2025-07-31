# ラムネの日々 🐱

オフィス猫「ラムネ」の日常を綴ったブログサイトです。

## 概要

このサイトは、オフィスで働くかわいい猫「ラムネ」の日常生活を写真と文章で紹介しています。Hugo静的サイトジェネレーターを使用して構築され、GitHub Pagesでホストされています。

🌐 **サイトURL**: https://luckofwise.github.io/cat-blog/

## 特徴

- 📸 インスタグラム風の写真グリッドレイアウト
- 📱 レスポンシブデザイン（スマートフォン・タブレット・デスクトップ対応）
- 🎌 日本語コンテンツ
- 🚀 高速な静的サイト（Hugo使用）
- 📄 ページネーション機能

## 技術スタック

- **静的サイトジェネレーター**: Hugo v0.148.2+
- **テーマ**: Ananke（カスタマイズ済み）
- **ホスティング**: GitHub Pages
- **言語**: 日本語

## 開発環境の構築

### 必要なソフトウェア

- Hugo v0.148.2以降（拡張版）
- Git

### セットアップ

1. リポジトリをクローン
```bash
git clone https://github.com/luckofwise/cat-blog.git
cd cat-blog
```

2. 開発サーバーを起動
```bash
hugo server -D
```

3. ブラウザで http://localhost:1313 にアクセス

### サイトのビルド

本番用のサイトを生成する場合：

```bash
hugo
```

生成されたファイルは `public/` ディレクトリに出力されます。

## コンテンツの追加

### 新しい投稿の作成

1. `content/posts/` ディレクトリに新しいMarkdownファイルを作成
2. ファイル名の形式: `post-YYYY-MM-DDTHH-MM-SS.md`
3. フロントマターの例：

```yaml
---
title: "投稿のタイトル"
date: 2025-07-31
draft: false
---
```

### 画像の追加

1. `static/images/` ディレクトリに画像ファイルを配置
2. ファイル名の形式: `cat-YYYY-MM-DDTHH-MM-SS.jpg`
3. 投稿内で画像を参照: `![説明文](/images/filename.jpg)`

## サイト構成

```
cat-blog/
├── content/posts/          # ブログ投稿
├── static/images/          # 画像ファイル
├── layouts/               # カスタムレイアウト
├── themes/ananke/         # テーマファイル
├── hugo.toml             # サイト設定
└── public/               # 生成されたサイト（自動生成）
```

## カスタマイズ

### 写真グリッドレイアウト

`layouts/index.html` でインスタグラム風のグリッドレイアウトを実装しています：

- 各投稿の最初の画像を自動抽出
- レスポンシブデザイン
- ホバーエフェクト
- ページネーション

### サイト設定

`hugo.toml` での主要な設定：

- `baseURL`: GitHub PagesのURL
- `languageCode`: "ja-jp"（日本語）
- `title`: "ラムネの日々"
- `paginate`: 36（グリッド表示の投稿数）

## デプロイ

このサイトはGitHub Pagesに自動デプロイされます。`main` ブランチにプッシュすると、自動的にサイトが更新されます。

## ライセンス

このプロジェクトは個人ブログとして作成されています。

---

🐾 ラムネの可愛い日常をお楽しみください！