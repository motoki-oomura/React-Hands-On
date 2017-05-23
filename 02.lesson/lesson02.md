# Lesson02
## スタイル
HTMLにCSSでスタイルを付与するように、Reactでも作成したコンポーネントにCSSスタイルを付与することができます。<br>
従来通り、CSSをclass名で指定することも可能ですが、「ファイルが分かれてしまうこと(jsx, css)」「命名が衝突する問題」などがあることから、コンポーネント指向では必ずしもいい方法とは言えなくなっています。


### 実際にやってみる
とりあえず、学ぶよりも実践しながら学んでみましょう。<br>
`src/lesson/lesson02.jsx`を作成してください。<br>
最初にAppコンポーネント（ルートコンポーネント）を記述しておきます。<br>
Appコンポーネントの中に今回作成するコンポーネントを内包し、レンダリングしていきます。

```jsx harmony
// lesson02.jsx

// ルートコンポーネントをsfcで作成
// コンポーネントの中にHelloコンポーネントを内包。
// Appコンポーネントがレンダリングされれば自動的にレンダリングされます。
const App = () => (
  <div>
    /* ここに今回作成するコンポーネントを内包する */
  </div>
);


// ここに今回作成するコンポーネントを定義していく

export default App;
```


また、 `src/index.js` に記載されている `import App from './src/lesson/lesson01';` はコメントアウトしておきましょう。<br>
（以前のLessonと混合してわかりずらくなるため）<br>
そして、 `src/lesson/lesson02.jsx` をインポートしておきましょう。

```js
// import文はnpmパッケージでインストールした `react` `react-dom`モジュールを使うために呼び出してます
import React from 'react';
import { render } from 'react-dom';

// Lesson01
// lesson01.jsxで作成したAppコンポーネントを読み込み
// import App from './src/lesson/lesson01';      <= ここをコメントアウト
// Lesson02
import App from './src/lesson/lesson02';          // ここを今回追加

// 定義したComponentを id="app" のDOMに当てはめてます
render(<App/>, document.getElementById('app'));
```

#### コンポーネントにインラインスタイルをあててみる
スタイルを定義する方法としては様々な方法がありますが、まず始めにインラインスタイルをコンポーネントにあててみましょう。


```
//lesson02.jsx

// Helloコンポーネントを作成
const Hello = () => (
  // style属性に {{}} で囲い、中にプロパティを書く
  <div style={{ color: 'red' }}>Hello!</div>
);

```








<span align="left">[<< Lesson00: コンポーネント](lesson01.md)</span>
<span align="right">[ >>](lesson03.md)</span>
