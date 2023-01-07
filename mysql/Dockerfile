FROM mysql:8.0

# データベースを作成するsqlをdockerで実行
# docker-entrypoint-initdb.dにおくと実行してくれる
COPY init.sql /docker-entrypoint-initdb.d/init.sql

# コンテナ内の環境変数を設定
## ルートユーザのパスワード
ENV MYSQL_ROOT_PASSWORD=root
## ユーザ名
ENV MYSQL_USER=test
## ユーザのパスワード
ENV MYSQL_PASSWORD=test
## データベース名
ENV MYSQL_DATABASE=test_db

# ボリューム
VOLUME ./data:/var/lib/mysql