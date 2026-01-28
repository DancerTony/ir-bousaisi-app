# PWA配布用パッケージ（防災士試験対策：極限訓練所）

このフォルダは、**アップするだけでURLで動くPWA**（ホーム画面に追加できるWebアプリ）として配布できる最小構成です。

## 構成
- `index.html` : アプリ本体（元HTMLにPWA用タグとSW登録を追加）
- `manifest.webmanifest` : PWA設定
- `sw.js` : オフライン対応（Cache-first）
- `icons/` : アイコン（192/512）

## 使い方（どれか1つでOK）
### 1) GitHub Pages
1. このフォルダ内容をリポジトリ直下に置いてPush
2. GitHubの **Settings → Pages** で `main / root` を選んで保存
3. 発行されたURLにアクセス → ブラウザの「ホーム画面に追加」

### 2) Netlify（ドラッグ&ドロップが最速）
1. Netlifyにログイン
2. このフォルダをZip化して **Deploy** にドラッグ&ドロップ
3. 発行URLにアクセス → 「ホーム画面に追加」

### 3) Vercel / Cloudflare Pages
- 「Static Site」としてこのフォルダをデプロイ（Build不要）

## 注意
- PWA（特にService Worker）は **HTTPS** または `localhost` でのみ有効です。
- 更新が反映されない場合は、ブラウザの更新（強制リロード）や、アプリ/サイトデータ削除を行ってください。

## カスタムしたい場合
- アプリ名や色：`manifest.webmanifest`
- アイコン：`icons/` のPNGを差し替え
- キャッシュ対象：`sw.js` の `PRECACHE_URLS`
