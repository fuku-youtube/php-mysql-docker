# コマンド

## ネットワークを作成
```
$ docker network create php-mysql-network
```

## php

### build(イメージ作成)

```
$ docker build -t php-app .
```

### run(コンテナ作成)

appディレクトリに移動して実行すること！

```
$ docker container run \
-d \
--rm \
-p 8080:80 \
-v "$(pwd)"/src:/var/www/html \
--network php-mysql-network \
--name run-php-app php-app
```

## mysql

### build(イメージ作成)

```
$ docker build -t php-db .
```

### run(コンテナ作成)

```
$ docker container run \
-d \
--rm \
--network php-mysql-network \
--name run-php-db php-db
```
