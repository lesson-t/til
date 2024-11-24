# selfキーワード

## selfの基本的な使い方
1. インスタンスメソッド内でのself
selfは現在のインスタンスを指します。
これにより、インスタンス変数や他のインスタンスメソッドにアクセスできます。

例: インスタンスメソッド内でselfを使って他のメソッドを呼び出すことで、明示的にそのメソッドが同じインスタンス上で呼ばれることを示せます。
```ruby:ruby
class Person
  def initialize(name)
    @name = name
  end

  def introduce
    "Hi, I'm #{self.name}"
  end

  def name
    @name
  end
end
```

2. クラスメソッド内でのself
クラスメソッドを定義する際、selfはクラス自体を指します。
クラスメソッドはクラスレベルで動作するため、クラス変数や他のクラスメソッドにアクセスする際に使います。

例: クラスメソッドを定義する際にdef self.method_nameと書くか、特異クラス構文を使ってまとめて定義します。
```ruby:ruby
class MyClass
  def self.greet
    "Hello from the class!"
  end
end

puts MyClass.greet  # 出力: Hello from the class!
```

3. トップレベルコンテキストでのself
トップレベルでは、selfは特別なオブジェクトであるmainを指し、これはRubyのトップレベルコンテキストです。
このコンテキストでは、トップレベルメソッドや変数が定義されます。

## ベストプラクティス
* 明確さ: selfを使うことで、どのオブジェクトやクラスに対して操作しているかを明確に示せます。特に同名のローカル変数がある場合などには有用です。
* 意図の表現: self.method_nameと書くことで、そのメソッドがインスタンスまたはクラス自身に属することを明確にできます。
* コードの整理: クラスメソッドを複数定義する場合は、特異クラス構文（class << self）を使うとコードが整理されます4。
これらのポイントを押さえておくと、Rubyでのオブジェクト指向プログラミングがより理解しやすくなり、保守性の高いコードを書くことができます。


RUBY[https://www.ruby-lang.org/ja/]