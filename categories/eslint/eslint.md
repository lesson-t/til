# ESLint

JavaScriptコードの静的解析ツール

1. 目的
+ コード品質の向上
+ 潜在的なバグの早期発見
+ コーディングスタイルの統一

2. 主な機能
+ 構文エラーの検出
+ ベストプラクティスの強制
+ コーディング規約の適用

3. 特徴
+ 高度にカスタマイズ可能：ルールの有効/無効の切り替えや、独自ルールの作成が可能
+ プラグイン対応：多数のプラグインが利用可能で、機能を拡張できる
+ モダンなJavaScript/TypeScriptのサポート：ES6以降の新しい構文や、TypeScriptにも対応


4. 使用方法
+ プロジェクトにインストールして設定ファイル(.eslintrc)を作成
+ コマンドラインから実行、またはエディタ/IDEと統合して使用

5. メリット
+ コードの一貫性維持：特に複数人での開発時に有効
+ 早期のバグ発見：実行前に潜在的な問題を検出
+ コード品質の向上：ベストプラクティスの適用を促進

6. 他ツールとの連携
+ Prettierなどのコードフォーマッタと組み合わせて使用可能
+ ESLintは、多くのJavaScript/TypeScriptプロジェクトで標準的に使用されており、コード品質の維持と向上に大きく貢献するツールです。



## インストール

```
npm i --save-dev  eslint @eslint/js
```

ルートディレクトリに下記ファイルを作成する。
eslint.config.js

作成したeslint.config.jsファイルに設定を追加する。
globalsを含む基本的なやつ
```
import js from "@eslint/js";
import globals from "globals";

export default [
  js.configs.recommended,

  {
    rules: {
      "no-unused-vars": "warn",
      "no-undef": "warn",
      "no-console": "warn",
      "no-unreachable": "warn",
    },
    languageOptions: {
      globals: {
        ...globals.browser,
      },
    },
  },
];
```

package.jsonに下記を追加する。
```
"type": "module"
```

コマンドから実行する。
```
npx eslint yourfile.js
```


ESLint[https://eslint.org/docs/latest/use/getting-started]