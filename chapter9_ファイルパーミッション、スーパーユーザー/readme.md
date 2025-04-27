### ファイルオーナーとグループ

ファイルにはオーナーが設定されている
![alt text](image.png)

![alt text](image-1.png)

- グループ
グループとはユーザーをまとめた集まりのこと

![alt text](image-2.png)

### ファイルのパーミッション
主に「誰にどのような操作を許可をするか」という権限設定

![alt text](image-3.png)

![alt text](image-4.png)

![alt text](image-5.png)

![alt text](image-6.png)

![alt text](image-7.png)

![alt text](image-8.png)

![alt text](image-9.png)

- ディレクトリのパーミッション
![alt text](image-10.png)

それぞれの記号はファイルの場合とは違った意味を持つ

![alt text](image-11.png)

![alt text](image-12.png)

ファイルの削除ができるかどうかはディレクトリのパーミッションで決まる
![alt text](image-13.png)

![alt text](image-14.png)

- chmodコマンド - ファイルモードを変更する

```
chmod [ugoa] [+-=] [rwx] <ファイル名>
```

![alt text](image-15.png)

![alt text](image-16.png)

![alt text](image-17.png)

オーナーの書き込み権限を追加
```
$ chmod u+w file.txt
```

![alt text](image-18.png)

グループの書き込み権限を削除
```
$ chmod g-w file.txt
```

![alt text](image-19.png)

複数のユーザーの権限をまとめて指定
```
$ chmod go=r file.txt
```
![alt text](image-20.png)

- 数値モード
数値モードによるパーミッションの変更
```
$ chmod <8進数の数値> <ファイル名>
```
数値モードは`元のパーミッションに関わらず新しいパーミッションの値へと変更する`

![alt text](image-21.png)

![alt text](image-22.png)

![alt text](image-23.png)

例：「rw-r--r--」へのパーミッション変更は「644」
![alt text](image-24.png)

### スーパーユーザー

スーパーユーザーは別名`「rootユーザー」`

- suコマンド - ユーザーを変更する

suコマンドは主にスーパーユーザーに変わるために使う
![alt text](image-25.png)

![alt text](image-26.png)

スーパーユーザーから一般ユーザーへ戻るにはexitを使う

スーパーユーザーへ初期化して切り替えるには以下のコマンド
```
$ su -
```

スーパーユーザーは主にスーパーユーザーでないと実行できないコマンドを実行するために使用する

以下の場合はsudoコマンドを実行
![alt text](image-27.png)

スーパユーザーとしてコマンドを実行する
```
sudo <実行したいコマンド>
```

![alt text](image-28.png)

![alt text](image-29.png)

- sudoコマンドの設定
あるユーザーにsudoコマンドが使えるように設定したい場合は`/etc/sudoers`ファイルで甘露されているので編集する

![alt text](image-30.png)

例えば以下のよううに設定されている箇所がある
![alt text](image-31.png)

「osumi」というユーザーにsudo権限を追加したい場合は以下を追記
```
osumi ALL=(ALL) ALL
```

- visudoコマンド - sudoersファイルを編集する
`直接テキストエディタで開いて編集はNG`
編集間違いがあった場合sudoコマンドが二度と使えなくなる
なので`visudoコマンド`という特別なコマンドを使う

sudoersファイルの編集手順
![alt text](image-32.png)

- suとsudoのどちらを使うか
sudoの方が必要に応じて一つだけコマンドを実行するという形式となっているので`sudo`の方がよく使われる
