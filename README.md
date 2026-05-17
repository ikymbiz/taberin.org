# ddashpot — あれるぎーと暮らす手帖（公開サイト一式）

アレルギー・健康ジャンルのアフィリエイト審査通過用サイト。サーバーにアップロードして公開する側のファイルです。

> 記事を作成・編集するためのadminツールは、**別パッケージ（ddashpot-admin）**として配布されています。adminツールはお手元のPCで動かし、生成された記事HTMLだけをサーバーにアップロードする運用です。

## 構成

```
ddashpot-site/
├── index.html              トップページ
├── about.html              運営者情報
├── contact.html            お問い合わせ
├── privacy.html            プライバシーポリシー
├── disclaimer.html         免責事項
├── sitemap.xml             サイトマップ
├── robots.txt              クローラー設定
│
├── css/style.css           共通スタイルシート
│
└── articles/               記事10本
    ├── first-allergy-test.html
    ├── recommended-books.html
    ├── allergy-friendly-snacks.html
    ├── egg-free-pancake.html
    ├── plant-based-milk.html
    ├── kids-eating-out.html
    ├── rice-flour-okonomiyaki.html
    ├── gluten-free-seasoning.html
    ├── pollen-season.html
    └── emergency-stock.html
```

## デプロイ方法

1. ZIPを解凍
2. `ddashpot-site` フォルダ内のファイルを、サーバーのドキュメントルートにFTPなどでアップロード
3. `https://ddashpot.com/` で表示確認
4. Google Search Consoleでサイトを登録、`sitemap.xml` を送信

## 公開前のチェックリスト

- [ ] `about.html` の運営者名、開設日を実情報に差し替え
- [ ] お問い合わせフォームをFormspree等の実働サービスに接続（現状はダミー）
- [ ] Google Analytics / Search Console のタグを `<head>` 内に追加
- [ ] スマホ表示の確認
- [ ] 全リンクの動作確認

## 新規記事を追加する流れ

1. お手元のPCでadminツール（`ddashpot-admin`）を起動して記事を作成
2. adminツールから記事HTMLをダウンロード
3. ダウンロードしたファイルを `articles/` フォルダにFTPアップロード
4. adminツールが生成する「トップページ用カードHTML」を、サーバー上の `index.html` に追記
5. `sitemap.xml` に新記事のURLを追記

詳細はadminパッケージ側のREADMEを参照してください。

## ASP申請順のおすすめ

1. A8.net（即時登録、慣れる）
2. 楽天アフィリエイト（通りやすい）
3. もしもアフィリエイト
4. Amazonアソシエイト（記事10本＋運用実績で申請）
5. i-mobile / 忍者AdMax

## 健康ジャンルでの記事執筆ガイドライン

NGワード：「治る」「効く」「予防できる」などの医療効能の断定。

OKな表現スタンス：「私の場合は」「主治医と相談した結果」「症状が気になる方は専門医を受診」など、体験ベース・情報案内に徹する。
