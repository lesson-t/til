styleプロパティの設定・削除

styleの設定
styleプロパティを使うと、要素のスタイルを設定することができます。

使用例
element.styleに続けて、プロパティ名と付与したい実際の値を記述します。
```
element.style.プロパティ名 = 'value';
```

styleの削除

スタイルを削除したい場合、値にnullを代入します。
```
element.style.プロパティ名 = null;
```