# PLUG 01 — 販売LP

Claude に差し込むプラグイン一式「PLUG 01 ／ つくる道具一式」の販売サイト。500円の買い切り。
運営ブランドは **FORGE**／販売事業者は **AIクリエイター**。静的HTML（ビルド不要）。

2026-09-08 に `artigia` リポジトリ（AI Creator Camp）から分離した。
事業ごとにリポジトリとVercelプロジェクトを分ける方針のため、今後この2つは混ぜない。

## 構成

```
index.html       販売LP（旧 start.html）
thanks.html      決済後の受け取り案内
plug/01/         受け取りページ本体（noindex）
terms.html       利用規約（PLUG 01 用に書き下ろし。第11条＝事業譲渡条項あり）
privacy.html     プライバシーポリシー（第5条＝事業承継に伴う提供あり）
tokushoho.html   特定商取引法に基づく表記
legal.css        法務ページ共通スタイル
```

## 決済

Stripe の Payment Link を `index.html` にベタ書き。**本番（Live）モード**。

- PLUG 01：500円（税込・買い切り） https://buy.stripe.com/4gM00k0C1eOP6SRcTegfu03

## 注意

- AI Creator Camp（90日コミュニティ）へのリンクは絶対URL `https://ai-creator-camp-theta.vercel.app/` を直書きしている。あちらに独自ドメインを付けたら差し替えること
- 利用規約は「500円・買い切り・デジタル商品」を前提に書いてある。AI Creator Camp の規約（月額・審査あり）とは別物なので、片方をコピーして使い回さないこと
- **利用規約 第11条／プライバシーポリシー 第5条** は事業譲渡時に購入者情報を承継するための条項。売却前提の設計なので外さないこと
