# 成約分析ダッシュボード（公開用ミニサイト）

`runbird-it-knowledge` の **`docs/cheng-yaku-dashboard.html`** と同じ HTML/CSS 図解を、**外部に URL で共有するためだけ**に載せる最小パッケージです。

## 手順（初回）

1. GitHub で **新しいリポジトリ**を作成する（**Public** にする。Private だと無料では Pages の公開 URL が出ません）。
2. このフォルダの **中身すべて**（`.github` / `index.html` / `.nojekyll` / `README.md`）を、新リポジトリの **ルート**にコピーして push する。
3. リポジトリの **Settings → Pages** で **Build and deployment** の **Source** を **GitHub Actions** にする。
4. **Actions** タブで「Deploy GitHub Pages」が成功したら、表示される URL（例: `https://<あなた>.github.io/<リポ名>/`）を共有する。

## ナレッジ側を更新したあと

親リポジトリで `scripts/sync-public-dashboard.ps1` を実行すると、この `index.html` が `docs/cheng-yaku-dashboard.html` から上書きコピーされます。その後、公開用リポジトリへ再度 push してください。
