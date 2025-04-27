# エイリアス

エイリアスとは既存のコマンドに別名をつけて実行できるようにカスタマイズできるようにすること

ls -F オプションの挙動
![alt text](image.png)


ls -Fオプションのエイリアスの設定
```
$ alias ls='ls -F'
```

エイリアス設定後の実行結果

![alt text](image-1.png)

エイリアスを設定する方法
```
alias <名前>='<コマンド>'
```

- エイリアスの確認と削除
![alt text](image-2.png)

- エイリアスの削除
```
$ unalias ls
```

### エイリアスを一時的に無効にする

一時的にエイリアスを無効にする方法は3通りある

- フルパスで指定する
```
$ /bin/ls
```

- commandを使う
```
$ command ls
```

- /を先頭につける
```
$ /ls
```

# bashのオプション
bashではシェルが持つ様々な機能を利用するためにオプションを指定することができる。
オプションは一つの機能につきオン/オフで有効・無効の切り替えができる

- setコマンド
```
set -o/+o <オプション>
```
-oでオプションがオン。+oでオプションがオフ


![alt text](image-3.png)

![alt text](image-4.png)

- shoptコマンド

```
shopt -s/-u <オプション名>
```

-sで指定したオプションをオン、-uで指定したオプションをオフ
オプション名はsetでしているものとは異なる
![alt text](image-5.png)

![alt text](image-6.png)

### シェル変数
シェル変数とはbash内部で使用される変数
様々な値を設定できる

- 変数の設定
```
<変数名>=<値>
```

![alt text](image-7.png)
![alt text](image-8.png)
![alt text](image-9.png)

- PS1 - プロンプト設定
コマンドラインの「$」表記を変更する

![alt text](image-10.png)

![alt text](image-11.png)

/wはカレントディレクトリを表す。これを設定しておくとpwdコマンドを叩かなくてもプロンプトを見るだけでカレントディレクトリがわかる
![alt text](image-12.png)

![alt text](image-13.png)

プロンプトが横に長すぎる場合は`\n`で途中で改行できる
![alt text](image-14.png)

- PATH - コマンド検索パス

![alt text](image-15.png)

- LANG - ロケール

インストール時に日本語で指定した場合はbashのエラーメッセージは

![alt text](image-16.png)

![alt text](image-17.png)

![alt text](image-18.png)

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

- その他のシェル変数

![alt text](image-22.png)

![alt text](image-23.png)

![alt text](image-24.png)

### 環境変数

ファイルシステム上に存在するコマンドを`外部コマンド`
シェル自体に存在しているコマンドを`組み込みコマンド`

![alt text](image-25.png)

![alt text](image-26.png)

![alt text](image-27.png)

catは外部コマンド
![alt text](image-28.png)

- 現在シェルに設定されている環境変数を表示には`printenv`コマンド

![alt text](image-29.png)

- exportコマンドコマンド - 環境変数の設定

指定した変数を環境変数として設定
```
export <シェル変数>
```

![alt text](image-30.png)

![alt text](image-31.png)

### bashの設定ファイル

![alt text](image-32.png)

![alt text](image-33.png)

- 設定ファイルの変更時の注意
設定を行うシェルとは別にもう一つのシェルを起動しておく

![alt text](image-34.png)

![alt text](image-35.png)

![alt text](image-36.png)

![alt text](image-37.png)

- コメント
`コメント`とは動作には関係ないメモ書きのこと
![alt text](image-38.png)

- bashのカスタマイズ例
![alt text](image-39.png)