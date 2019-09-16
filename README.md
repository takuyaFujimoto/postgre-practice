# postgre-practice

### 事前に用意するもの
1. gitをインストール `git --version`叩いて結果が返ってくれば問題ない。
2. dockerとdocker-composeをインストール docker for windowsが安定していておすすめ
https://ops.jig-saw.com/techblog/docker-for-windows-install/

### コマンド解説
<img width="1680" alt="スクリーンショット 2019-09-16 23 53 47" src="https://user-images.githubusercontent.com/42311219/64968954-fd446200-d8dd-11e9-9ce0-daeada2b3e71.png">

1. `mkdir practice`　作業ディレクトリの作成
2. `cd practice`　作業ディレクトリに移動
3. `git clone -b develop https://github.com/takuyaFujimoto/postgre-practice.git`　資産の取得
4. `cd postgre-practice` 資産のディレクトリに移動
5. `docker-compose up -d` コンテナの立ち上げ
6. `docker-compose ps` コンテナの状態確認

### 接続情報
`localhost:5050`にアクセス
1. id: root password:root

![スクリーンショット 2019-09-08 4 08 19](https://user-images.githubusercontent.com/42311219/64479198-91cc0780-d1ee-11e9-97b4-66cee4eba8af.png)

<img width="1680" alt="スクリーンショット 2019-09-16 23 49 05" src="https://user-images.githubusercontent.com/42311219/64969435-dd616e00-d8de-11e9-925b-f9d2ab4899ba.png">

2. host-name: postgresql port 5432

![スクリーンショット 2019-09-08 4 12 51](https://user-images.githubusercontent.com/42311219/64479244-364e4980-d1ef-11e9-86a7-614690f181e9.png)

### その他情報
1. ツール -> クエリツールからSQL用のエディタが出せる

### docker for windowsのバグ
マウントが上手くいかなくて落ちるのでその場合はymlファイルの9行目の
`- ./database:/var/lib/postgresql/data`を
`- ./database:/var/lib/postgresql`に変更してトライしてください。

