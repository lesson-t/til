# Event.preventDefault() メソッド

## Event.preventDefault() メソッドとは
ウェブブラウザのデフォルトの動作を阻止するために使用される重要な JavaScript のメソッドです。

preventDefault() メソッドは、イベントが発生したときにブラウザが自動的に行う標準の動作を停止させます。
例えば、次のようなものがあります。
* リンクをクリックしたときに新しいページに移動するのを防ぐ
* フォームの送信ボタンを押したときにフォームが送信されるのを防ぐ
* チェックボックスをクリックしたときに選択状態が変わるのを防ぐ

## 使用方法
```javascript:javascript
element.addEventListener("event", function(event) {
  event.preventDefault();
  // カスタムの処理をここに書く
});
```

## 具体例
リンクのクリックを防ぐ:
```javascript:javascript
document.querySelector("a").addEventListener("click", function(event) {
  event.preventDefault();
  console.log("リンクはクリックされましたが、ページ遷移は起こりません");
});
```

フォームの送信を防ぐ:
```javascript:javascript
document.querySelector("form").addEventListener("submit", function(event) {
  event.preventDefault();
  console.log("フォームは送信されませんでした");
});
```
## 注意点
preventDefault() を使用しても、イベントの伝播（バブリング）は止まりません。
イベントがキャンセル可能でない場合、preventDefault() は効果がありません。
パッシブイベントリスナーでは preventDefault() は機能しません。

MDN[https://developer.mozilla.org/ja/docs/Web/API/Event/preventDefault]