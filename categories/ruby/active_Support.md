# Active Support ：Railsライブラリ

数値や日付や文字列などさまざまなライブラリの集まり。
その中でCore Extensions（コア拡張機能）と呼ばれるものの多くは、
Railsで使うためにRubyの標準ライブラリに含まれるクラスを拡張しています。

Active Supportを大きく分けると、コア拡張機能とそれ以外のライブラリがあります。
コア拡張機能：	Rubyの機能をRails用に拡張する（Railsでは必須）
それ以外　　：	上におさまらないもの（必須なものもある）

コア拡張機能
全オブジェクトで使えるもの：	json.rb、try.rbなど
モジュールやクラスの拡張用：	module/aliasing.rb、class/attribute.rbなど
数値関連　　　　　　　　　：	integer/inflections.rb、big_decimal/conversions.rbなど
文字列関連　　　　　　　　：	string/inquiry.rb、string/multibyte.rb
列挙/ハッシュ/配列関連　　：	enumerable.rb、hash/indifferent_access.rb、array/access.rbなど
日付・時刻関連　　　　　　：	date_and_time/zones.rb、time/calculations.rbなど
その他　　　　　　　　　　：	正規表現、ファイル、マーシャル、NameError/LoadError

それ以外
キャッシュ　　　　　　　　　　　　　：	cache/mem_cache_store.rb、cache/strategy/local_cache_middleware.rbなど
並列・並行処理（concurrency）　　　 ：	concurrency/share_lock.rbなど
依存関係（dependencies）　　　　　　：	dependencies/autoload.rbなど
非推奨（deprecated）ライブラリ処理　：	deprecation/behaviors.rbなど
期間（duration）　　　　　　　　　　：	duration.rbなど
英単語の活用（inflection）　　　　　：	inflector/inflections.rbなど
JSON　　　　　　　　　　　　　　　　：	json/decoding.rbなど
ログ　　　　　　　　　　　　　　　　：	log_subscriber.rb、logger_thread_safe_level.rbなど
暗号化・署名　　　　　　　　　　　　：	message_encryptor.rb、message_verifier.rbなど
マルチバイト　　　　　　　　　　　　：	multibyte/unicode.rbなど
通知・監視　　　　　　　　　　　　　：	notifications/instrumenter.rbなど
数値変換　　　　　　　　　　　　　　：	number_helper/number_to_currency_converter.rb、number_helper/number_to_phone_converter.rbなど
テスト　　　　　　　　　　　　　　　：	testing/assertions.rb、testing/file_fixtures.rbなど
時間　　　　　　　　　　　　　　　　：	time_with_zone.rb、values/time_zone.rbなど
XML・Nokogiri　　　　　　　　　　　 ：	xml_mini/libxml.rb、xml_mini/nokogirisax.rbなど
その他　　　　　　　　　　　　　　　：	array_inquirer.rbなど

TechRacho[https://techracho.bpsinc.jp/hachi8833/2016_11_09/28535]