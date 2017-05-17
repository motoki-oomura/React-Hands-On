# Lesson00
## 環境構築
###  はじめに
これからReactを様々な技術を使って学んでいきます。<br>
そのためには色々準備が必要なため、最初に環境構築を行なっていきます。<br>
今回のLessonで使用する技術は下記です。

- ECMAScript2015 => 新しいjsの書き方
- babel => ECMAScript2015をブラウザで動かすためにコンパイルするツール
- webpack => バンドラーツール
- React => 本レッスンで学ぶライブラリ

これら技術を使用してReactを学ぶので、それぞれなんだろう？となる場合は Introduction をみてください。

### 環境構築をしよう
#### 1.作業ディレクトリを作成する
まずはじめに、Hands Onを学んでいくための作業ディレクトリを作成します。<br>
作業ディレクトリの名前は場所は好きに作成していただいて構いません。

#### 2.package.jsonの作成
次にnpmパッケージを使用するために`package.json`を作成します。

```bash
$ npm init -y
```

```
// 現在のディレクトリ構造
ProjectRoot/
  |- package.json
```

#### 3.パッケージをインストール
次にnpmを用いてwebpack、またそれに伴うパッケージをインストールします。<br>
まず７つのパッケージを `--save-dev` でインストールします。<br>
※ 開発の際のみに使用するパッケージは基本的に `--save-dev` でインストールします。

- webpack
- webpack-dev-server
- babel-loader
- babel-core
- babel-preset-es2015
- babel-preset-react
- html-webpack-plugin

```bash
$ npm install --save-dev webpack webpack-dev-server babel-loader babel-core babel-preset-es2015 babel-preset-react html-webpack-plugin 
```

次に、２つのパッケージを `--save` でインストールします。<br>
※ 実際にブラウザで動かして使用するパッケージは基本的に `--save` でインストールします。

- react
- react-dom

```bash
$ npm install --save react react-dom
```

`package.json` をみると、にパッケージのリストが登録されたことが確認できます。

```
// 現在のディレクトリ構造
ProjectRoot/
  |- package.json
  |- node_modules/
```
