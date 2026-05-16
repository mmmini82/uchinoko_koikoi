うちの子こいこい PWA版

■中身
- index.html：ゲーム本体
- manifest.webmanifest：PWA設定
- sw.js：オフライン用キャッシュ
- icons/：ホーム画面用アイコン

■大事
PWAとして「ホーム画面に追加」するには、基本的にHTTPSで公開する必要があります。
HTMLをダブルクリックで開く file:// では、ゲーム自体は動いてもService Workerが使えないため、PWA化はできません。

■スマホに入れる流れ
1. このフォルダの中身をGitHub Pages / Netlify / Vercelなどにアップロード
2. スマホで公開URLを開く
3. iPhone：Safariの共有ボタン → ホーム画面に追加
   Android：Chromeのメニュー → アプリをインストール / ホーム画面に追加

■PCで軽く試す
フォルダ内で簡易サーバーを立てると確認できます。
Pythonが入っている場合：
python -m http.server 8000
そのあと http://localhost:8000 を開きます。
