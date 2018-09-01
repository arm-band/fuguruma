# Fuguruma

## Abstract

`markdown-pdf`をWeb上から実行するためのミニマルパッケージです。

## Files

ファイル一覧

- `index.html`: Node.jsで動作させるコード&レスポンスとして表示させるページ本体
- `.htaccess`: 通常のままではNode.jsは8001ポートで動作するようにしてあるので、ポート番号の違いからクロスオリジン判定されてブラウザでのダウンロードが実行できない。それを回避するために文言を入れてある。
- `form.html`: `index.html`にデータを投げるフォーム部分
- `package.json`: 必要なライブラリ列挙、`npm scripts`など
- `readme.md`: このファイルです。

## Prepare

事前の準備。Node.jsインストール済みの前提。

1. SSL無効化する:  
~~~
# npm config set strict-ssl false
~~~
2. 必要なパッケージのインストール:  
~~~
# sudo npm i -D
~~~
3. 設定(PDF生成先ディレクトリの作成):  
~~~
# sudo npm run mkd
# sudo npm run chm
~~~

## Execute

サーバで`index.html`のある場所まで移動して

~~~
# node index.html &
~~~

する(手動起動)。

## Origin of the name

「Fuguruma」という名前は、妖怪の「文車妖妃」から(`form.html`の見出しが「Youhi」となっているのもここから)。文車は寺院や邸宅の書物を火災などの非常時に持ち出すために使う車のこと。

`index.html`の1つのファイルでサーバとクライアントの双方の処理を行き来する様子を車輪に例えました。また、PDF文書を扱うことから紙や本に関連のあるものということで、文車を連想した結果です。