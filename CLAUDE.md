# CLAUDE.md — NaviSolForge ポートフォリオサイト

このファイルは、Claude Code がこのプロジェクトを理解するための前提メモです。

## プロジェクト概要
個人開発事業「**NaviSolForge**」の制作実績ポートフォリオサイト。
小さな店舗（美容室など）向けにウェブサイト制作の営業をかける際に使う、名刺代わりの1ページサイト。
HTML/CSS/JSのみの静的サイト（CMS・サーバー処理なし）。

**`lagray3-website`（美容室ラグレー3の納品サイト）とは別プロジェクト。**
あちらは制作実績の1件目として本サイトからリンクしているが、リポジトリ・デプロイ先はそれぞれ独立している。

## デザインコンセプト
「NaviSolForge（Forge＝鍛冶場）」から着想した、鉄色の地に熱した金属のようなオレンジが差し色の世界観。
La gray3サイトの和モダン（グレージュ＋オレンジ）とは意図的にトーンを分けている。

- 色（ライト基調）：`--bg:#F2EDE6` / `--surface:#E7DFD3` / `--ink:#211B16` / `--ink-soft:#6B6055` /
  `--ember:#C1451F`（アクセント）/ `--steel:#3E4F54`
- ダークモードにも対応済み（`prefers-color-scheme`で自動切替、`--ember`は`#E8592A`など明るめに調整）
- フォント：見出し=Shippori Mincho B1、本文=Noto Sans JP、英字・ロゴ・数字=Big Shoulders Display
- ヒーローに控えめなキャンバスアニメーション（火の粉が上る演出、`prefers-reduced-motion`で無効化）

## セクション構成（public/index.html）
ヒーロー → 制作実績（実績をログ形式で並べる。管理上は連番だが、画面上に「No.01」等の表記はしない） → つくり方（4ステップ） → ご依頼・ご相談

- 実績は連番管理。**新しい実績が増えたら、既存の「準備中」プレートを実績に差し替え、新しい「準備中」プレートを追加する**運用。
- 現在：1件目 = 美容室ラグレー3（実在の納品実績、`https://lagray3.com/`にリンク）。2件目 = 空き枠（準備中）。
- 実績に書く内容は、実際にやった作業ベースの具体的な記述にする（誇張・架空の実績は書かない）。

## 実データ
- 連絡先：`navisolforge@gmail.com`（mailtoリンク）
- 対応エリア：札幌近郊
- 実績No.01の画像：`public/images/lagray3-thumb.jpg`（La gray3のOGP画像を流用）

## ファイル構成
- `public/index.html` … 本体（唯一のページ）
- `public/images/` … 実績サムネイル等の画像
- `netlify.toml` … Netlifyの公開フォルダを`public`に指定

## デプロイ
- GitHub: `NaviSolForge/myPortfolio`
- Netlify: 公開済み。`https://navisolforgeportfolio.netlify.app/`
- 独自ドメインは今のところ予定なし。まずは仮URLで営業に使う想定。

## 今後の想定
- 系列店など新しい制作依頼が来たら、No.02を実績に差し替えて実績を増やしていく
- 依頼者からの要望に応じて、料金感・対応内容などのセクションを追加する可能性あり
