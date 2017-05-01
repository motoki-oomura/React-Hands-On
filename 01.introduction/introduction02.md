# Introduction02
## Reactを使うために必要な技術
Reactを使ってwebサイトを構築するためには下記の技術が必要になります。
- Ecmascript2015（es2015）
- npm/node.js
- webpack

Reactは基本的にシングルページアプリケーションと言われるwebアプリを構築する際に用いられますが、
<br>そのwebアプリを構築する際の環境周りとして、es2015の仕様にのっとってjsコーディングをします。
<br>es2015はブラウザによって実装されていない機能もあるため、ブラウザで使用できるようにするためには、es5の仕様に変換（トランスパイル）する必要があります。
<br>es5にトランスパイルをするためには、タスクランナー（gulpやwebpackなど）にてbabelを使用します。
<br>その際に使用するタスクランナー、webpackを使うためには、npm/node.jsの技術も知っておく必要があります。

以上のように、ただReactというライブラリを使用するだけでも色々な技術を知っておく必要があるため
<br>Reactを学ぶ前に必要な技術を使えるようにならなければなりません。

そこで今回のHands Onでは、そこらへんの技術を踏まえ学習していく内容になっております。


<span align="left">[<< Introduction 01: Reactとは](introduction01.md)</span>
<span align="right">[Introduction 03: webpack >>](introduction03.md)</span>
