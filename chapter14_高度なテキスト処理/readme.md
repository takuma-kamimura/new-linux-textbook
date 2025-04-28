### sedコマンド

- 非対話型エディタとは

![alt text](image.png)

![alt text](image-1.png)

- sedコマンドの形式

![alt text](image-2.png)

![alt text](image-3.png)

![alt text](image-4.png)

`行を削除するd`
`行を表示するp`
`行を置換するs`

- 行を削除する

![alt text](image-5.png)

![alt text](image-6.png)

![alt text](image-7.png)

全行の削除は`d`

正規表現は下記
![alt text](image-8.png)

- 行を表示する

![alt text](image-9.png)

![alt text](image-10.png)

- 行を置換する

![alt text](image-11.png)

![alt text](image-12.png)

![alt text](image-13.png)

`見つかった全ての文字列を置換するにはgコマンド`

![alt text](image-14.png)

![alt text](image-15.png)

`置換後文字列を指定しない場合は空文字となる`

![alt text](image-16.png)

![alt text](image-17.png)

- 後方参照

`マッチした文字列を置換後に埋め込みたいケース`

![alt text](image-18.png)

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

![alt text](image-22.png)

### awkコマンド

パターン検索・処理言語
- awkコマンドの形式

```
パターン { アクション }
```

![alt text](image-23.png)

![alt text](image-24.png)

![alt text](image-25.png)

- prontとフィールド変数

特定のフィールドを抽出して表示するという列選択

![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)

![alt text](image-29.png)

![alt text](image-30.png)

![alt text](image-31.png)

- パターン指定

![alt text](image-32.png)

![alt text](image-33.png)

- アクションの省略

![alt text](image-34.png)

- 実践例 csvファイルからスコア集計

![alt text](image-35.png)

![alt text](image-36.png)

![alt text](image-37.png)

![alt text](image-38.png)

![alt text](image-39.png)

![alt text](image-40.png)

