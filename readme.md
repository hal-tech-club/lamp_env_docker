# LNMP (Linux + Nginx + MySQL + PHP)環境構築用Docker-Compose

## ■構成

Nginx(1.11) + MySQL(5.7) + PHP(7.2) + phpMyAdmin

## ■各ページへのアクセス

|name|url|
|:-|:-|
|html|http://localhost:8080/|
|phpMyAdmin|http://localhost:4001/|

## ■利用方法

1. `$ git clone git@github.com:hal-tech-club/lamp_env_docker.git`
2. `$ cd lamp_env_docker`
3. docker-compose.ymlの`MYSQL_DATABASE`等を適当なものに変える
4. `$ docker-compose ud -d`

作業は基本的に/htmlから開き直して行う。  
画面上から直接アタッチすることができるエディタ or IDE推奨。(VSCodeもしくはPhpStorm等)

`$ docker-compose up -d`をし直したい場合は、  
先にvolume外出しによって永続化されている/mysql以下のファイルを手動で全消ししてください。

## ■Q&A

Q, PHPの授業でも使いたい  
A, ご自由にどうぞ

Q, そもそもこれって何がしたいの？  
A, MAMPやXAMPPを使うことによる弊害を回避 & 各メンバーが持つ実行環境の共通化

Q, Nginxを使っている理由は？  
A, Apacheコンテナだとなぜかルーティングファイルの設定が弄れなかった為。  
　特に利用上での違いはないので無視してOK

Q, dockerfileにある内容だけじゃツール周りが足りない  
A, 自分で追加して修正(このリポジトリにcommit)してください

Q, docker-compose.ymlが初期設定のまま`$~ up -d`してしまった…  
A, 修正して`$~ down`して`$~ up -d`しましょう

Q, PHPの環境情報が見たい  
A, /html下に```<?php phpinfo();```と書いたPHPファイルを作って確認してください

Q, phpMyAdmin以外のDBクライアントが使いたい  
A, host: localhost, port: 13306 で接続してください
