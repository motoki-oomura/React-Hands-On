# Lesson01
## コンポーネント
Reactはコンポーネント指向のライブラリです。<br>
コンポーネント単位でUIの部品を作成し、それを組み合わせてwebアプリケーションを構築していきます。<br>

コンポーネントは役割に応じていくつかの方法で定義することができます。<br>

参考URL：
- [協働のためのUIコンポーネント指向とエンジニアリングの前知識](https://m.axross.io/%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%8B%E3%82%A2%E3%83%AA%E3%83%B3%E3%82%B0%E3%81%AB%E3%81%8A%E3%81%91%E3%82%8Bui%E3%82%B3%E3%83%B3%E3%83%9D%E3%83%BC%E3%83%8D%E3%83%B3%E3%83%88%E6%8C%87%E5%90%91%E3%81%AE%E8%80%83%E3%81%88%E6%96%B9%E3%81%A8%E5%8D%94%E5%83%8D%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6-2c3dbca01ab9)


### はじめてのコンポーネント作成
まずはじめに、実際に簡単なコンポーネントを作成してみましょう。

#### 1.テンプレートの作成
今回のLessonの表示結果を出すためのindex.htmlから記載していきます。<br>
reactでは作成したコンポーネントをjavascriptを使って展開していきます。<br>
そのために展開先となるDOM `<div id="app"></div>` をhtmlに記述しておきます。

```html
<!--src/index.html-->

<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>React Hands On</title>
</head>
<body>
  <!--Reactのコンポーネントを展開するために、下記要素を記載-->
  <div id="app"></div>
</body>
</html>
```

#### 2.React Componentの作成
次にコンポーネントを作成するためのjsを作成します。<br>
まず `src/lesson/lesson01.jsx` を作成します。<br>
※ jsx拡張子はReactでよく使われる拡張子です。

```jsx harmony
// lesson01.jsx

// AppというComponentの定義をしてます
const App = () => (
  <div>Hello, React!</div>
);

// 作成したApp Componentを他のファイルで使えるようにするためにはexportしてます
export default App;
```

#### 3.index.jsに記述
React Componentを作成したあと、それをwebpackでバンドルさせるために、エントリポイントである `index.js` に読み込ませます。

```jsx harmony
// index.js

// import文はnpmパッケージでインストールした `react` `react-dom`モジュールを使うために呼び出してます
import React from 'react';
import { render } from 'react-dom';

// Lesson01
// lesson01.jsxで作成したAppコンポーネントを読み込み
import App from './src/lesson/lesson01';

// 定義したComponentを id="app" のDOMに当てはめてます
render(<App/>, document.getElementById('app'));
```

#### 4.buildする
作成したソースファイルから実際に動かすためにwebpackを実行します。<br>
ターミナルからプロジェクト直下内で下記コマンドを叩いてください。

```bash
$ npm run build
```

そうすると、プロジェクトルート直下に `build`フォルダができるので、ブラウザで開いてみましょう。<br>
ブラウザに `Hello, React!`と表示されていれば成功です。


### React Componentの種類
React Componentを作成するためにはいくつかの方法があります。

- React.createClass
- React.Component
- Stateless function component 

#### React.createClass
`React.createClass` は主にES5記法で用いられる書き方です。<br>
またこちらの書き方に関しては現在、React開発サイドが非推奨としているため、使わない方がいいです。

```jsx harmony
var Component = React.createClass({
  render: function() {
    return (
      <div>this is component</div>
    );
  }
});
```

#### React.Component
`React.Component` はECMAScript2015記法で用いられる書き方です。<br>
基本開発するときはECMAScript2015で開発することがほとんどなので `createClass`よりこちらを使用することがほとんです。
```jsx harmony
class Component extends React.Component {
  render() {
    return (
      <div>this is component</div>
    );
  }
}
```


#### Stateless function components（SFC）
さきほど作成したReact ComponentはこのSFCで作成しました。<br>
SFCはReactのState（状態）を保持しないコンポーネントです。<br>
コンポーネントを作成するときはStateを必要としない限りはSFCでコンポーネントを作成しましょう。<br>
※ stateについては別のLessonにて説明します。
```jsx harmony
const Component = () => {
  return (
    <div>this is component</div>
  );
}
```

<span align="left">[<< Lesson00: 環境構築](lesson00.md)</span>
<span align="right">[Lesson01: React Component >>](lesson02.md)</span>
