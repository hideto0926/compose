# KOZU 構図カメラ — Website

KOZU 構図カメラ（KOZU Composition Camera）の公開ページ。日英切り替え（EN/JA）、ビルド不要の静的ページ。Three.js は CDN（jsdelivr）から読み込む。

- `index.html` — 紹介ページ（Three.js のヒーロー、被写体をタップして構図を試すデモ、14の構図、スクリーンショット、特長、プライバシーの要点、よくある質問）。App Store の「サポートURL」「マーケティングURL」にも使う
- `privacy.html` — プライバシーポリシー（App Store の「プライバシーポリシーURL」）
- `assets/icon.png` — アプリアイコン、`assets/shots/` — スクリーンショット、`assets/examples/` — 構図の見本画像
- `assets/compositions.json` — 14構図のガイド線（アプリの `Composition.guide()` から書き出したもの。アプリ側を変えたら書き出し直す）
- `.nojekyll` — GitHub Pages でそのまま配信する

## 公開（GitHub Pages）
1. このフォルダの中身を `composeCam` リポジトリ（https://github.com/hideto0926/composeCam ）のルートに push する
2. リポジトリ → Settings → Pages → Source: *Deploy from a branch*、branch = default、folder = `/ (root)`
3. 1分ほど待って https://hideto0926.github.io/composeCam/ を開く
4. App Store の URL が決まったら、`index.html` の「App Store で近日公開」ボタンを差し替え、`homepageRoot` のカードも更新する

## 公開前にやること
- スクリーンショットはシミュレータのダミー風景（描いた絵）で撮ったもの。実機の画面に差し替えるとより伝わる
- プライバシーポリシーはアプリの実装（2026-09-29 時点：通信なし、解析はすべて端末内）に合わせてある。通信や SDK を増やしたら更新する
