### バージョン管理システムとは

`ファイルの変更履歴を保存し管理するためのツール`

`ファイルに対して「いつ・誰がどんな目的で・どういう変更を加えたのか」記録して閲覧できるように`

`必要に応じてファイルを過去の状態に巻き戻す`

### Gitのインストールと初期設定

![alt text](image.png)

CentOS Streamの場合のgitインストール

![alt text](image-1.png)

Ubuntuの場合のgitインストール

![alt text](image-2.png)

- gitの初期設定

![alt text](image-3.png)

![alt text](image-4.png)

![alt text](image-5.png)

![alt text](image-6.png)

### 基本的な使い方

- リポジトリの作成

![alt text](image-7.png)

![alt text](image-8.png)

![alt text](image-9.png)

![alt text](image-10.png)

- リポジトリにファイルを追加する

addでリポジトリに履歴として追加

![alt text](image-11.png)


commmitでリポジトリに変更履歴を追加

![alt text](image-12.png)

- 差分の表示と再コミット

![alt text](image-13.png)

![alt text](image-14.png)

![alt text](image-15.png)

オプションをつけずにコミットすると自動でエディターが立ち上がりメッセージの追加を求められるので、書くこと

![alt text](image-16.png)

![alt text](image-17.png)

![alt text](image-18.png)

- 変更履歴を確認する

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

オブジェクト名は40文字もあるため、一意的に定まる位置で省略して良い決まりがある

![alt text](image-22.png)

![alt text](image-23.png)

### ワークツリーとインデックス

![alt text](image-24.png)

![alt text](image-25.png)

![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)

### コミットの単位とインデックス

![alt text](image-29.png)

![alt text](image-30.png)

### 誤りから復旧する

- ワークツリーに対する誤りからの復旧

![alt text](image-31.png)

![alt text](image-32.png)

![alt text](image-33.png)

![alt text](image-34.png)

- 誤ったコミットからの復旧

```
git revert <取り消したいコミットオブジェクト名>
```

![alt text](image-35.png)

### ブランチを使う

![alt text](image-36.png)

![alt text](image-37.png)

![alt text](image-38.png)

新しいブランチの作成

```
git branch <ブランチ名>
```

![alt text](image-39.png)

![alt text](image-40.png)

ブランチを切り替える

```
git switch <移動先ブランチ>
```

![alt text](image-41.png)

![alt text](image-42.png)

![alt text](image-43.png)

![alt text](image-44.png)

![alt text](image-45.png)

![alt text](image-46.png)

![alt text](image-47.png)

```
git merge <マージするブランチ名>
```

![alt text](image-48.png)

![alt text](image-49.png)

![alt text](image-50.png)

ブランチの削除

```
git branch -d <ブランチ名>
```

![alt text](image-51.png)

### リポジトリのバックアップを作成する

![alt text](image-52.png)

![alt text](image-53.png)

```
git push <送信先リポジトリ> <送信元ブランチ>:<送信先ブランチ>
```

![alt text](image-54.png)

リポジトリを複製する

```
git clone <複製元リポジトリ>
```

![alt text](image-55.png)

![alt text](image-56.png)

![alt text](image-57.png)

![alt text](image-58.png)

リポジトリに別名を設定

```
git remote add <別名> <リポジトリパス>
```

慣習として`origin`という名前が使われる

![alt text](image-59.png)

![alt text](image-60.png)

### 二人以上で作業する

![alt text](image-61.png)

共有リポジトリを経由して経由して全ユーザー間で変更の履歴を確認できる

![alt text](image-62.png)

![alt text](image-63.png)

![alt text](image-64.png)

リポジトリの変更を取り込む

```
git fetch <リポジトリ>
```

![alt text](image-65.png)

![alt text](image-66.png)

![alt text](image-67.png)

![alt text](image-68.png)

### 競合を解決する

競合をコンフリクト(conflict)と呼ぶ

![alt text](image-69.png)

![alt text](image-70.png)

![alt text](image-71.png)

### gitのマニュアル

![alt text](image-72.png)

![alt text](image-73.png)

![alt text](image-74.png)

![alt text](image-75.png)

![alt text](image-76.png)

![alt text](image-77.png)

![alt text](image-78.png)

