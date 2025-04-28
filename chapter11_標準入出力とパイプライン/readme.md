### 標準入力、標準出力、標準エラー出力
![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

### リダイレクト

- 表中入力のリダイレクト

![alt text](image-3.png)

![alt text](image-4.png)

![alt text](image-5.png)

- 標準出力のリダイレクト

コマンドの実行結果を画面でなくファイルに保存したい場合

![alt text](image-6.png)

- 標準エラー出力
![alt text](image-7.png)

![alt text](image-8.png)

![alt text](image-9.png)

`標準出力とエラー出力は別々のチャネルになっている`

![alt text](image-10.png)

![alt text](image-11.png)

![alt text](image-12.png)

標準出力と標準エラー出力をまとめる

![alt text](image-13.png)

![alt text](image-14.png)


- リダイレクトによる上書き
![alt text](image-15.png)

![alt text](image-16.png)

![alt text](image-17.png)

- /dev/null

![alt text](image-18.png)


### パイプライン

`コマンドの標準出力を別のコマンドの標準入力に繋げる`

![alt text](image-19.png)

```
<コマンド1>| <コマンド2> | <コマンド3>
```

![alt text](image-20.png)

![alt text](image-21.png)

![alt text](image-22.png)

コマンドライン履歴をlessで読む
```
$ history | less
```

![alt text](image-23.png)

![alt text](image-24.png)

### フィルター

- フィルタの例 - headコマンド

![alt text](image-25.png)

![alt text](image-26.png)


- コマンドの組み合わせ例
```
du [オプション] [ファイル/ディレクトリ]
```

![alt text](image-27.png)

![alt text](image-28.png)

![alt text](image-29.png)

![alt text](image-30.png)

![alt text](image-31.png)

