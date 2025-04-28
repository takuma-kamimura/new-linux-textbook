### grepコマンドと正規表現

文字列を検索する

```
grep [オプション] <検索パターン> <ファイル名>
```

![alt text](image.png)

![alt text](image-1.png)

条件とマッチしない行を表示する場合は-vオプション

![alt text](image-2.png)

別のコマンドの結果をgrepで表示

![alt text](image-3.png)

- 正規表現って何？

条件にマッチする文字列集合を表現する記法

![alt text](image-4.png)

![alt text](image-5.png)

### 文字列にマッチするメタ文字

![alt text](image-6.png)

`t.st`というパターンで検索

![alt text](image-7.png)

`t..st`と書くと任意の２文字になる

![alt text](image-8.png)

.そのものにマッチさせる
![alt text](image-9.png)

- 特定の文字を指定する

![alt text](image-10.png)

![alt text](image-11.png)

![alt text](image-12.png)

![alt text](image-13.png)

### 位置にマッチするメタ文字

![alt text](image-14.png)

![alt text](image-15.png)

### 繰り返しを指定するメタ文字

![alt text](image-16.png)

![alt text](image-17.png)

![alt text](image-18.png)

![alt text](image-19.png)

- 拡張正規表現とは

`-Eオプションを利用すると、拡張正規表現として解釈される`
拡張正規表現とはメタ文字を増やしたもの

![alt text](image-20.png)

![alt text](image-21.png)

- 拡張正規表現による繰り返し回数の指定

`直前の文字は少なくとも一つは必要`

![alt text](image-22.png)

![alt text](image-23.png)

![alt text](image-24.png)

- 繰り返し回数を指定するメタ文字

![alt text](image-25.png)

![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)

- その他のメタ文字

![alt text](image-29.png)

![alt text](image-30.png)

![alt text](image-31.png)

### 正規表現の利用

![alt text](image-32.png)

