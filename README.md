# FFTPRS ワークショップ公式サイト

有限体理論とその擬似乱数系列生成への応用ワークショップ（FFTPRS）の公式サイトです。

## 概要

このサイトは、FFTPRSワークショップの情報を提供するためのJekyllベースのウェブサイトです。ワークショップの開催情報、プログラム、申し込み方法などを掲載しています。

## 技術スタック

- **静的サイトジェネレーター**: Jekyll
- **CSS フレームワーク**: Tailwind CSS
- **ホスティング**: GitHub Pages
- **コンテナ化**: Docker
- **言語**: HTML, CSS, JavaScript, Liquid (Jekyllテンプレート言語)

## プロジェクト構造

```
fftprsws_website/
├── _config.yml                 # Jekyll設定ファイル
│
├── _data/                      # データファイル
│   ├── workshops.yml           # ワークショップ一覧データ
│   └── workshop11.yml          # 第11回ワークショップ詳細データ
│   
├── _includes/                  # 共通コンポーネント
│   ├── header.html             # ヘッダー
│   ├── footer.html             # フッター
│   └── nav.html                # ナビゲーション
│
├── _layouts/                   # レイアウトテンプレート
│   ├── default.html            # デフォルトレイアウト
│   └── workshop.html           # ワークショップ専用レイアウト
├── _site/                      # ビルド出力ディレクトリ（自動生成）
│
├── assets/                     # 静的アセット
│   ├── css/
│   │   └── style.css           # カスタムCSS
│   ├── js/
│   │   └── main.js             # カスタムJavaScript
│   └── img/                    # 画像ファイル
│
├── pages/                      # ページファイル
│   ├── workshops.html          # ワークショップ一覧ページ
│   └── workshop11.html         # 第11回ワークショップページ
│    
├── index.md                    # トップページ
├── Gemfile                     # Ruby依存関係
├── Gemfile.lock                # 依存関係ロックファイル
└── robots.txt                  # 検索エンジン用ファイル

```

## セットアップ

### 前提条件

- **Docker Desktop**: 最新版をインストール済み
- **Git**: SSHキーが設定済み
- **GitHubアカウント**: SSHキーがGitHubに登録済み

### ローカル環境インストール手順

1. **リポジトリのクローン（SSH使用）**
```bash
git clone git@github.com:your-username/fftprsws_website.git
cd fftprsws_website
```

2. **DockerDesktopのビルドと起動**
```bash
docker run --rm -it -p 4000:4000 -v ${PWD}:/srv/jekyll jekyll/jekyll:4 jekyll serve --livereload
```

3. **ブラウザで確認**
```
http://localhost:4000
```


## 開発ガイド

### 新しいワークショップページの作成

新しいワークショップページを作成する場合は、[新しいページ作成手順書](./新しいページ作成手順書.md)を参照してください。

### データファイルの管理

#### ワークショップ一覧 (`_data/workshops.yml`)
```yaml
- title: "第〇〇回 有限体理論とその擬似乱数系列生成への応用ワークショップ"
  start_date: 2026-09-15
  end_date: 2026-09-16
  url: "/site/pages/workshop12/"
  status: "未定"
  location: "開催地説明"
```

#### ワークショップ詳細 (`_data/workshop{回数}.yml`)
```yaml
title: "第〇〇回 有限体理論とその擬似乱数系列生成への応用ワークショップ"
sponsored_by: "協賛名称"
executive_committee_member: "実行委員名（大学名）"
overview: "ワークショップの概要説明"
start_date: 2026-09-15
end_date: 2026-09-16
place: "開催場所名"
place_url: "https://example.com"
# ... その他の設定
```

### ページの追加

1. **データファイルの作成**: `_data/` ディレクトリにYAMLファイルを作成
2. **HTMLページの作成**: `pages/` ディレクトリにHTMLファイルを作成
3. **ナビゲーションの更新**: 必要に応じて `_includes/nav.html` を更新

### スタイルのカスタマイズ

- **Tailwind CSS**: ユーティリティファーストのCSSフレームワーク
- **カスタムCSS**: `assets/css/style.css` で追加スタイルを定義
- **レスポンシブデザイン**: モバイルファーストのアプローチ

## デプロイ

### GitHub Pages

このサイトはGitHub Pagesでホストされています。

1. **mainブランチにプッシュ（SSH使用）**
```bash
git add .
git commit -m "Update site content"
git push origin main
```

2. **自動デプロイ**
- GitHub Pagesが自動的にサイトをビルド・デプロイ
- 数分後に変更が反映されます

## メンテナンス

### 定期メンテナンス

1. **リンク切れの確認**
- 外部リンクの動作確認
- 内部リンクの動作確認

2. **コンテンツの更新**
- ワークショップ情報の更新
- プログラムの更新
- 申し込み情報の更新


## 開発フロー

未定
### コーディング規約

- **HTML**: セマンティックなマークアップ
- **CSS**: Tailwind CSSクラスの使用
- **JavaScript**: ES6+の使用
- **YAML**: 適切なインデントと構造
- **Docker**: マルチステージビルドの活用

## ライセンス

このプロジェクトの著作権はFFTPRSワークショップ実行委員会に帰属します。

## 連絡先

- **メール**: fftprs[at]googlegroups.com
- **GitHub**: [リポジトリのIssues](https://github.com/your-username/fftprsws_website/issues)


---

© 2025 FFTPRS Workshop. All rights reserved. 