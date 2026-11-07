# LEI MAKANI ファーストビュー動画（自前ホスティング）

BASE の HOME 動画パーツに埋め込む、動画だけのページ。YouTube のタイトルやボタンを出さないために使う。

- `index.html` 動画を画面いっぱいに自動再生・無音・ループ
- `hero_720.mp4`（3.1MB、PC）/ `hero_540.mp4`（1.9MB、幅640px以下）を iframe 幅で自動選択。元の 1080p 版は `_trial/`（git 管理外）
- `poster.jpg` 読み込み前に出す静止画

公開先: Cloudflare Workers（静的アセット）https://leimakani-hero.leimakani.workers.dev/ 。更新は `dist/` に index.html・mp4・poster をコピーして `npx wrangler deploy`。GitHub Pages（https://matsubishion.github.io/leimakani-hero/）は予備。
