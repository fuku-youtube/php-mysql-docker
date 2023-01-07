FROM php:8.1.12-apache

# コンテナ内でパッケージをインストールできる
# mysqlに接続するためのパッケージをインストールするコマンド
RUN apt update  \
  && docker-php-ext-install pdo_mysql

COPY src/ /var/www/html/