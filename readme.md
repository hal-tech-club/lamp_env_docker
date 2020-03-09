# LNMP (Linux + Nginx + MySQL + PHP)環境構築用Docker-Compose

## 構成

Nginx(1.11) + MySQL(5.7) + PHP(7.2) + phpMyAdmin

## 各ページへのアクセス

|name|url|
|:-|:-|
|html|http://localhost:8080/|
|phpMyAdmin|http://localhost:4001/|

## 利用方法

1. `$ git clone git@github.com:hal-tech-club/lamp_env_docker.git`
2. `$ cd lamp_env_docker`
3. docker-compose.ymlの`MYSQL_DATABASE`等を適当なものに変える
4. `$ docker-compose ud -d`

作業は基本的に/htmlから開き直して行う。  
画面上から直接アタッチすることができるエディタ or IDE推奨。(VSCodeもしくはPhpStorm等)
