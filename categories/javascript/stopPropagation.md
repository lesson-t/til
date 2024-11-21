# Event: stopPropagation() メソッド

## Event: stopPropagation() メソッドとは
Event インターフェイスのメソッドで、
キャプチャおよびバブリング段階において現在のイベントのさらなる伝播を阻止します。
しかし、これは既定の動作の発生を妨げるものではありません。
例えば、リンクのクリックはまだ処理されます。
これらの動作を止めたい場合は、preventDefault() メソッドを参照してください。
また、現在の要素における他のイベントハンドラーへの伝搬も防げません。
それらを止めたい場合は、stopImmediatePropagation()　を参照してください。

## 構文
```javascript:javascript
event.stopPropagation()
```
引数および返値： なし

MDN[https://developer.mozilla.org/ja/docs/Web/API/Event/stopPropagation]