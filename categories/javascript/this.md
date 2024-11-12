# this

## thisとは
thisは、現在のコードが実行されている「コンテキスト」（文脈）を指すキーワードです。
簡単に言えば、「今、誰が（どのオブジェクトが）この処理を行っているか」を示します。

## thisの基本的な動作
1. グローバルスコープ:
通常の関数やグローバルスコープでは、thisはグローバルオブジェクト（ブラウザではwindow）を指します。

```javascript:javascript
console.log(this); // window オブジェクト
```

2. オブジェクトのメソッド:
オブジェクトのメソッド内では、thisはそのメソッドを持つオブジェクトを指します。

```javascript:javascript
const person = {
  name: "太郎",
  sayHello: function() {
    console.log(`こんにちは、${this.name}です`);
  }
};
person.sayHello(); // "こんにちは、太郎です"
```

3. イベントハンドラ:
DOM要素のイベントハンドラ内では、thisは通常そのイベントが発生した要素を指します。

```javascript:javascript
button.addEventListener("click", function() {
  console.log(this); // クリックされたボタン要素
});
```

## thisの注意点
1. 関数の呼び出し方によって変わる:
thisの値は、関数がどのように呼び出されたかによって変わります。

2. アロー関数での特殊性:
アロー関数内のthisは、その関数が定義された場所のthisを引き継ぎます。

```javascript:javascript
const obj = {
  name: "オブジェクト",
  regularFunc: function() {
    console.log(this.name); // "オブジェクト"
  },
  arrowFunc: () => {
    console.log(this.name); // undefined（グローバルスコープの this を参照）
  }
};
```

3. 明示的なthisの指定:
call(), apply(), bind()メソッドを使用すると、thisの値を明示的に指定できます。

## まとめ
thisは、コードの実行コンテキストを示す重要な概念です。
関数やメソッドがどのように呼び出されたかによって、
その値が変わることを覚えておくことが大切です。
初学者の段階では、特にオブジェクトのメソッド内でのthisの使用に注目し、
徐々に他のケースについても理解を深めていくとよいでしょう。

MDN[https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/this]