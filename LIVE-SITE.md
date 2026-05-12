# 公開済みダッシュボード（成約分析スナップショット）

次の **Public** リポジトリに、本パッケージ（`index.html` 等）をデプロイ済みです。

- **Pages URL:** https://takuyaeguchi00.github.io/seisan-knowledge-dashboard/
- **リポジトリ:** https://github.com/TakuyaEguchi00/seisan-knowledge-dashboard

## ダッシュボードの数値の対象期間

図表の集計は **受注日が 2023年5月1日〜2026年4月30日まで（暦で丸3年・36ヶ月）** に入る成約のみです（`ナレッジ/成約分析` の個別 `.md`、サマリー除外）。**2023年5月〜2024年2月**は当フォルダに該当ファイルが無く **0件** の月として表に出ます。再集計の参照用スクリプト: **`scripts/dashboard-aggregate-3y.mjs`**（`node scripts/dashboard-aggregate-3y.mjs`）。

## IT事業部からの導線（ナレッジ内）

事業部の地図として、同じ URL と更新の考え方を **`01_IT事業部/zz_ITルール/README.md`** の **「成約分析ダッシュボード（受注スナップショット）」** にも記載しています。社内でリンクを貼るときはそちらを正にしても構いません。

## 中身の更新（親リポジトリ側）

1. 編集の正本は **`docs/cheng-yaku-dashboard.html`**（静的 HTML・外部ライブラリなし）。
2. 本フォルダへ反映: **`scripts/sync-public-dashboard.ps1`**（`docs` → `share/public-dashboard-site/index.html`）。
3. 公開サイトへ反映: `share/public-dashboard-site/` の**中身すべて**を、上記 Public リポの**ルート**にコピーして **commit / push**（手順の細部は同フォルダの **`README.md`**）。

## 404 のとき

リポジトリの **Actions** で「Deploy GitHub Pages」が緑か確認する。初回は **Settings → Actions → General** の **Workflow permissions** を **Read and write** にし、失敗したワークフローを **Re-run** する。
