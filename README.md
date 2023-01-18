# Dokcerを使用したRailsの環境構築
- Dockerfileを作成する
  - Railsアプリのコンテナイメージを作成するため
- Gemfileを作成する
- 空のGemfile.lockを作成する
- docker-compose.ymlを作成する
  - Railsアプリのコンテナとdbコンテナを同時に実行・停止・破棄するため
- プロジェクトのビルド
```bash
docker-compose run web rails new . --force --database=postgresql
```
- データベースの接続設定
  - dbコンテナに接続するようにdatabase.ymlを書き換える
- アプリの起動
```bash
docker-compose up
```
- db作成
```bash
docker-compose run web rake db:create
```


# 参考
https://docs.docker.jp/compose/rails.html?highlight=rails
