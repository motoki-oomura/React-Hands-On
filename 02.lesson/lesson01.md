# Lesson01
## React Component
Reactはコンポーネント指向のライブラリです。<br>
コンポーネント単位でUIの部品を作成し、それを組み合わせてwebアプリケーションを構築していきます。<br>

コンポーネントは役割に応じていくつかの方法で定義することができます。<br>

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
  <title>Document</title>
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

- 
- 
- 
- Stateless function component 
