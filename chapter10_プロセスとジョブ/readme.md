### プロセスとは

`メモリ上で実行状態にあるプログラム`のこと

- psコマンド - プロセスの表示
![alt text](image.png)

![alt text](image-1.png)

- 現在のターミナル以外のプロセスも表示する
![alt text](image-2.png)

- オプション形式
![alt text](image-3.png)

- 全てのプロセスを表示
![alt text](image-4.png)

`Linuxはマルチタスク機能により、様々なプロセスが同時に動作している`

- よく使われるオプション
![alt text](image-5.png)

### ジョブとは

`シェルから見た処理の単位のこと`

![alt text](image-6.png)

![alt text](image-7.png)

- コマンドを一時停止する
![alt text](image-8.png)

![alt text](image-9.png)

- fgコマンド - ジョブをフォアグラウンドにする

ジョブを停止状態から、ユーザーが対話的に操作できる元の状態に戻す
これをフォアグラウンドという
```
fg %<ジョブ番号>
```

![alt text](image-10.png)

![alt text](image-11.png)

![alt text](image-12.png)


- bgコマンド - ジョブをバックグラウンドにする


![alt text](image-13.png)

　以上の場合はバックグラウンドで処理を継続したままシェルへ戻ってこれると便利

```
bg %<ジョブ番号>
```

![alt text](image-14.png)

![alt text](image-15.png)

![alt text](image-16.png)

![alt text](image-17.png)

![alt text](image-18.png)

### ジョブ・プロセスの終了

フォアグラウンドジョブの終了
![alt text](image-19.png)
上はバックグラウンドジョブは停止できない

```
kill %<ジョブ番号>
```

![alt text](image-21.png)

![alt text](image-22.png)

![alt text](image-23.png)

- プロセスの終了

```
kill <プロセス　ID>
```

![alt text](image-24.png)

![alt text](image-20.png)
![alt text](image-25.png)

- killコマンド - シグナルを送信する

`killはコマンドではなくシグナルを送信するコマンド`

下記は全て同じ意味
![alt text](image-26.png)
![alt text](image-27.png)

