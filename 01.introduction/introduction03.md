# Introduction03
## ECMAScript2015について
ECMAScriptとは、ECMA Internationalにて標準化をされているjavascriptの仕様のことをいいます。

javascriptはECMAScriptの仕様を元に実装された言語のことをさします。

ECMAScript2015とは2015年に新しく仕様が決まったものです。
<br>ただ仕様が決まったとしても、既存全てのブラウザで使用できるとは限りません。
<br>ECMAScript2015はあくまでも仕様の話なので、実装とは違います。

では、ECMAScript2015の機能を使用するためにはどうしたらいいか。
<br>Babelというトランスパイルツールを使用して、現在のブラウザでほとんど実装が終わっているECMAScript5の仕様に変換する必要があります。


## よく使う文法
Reactをコーディングする上で使用するes2015の書き方を紹介します。
実際に試しながらコーディングしたほうがいいと思いますので、テストコードを簡単にかけるサイトで試してみてください。
https://codepen.io/

使い方
1. Create => NewPen　を押下
2. Settings => javascript を押下
3. 「JavaScript Preprocessor」をBabelに変更しCloseをオス
4. コードを書いてみる



### letとconst
es2015では、`var`を使わず、 `let`または `const`を使うことを推奨してます。
`let`は再代入が可能な変数を定義し、 `const`は再代入が不可能な変数（定数）を定義します。
```ecmascript 6
// es5
var x = 10;
console.log(x); // 10

x = 20;
console.log(x); // 20

// es2015
let y = 10;
console.log(y); // 10

y = 20;
console.log(y); // 20

const z = 10;
console.log(z);

z = 20 // error

```

### Object Shorthand
es2015では、Objectのkey名と変数名が同じ場合は、省略記法を使用することができます。

```ecmascript 6
// es5
var hoge = 'xyz';
var obj = {
  hoge: hoge
};
console.log(obj.hoge) // 'xyz'

// es2015
let fuga = 'abc';
let obj = { fuga };
console.log(obj.fuga) // 'xyz'


```

### Destructuring Assignment
分割代入は、配列とオブジェクトを分解して、要素とプロパティ値をひとつひとつの変数に分解するための構文です。

```ecmascript 6
// es5
var obj = {hoge: 'abc', fuga: 'xyz'};
var hoge = obj.hoge;
var fuga = obj.fuga;

console.log(hoge); // 'abc'
console.log(fuga); // 'xyz'


// es2015
const obj = {hoge: 'abc', fuga: 'xyz'};
const { hoge, fuga } = obj;

console.log(hoge); // 'abc'
console.log(fuga); // 'xyz'


```


### Arrow Function
es2015では関数の新しい書き方でアロー関数というものがあります。
<br>いままでコールバック関数内で `this`を使いたかった際には、変数に一度代入する必要がありましたが、
<br>アロー関数ではそれをする必要がありません。


```ecmascript 6
// es5
var mtself = this;
setInterval(function(){
  this.hoge();
});

// function(引数) {
// 処理  
// }


// es2015
setInterval(() => {
  this.hoge();
});

// (引数) => { 
//   処理
// }

```




## 参考
- [ECMAScriptとは何か？](https://azu.github.io/slide-what-is-ecmascript/)

<span align="left">[<< Introduction 02: Reactを使うために必要な技術](introduction02.md)</span>
<span align="right">[Introduction 04: webpackについて >>](introduction04.md)</span>
