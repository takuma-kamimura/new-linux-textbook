### シェルスクリプトの基礎知識

- シェルスクリプトの行

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

- 複数行での記述

![alt text](image-3.png)

![alt text](image-4.png)

シェルでの複数行のい記入
以下の状態は「まだコマンドラインが終了していないので入力してください」という状態
これを`セカンダリプロンプト`という

![alt text](image-5.png)

![alt text](image-6.png)

- コメント

「#」を書くとその行をコメントとすることができる

![alt text](image-7.png)

### 変数

通常のプログラムと同じように変数を利用でき、これをシェル変数という。

`変数を参照するには変数名の前に「$」をつける`

![alt text](image-8.png)

![alt text](image-9.png)

- 変数の書き方の注意

`変数に代入時に$は付けない。値を参照したい時だけ`

`=の前後にスペースを入れない`

`変数名に利用できる文字はアルファベットと数値と_(アンダースコア)だけ`

`変数名の区切りを明示する。{}で明示できる`

![alt text](image-10.png)

![alt text](image-11.png)

### クォーティング

`''`か`""`で囲むことによって`スペースも含めて１つの単語とみなされるよう`にできる

![alt text](image-12.png)

クォーティングすることでシェルによるスペースやメタ文字の解釈をさせず、まとめて一つの文字列として扱うことができる

- クォート中の変数展開

![alt text](image-13.png)

![alt text](image-14.png)

### コマンド置換

コマンド置換を利用すれば、コマンドの結果を文字列として取得する

![alt text](image-15.png)

![alt text](image-16.png)

ダブルクォートでの記法

![alt text](image-17.png)

バックコートでの記法

![alt text](image-18.png)

### 位置パラメーター

シェルスクリプトからコマンドライン引数を扱う

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

*を使用するとファイル名が位置パラメーターとして表示される

![alt text](image-22.png)


- 引数の個数

引数の個数は特殊パラメーター$#という変数で参照できる

![alt text](image-24.png)

![alt text](image-23.png)

- 引数全体の参照

`引数を分割させずにまとめて扱うには$@または$*を使う`

![alt text](image-25.png)

![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)

### 制御構造

- if文

条件を評価してその真偽に応じて処理を分岐する

![alt text](image-29.png)

![alt text](image-30.png)

- 記述上の注意点

セミコロンなしの場合はエラー

![alt text](image-31.png)

セミコロンなしでどうしても描きたい場合

![alt text](image-32.png)

![alt text](image-33.png)

if文の後ろにはコマンドを書く

![alt text](image-34.png)

![alt text](image-35.png)

`ちなみに[]はカッコではなくbashのコマンドである`

![alt text](image-36.png)

- コマンドと終了ステータス

![alt text](image-37.png)

終了した場合は0、エラー時は0以外

![alt text](image-38.png)

![alt text](image-39.png)

- if文と終了ステータス

![alt text](image-40.png)

![alt text](image-41.png)

![alt text](image-42.png)

- testコマンドと演算子

![alt text](image-43.png)

- 文字列の比較

![alt text](image-44.png)

![alt text](image-45.png)

- 整数の比較

![alt text](image-46.png)

![alt text](image-47.png)

![alt text](image-48.png)

![alt text](image-49.png)

![alt text](image-50.png)

![alt text](image-51.png)

![alt text](image-52.png)

- 演算子の結合

![alt text](image-53.png)

![alt text](image-54.png)

![alt text](image-55.png)

()で囲むと条件をグループ化できる

![alt text](image-56.png)

- &&と||

![alt text](image-57.png)

![alt text](image-58.png)

![alt text](image-59.png)

if文では&&はand条件となる

![alt text](image-60.png)

逆に||はor条件となる

![alt text](image-61.png)

![alt text](image-62.png)

- シェルスクリプトの終了ステータス

シェルスクリプトの中で最後に実行したコマンドの終了ステータスがシェルスクリプトの終了ステータスとなる

![alt text](image-63.png)

```
exit <終了ステータス>
```

シェルスクリプトが別のプログラムから呼び出された際にエラー処理を行わせることができる

![alt text](image-64.png)

- 演習1

![alt text](image-65.png)

![alt text](image-66.png)

![alt text](image-67.png)

- for文

単語のリストに対して繰り返し処理を行う構文

![alt text](image-68.png)

![alt text](image-69.png)

![alt text](image-70.png)

```
seq <開始値> <終了値>
```

![alt text](image-71.png)

![alt text](image-72.png)

![alt text](image-73.png)

![alt text](image-74.png)

- case文

`指定された文字列がパターンにマッチするか判断しマッチしたパターン対応する処理を行う`

![alt text](image-75.png)

- while文

`指定した条件が真である限り繰り返し処理を行う`

![alt text](image-76.png)

![alt text](image-77.png)

![alt text](image-78.png)

- 算術展開

![alt text](image-79.png)

![alt text](image-80.png)

bashの算術式展開は読みやすく動作が早い

### シェル関数

![alt text](image-81.png)

![alt text](image-82.png)

![alt text](image-83.png)

`関数は上のように利用する場所よりも前に定義しておかなければならない`

- シェル関数内での位置パラメーター

![alt text](image-84.png)

![alt text](image-85.png)

![alt text](image-86.png)

- シェル関数の終了ステータス

```
return <終了ステータス>
```

![alt text](image-87.png)

