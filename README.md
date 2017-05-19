# PHP の基本( http://www.php.net/manual/ja/ などを参照）

## 表示の基本
PHP 自体は単独でも実行できるプログラム言語であるが、この講義では、それをウェブページとして表示させる。

xampp の apache を「start」しておき、

http://localhost/リポジトリ名/ファイル名

で表示させる。

例：
http://localhost/php-basics-???/hello.php

## HTML 中に PHP スクリプトを埋め込む

```html:PHP Script
		<?php
PHP スクリプト
		?>
```

一つのファイル中に何度も PHP スクリプト部分が出現してよい。スクリプト中では、大文字･小文字は区別する。

## 命令文

PHP の命令文は、```;``` で終了する。付け忘れると「次の行」でエラーが発生する。

```html:php check
<?php
  phpinfo();
?>
```


例：
http://localhost/php-basics-???/info.php


## コメント：
```php:Comment
	// 行末までコメント
	/*
		コメントブロック
	*/
```

## 基本型
		```
    integer, float, boolean, string, array, object, resource, NULL
    ```

## 変数名
		```
    $ の後に英文字＋（任意長の英数文字の繰り返し）（英文字にはアンダースコアを含む）
    ```

PHP では、変数宣言なしに変数を使用できる。変数がすでに宣言されているかどうかを調べるには、関数 ```isset(変数名)```　を用いる。定義済み変数を未定義にするには、命令 ```unset(変数名)``` を使用する。

```php:isset
print(isset($newvar));
```

## 文字列：
シングルクォーテーションで囲った文字列は、ほぼそのまま評価される。ダブルクォーテーションで囲った文字列は、C 言語に類似したエスケープを行う。また、ダブルクォーテーション内の変数は展開される。文字列の接続には、ピリオドを使う。

```php:strings
$var = 'test';
echo ' $var \n';	// $var \n
echo " $var \n";	// test 改行
echo $var . '000';	// test000
```

## 型の自動変換：
		型は代入･参照時に自動的に変換される。（注意が必要）

```php:implicit typing
		$x = '10';
		$y = $x + 10;	// 20
```
# 自習用リンク

https://www.w3schools.com/php/

# 課題

配布した「kadai.php」中で、書き換え指示に従って課題ページを作成し、提出すること。期限は、５月２６日。次回講義で質問があれば受け付ける。

動作チェック：
http://localhost/php-basics-???/info.php
