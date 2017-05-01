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

### letとconst
es2015では、`var`を使わず、 `let`または `const`を使うことを推奨してます。
`let`は再代入が可能な変数を定義し、 `const`は再代入が不可能な変数（定数）を定義します。
```javascript
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



## 参考
- [ECMAScriptとは何か？](https://azu.github.io/slide-what-is-ecmascript/)

<span align="left">[<< Introduction 02: Reactを使うために必要な技術](introduction02.md)</span>
<span align="right">[Introduction 04: webpackについて >>](introduction04.md)</span>
