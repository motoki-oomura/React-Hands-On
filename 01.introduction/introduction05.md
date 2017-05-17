# Introduction05
## Single Page Applicationとは
通常のwebサイトはブラウザでリンクをクリックした際に、次のページを読み込み遷移するためにサーバーに「htmlファイルをください」とリクエストを投げます。<br>
リスエストを受け取ったサーバーは「このhtmlファイルです」とレスポンスを返します。<br>
レスポンスを受け取ったブラウザはもらったhtmlファイルから構造を解決し、さらに必要なファイルをリクエストして最終的にページを表示させる仕組みです。

近年よくきくSingle Page Application(以下SPA)とは、**１度htmlファイルを受け取った後は、サーバーにリクエストするたびに「htmlファイルではなくデータ（jsonなど）をレスポンスで返し、それをjavascriptを用いてページを表示させていく**方法です。

<span align="left">[<< Introduction 03: webpackについて](introduction04.md)</span>
<span align="right">[ここをレッスンに飛ばす予定](introduction05.md)</span>
