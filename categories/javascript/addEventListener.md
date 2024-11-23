# EventTarget: addEventListener() メソッド

## EventTarget: addEventListener() メソッドとは
addEventListener() は EventTarget インターフェイスのメソッドで、
ターゲットに特定のイベントが配信されるたびに呼び出される関数を設定します。

対象としてよくあるものは Element、Document、Window ですが、
イベントに対応したあらゆるオブジェクトが対象になることができます（IDBRequest など）。

## 構文
```javascript:javascript
addEventListener(type, listener)
addEventListener(type, listener, options)
addEventListener(type, listener, useCapture)
```

type
対象とするイベントの種類を表す文字列です。

マウス関連イベント:
"click": 要素がクリックされたとき12
"dblclick": 要素がダブルクリックされたとき2
"mousedown": マウスボタンが押されたとき2
"mouseup": マウスボタンが離されたとき2
"mousemove": マウスが要素上で移動したとき2
"mouseover": マウスが要素上に入ったとき2
"mouseout": マウスが要素から出たとき2
キーボード関連イベント:
"keydown": キーが押されたとき2
"keyup": キーが離されたとき2
フォーム関連イベント:
"submit": フォームが送信されたとき
"change": フォーム要素の値が変更されたとき
"focus": 要素にフォーカスが当たったとき
"blur": 要素からフォーカスが外れたとき
ウィンドウ関連イベント:
"resize": ウィンドウサイズが変更されたとき1
"scroll": スクロールが発生したとき
ドラッグ＆ドロップ関連イベント:
"dragstart": ドラッグが開始されたとき
"drop": 要素がドロップされたとき
タッチ関連イベント:
"touchstart": タッチが開始されたとき
"touchmove": タッチしながら移動したとき
"touchend": タッチが終了したとき

listener
指定された種類のイベントが発生するときに通知（Event インターフェイスを実装しているオブジェクト）を受け取るオブジェクト。これは null であるか、handleEvent() メソッドのあるオブジェクトか、JavaScript の関数のいずれかでなければなりません。コールバックについて詳しくは、イベントリスナーのコールバックを参照してください。

options 省略可
対象のイベントリスナーの特性を指定する、オプションのオブジェクトです。 次のオプションが使用できます。

useCapture 省略可
論理値で、この型のイベントが、DOM ツリー内の下の EventTarget に配信される前に、
登録された listener に配信されるかどうかを示します。
ツリーを上方向にバブリングしているイベントは、キャプチャを使用するように指定されたリスナーを起動しません。
イベントのバブリングとキャプチャは、両方の要素がそのイベントのハンドラーを登録している場合に、
別の要素内に入れ子になっている要素で発生するイベントを伝播する 2 つの方法です。
イベント伝播モードは、要素がイベントを受け取る順番を決定します。
指定されていない場合、 useCapture は既定で false となります。

wantsUntrusted 省略可 Non-standard
Firefox (Gecko) 独自の引数です。
true の場合、このリスナーはウェブコンテンツによって発行された合成イベント (カスタムイベント) を受け取ります (ブラウザーのクロームでは既定で false ですが、一般のウェブページでは true です)。
この引数は、主にアドオンやブラウザー自身の役に立つものです。

返値
なし (undefined)。

MDN[https://developer.mozilla.org/ja/docs/Web/API/EventTarget/addEventListener]