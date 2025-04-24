### ファイルを探す

- findコマンド- ディレクトリツリーからファイルを探す

```
find <検索開始ディレクトリ> <検索条件> <アクション>
```

- findコマンド例
![alt text](image-2.png)

アクションにprintを指定することで検索結果を表示することができる

- 以下のようにすることで指定したディレクトリ直下だけでなく、ディレクトツリーを下り、一致するファイル全てを表示する。

![alt text](image-1.png)

- ファイル名で探す場合は「name」か「iname」で探す。
ちなみに「*」か[?]を含む単語は''か""で囲む

```
find . -name '*.txt' -print
```

- ファイルの種類で探す

![alt text](image.png)


カレントディレクトリの下にあるディレクトリを列挙

![alt text](image-3.png)


ー複数の検索条件を-aで指定

![alt text](image-4.png)

- Locateコマンド・ファイル名データベースからファイルを探す

locateコマンドはパスの一部を検索してファイルを探すコマンド

```
locate [オプション] <検索パターン>
```

「bash」という文字列を含むパス名を検索

![alt text](image-5.png)

拡張子.sedのファイルを検索

![alt text](image-6.png)


大文字小文字を区別しない

![alt text](image-7.png)

ファイル名だけを対象に検索

![alt text](image-8.png)

複数の検索条件を指定してOR検索

![alt text](image-9.png)

複数の検索パターンを含むようAND検索

![alt text](image-10.png)

### コマンドの使い方を調べる

- --helpオプション

![alt text](image-11.png)


- manコマンド - マニュアルを表示する

コマンドについて調べる

```
man <調べたいコマンド>
```

- man catの実行結果

![alt text](image-12.png)

manの各項目

![alt text](image-13.png)

キーワードで調べる

```
man -k <キーワード>
```

![alt text](image-14.png)

()内の数字はセクション番号である
下記は各セクション番号の意味

![alt text](image-15.png)


セクジョンで調べる

```
man <セクション番号> <名前>
```

![alt text](image-16.png)


セクション番号のリスト表示

![alt text](image-17.png)
