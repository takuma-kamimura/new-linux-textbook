### シェルスクリプトの活用

![alt text](image.png)

- シェルスクリプトの欠点

`大規模システムのプログラミング`

`高速性が必要な処理`

### 演習1　日記を書くためのシェルスクリプト

![alt text](image-1.png)

![alt text](image-2.png)

### 演習2 指定したパスは以下のファイル一覧表示

![alt text](image-5.png)

![alt text](image-3.png)

![alt text](image-4.png)

![alt text](image-6.png)

- IFS　内部フィールド区切り文字

![alt text](image-7.png)

![alt text](image-8.png)

![alt text](image-9.png)

`スペースで区切らせないようにIFSの値からスペースを抜いておく`

![alt text](image-10.png)

上では「IFS」に`改行`を代入しておく

![alt text](image-11.png)

- IFSのバックアップ

![alt text](image-12.png)

### 演習3 検索コマンド

![alt text](image-13.png)

- xargsコマンド - 標準入力からコマンドラインを組み立てて実行する

xargsは標準入力として「引数リスト」を与えます

![alt text](image-14.png)

![alt text](image-15.png)

![alt text](image-16.png)

![alt text](image-17.png)

- xargsを利用してgrep

![alt text](image-18.png)

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

![alt text](image-22.png)

![alt text](image-23.png)

![alt text](image-24.png)

- 指定できる項目を増やして実用的に

![alt text](image-25.png)

![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)

- ヘルプの表示

![alt text](image-29.png)

![alt text](image-30.png)

![alt text](image-31.png)

- エラーメッセージの表示

![alt text](image-32.png)

![alt text](image-33.png)

完成したシェルスクリプト「findgrep.sh」

![alt text](image-34.png)

![alt text](image-35.png)

