# docker-compose デモ
- 以下のようにコンテナを立ち上げる
- コンテナが立ち上がると src/public/ 以下が localhost に公開される
- `docker-compose exec` コマンドでコンテナに入ることもできる

```bash
$ docker-compose build
$ docker-compose up -d
// コンテナが立ち上がり、ブラウザから http://localhost で確認できるようになる
$ docker-compose exec cgi bash
// コンテナに入りシェルを立ち上げ
[container] $ root@xxxxxxxx:/var/www#
```

# 注意点
- PHP の Dockerfile は最小限のため、PDO などの外部モジュールがインストールされていない
