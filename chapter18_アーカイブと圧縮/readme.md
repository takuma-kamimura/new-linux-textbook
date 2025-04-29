### アーカイブファイルと圧縮ファイル

複数のファイルやフォルダをまとめたファイルのことをアーカイブ（書庫）

![alt text](image.png)

### tarコマンド ファイルをアーカイブする

- まずは練習用ファイルの準備

![alt text](image-2.png)

![alt text](image-1.png)

- 余談、ブレース展開

```
{<開始位置>..<終了位置>}
```

![alt text](image-3.png)

- アーカイブファイルの作成

```
tar cf <アーカイブファイル> <アーカイブ元のファイルパス>
```

![alt text](image-4.png)

- アーカイブファイルの内容確認

```
tar tf <アーカイブファイル>
```

![alt text](image-5.png)

- アーカイブ展開

```
tar ｘf <アーカイブファイル>
```

![alt text](image-6.png)

- ファイルリストを表示するvオプション

![alt text](image-7.png)

![alt text](image-8.png)

- ファイル属性の保持

`ファイル属性もそのままアーカイブされる`

### gzipコマンド

ファイルを圧縮するコマンド

```
gzip <圧縮元>
```

![alt text](image-9.png)

![alt text](image-10.png)

![alt text](image-11.png)

![alt text](image-12.png)

- 標準出力にgzipファイルを出力

![alt text](image-13.png)

- tarとgzipを組み合わせる

![alt text](image-14.png)

![alt text](image-15.png)

![alt text](image-16.png)

- パイプとリダイレクトによるtar+gzファイルの作成

![alt text](image-17.png)

![alt text](image-18.png)

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

### bzip2コマンド

gzipコマンドよりもさらに圧縮率が高くデータ量をより小さくできる

```
bzip2 <圧縮元ファイル>
```

![alt text](image-22.png)

![alt text](image-23.png)

![alt text](image-24.png)

![alt text](image-25.png)

- tarとbzip2を組み合わせる

`tarでbzip2形式を利用するには、jオプションを利用`

![alt text](image-26.png)

- その他の圧縮形式

bzip2よりもさらに高圧縮率なのがxz形式

![alt text](image-27.png)

### zipコマンド

zipはファイルの圧縮とアーカイブを同時に行うコマンド
linuxではあまり使われないが,macOSやwindowsでよく使われる

![alt text](image-28.png)

- zipファイルの作成

```
zip -r <圧縮ファイル名> <圧縮対象パス>
```

![alt text](image-29.png)

-rオプションは指定したディレクトリ内のファイルをまとめて圧縮する

`zipファイルを作成するときは常に-rオプションを使った方がいい`

![alt text](image-30.png)

![alt text](image-31.png)

-qオプションを利用するとファイル名を表示しないようにする

![alt text](image-32.png)

![alt text](image-33.png)

- パスワード付きzipファイル

![alt text](image-34.png)

![alt text](image-35.png)

