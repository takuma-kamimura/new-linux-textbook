### パッケージとリポジトリ

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

### dnfコマンド パッケージ管理

- 基本的な使い方

```
dnf [オプション] <コマンド> <パッケージ名>
```

![alt text](image-3.png)

- パッケージのインストール

```
dnf install <パッケージ名>
```

![alt text](image-4.png)

![alt text](image-5.png)

このあとパッケージのインストール確認画面に移行するのでyを押す
全てyで省略したい場合は下記

![alt text](image-6.png)

- パッケージ間の依存性

![alt text](image-7.png)

- パッケージの削除

```
dnf remove <パッケージ名>
```

![alt text](image-8.png)

- パッケージを探す

```
dnf search <検索ワード>
```

![alt text](image-9.png)

![alt text](image-10.png)

- パッケージ情報表示

```
dnf info <パッケージ名>
```

![alt text](image-11.png)

### aptによるパッケージ管理

```
apt [オプション] [コマンド] [パッケージ名...]
```

- パッケージのインストール

![alt text](image-12.png)

![alt text](image-13.png)

![alt text](image-14.png)

![alt text](image-15.png)

- パッケージ間の依存性

![alt text](image-16.png)

![alt text](image-17.png)

- パッケージの削除

```
sudo apt remove <パッケージ名>
```

![alt text](image-18.png)

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

```
sudo apt purge <パッケージ名>
```

- パッケージを探す

```
apt serch <検索ワード>
```

![alt text](image-22.png)

![alt text](image-23.png)

- パッケージの情報表示

![alt text](image-24.png)

![alt text](image-25.png)

