Element: classList プロパティ

Element.classList は読み取り専用のプロパティで、
生きた DOMTokenList コレクションでその要素の class 属性を返します。
これを使用してクラスリストを操作することができます。


DOMTokenList 自体は読み取り専用ですが、
add(), remove(), replace(), toggle() 
の各メソッドを用いてオブジェクトを変更することはできます。

使用例
element.styleに続けて、プロパティ名と付与したい実際の値を記述します。
```
const div = document.createElement("div");
div.className = "foo";

// 最初の状態: <div class="foo"></div>
console.log(div.outerHTML);

// classList API を用いてクラスを除去、追加
div.classList.remove("foo");
div.classList.add("anotherclass");
```

MDN[https://developer.mozilla.org/ja/docs/Web/API/Element/classList]