php+nodejsの開発環境構築用

1. docker-compose用のenvの設定
```
$ cp env.example .env
$ vi .env
```
```
COMPOSE_PROJECT_NAME=project-name
WWWGROUP=1000
WWWUSER=1000
DB_PASSWORD=project
DB_DATABASE=project
DB_USERNAME=project
DB_PASSWORD=project
```
COMPOSE_PROJECT_NAMEを適用な名前に変更

2. バックエンドとフロントエンドのソースを用意

./app/backend以下にバックエンド用のPHP

./app/forntend以下にフロントエンド用のnodejs


3. コンテナのビルド
```
$ docker-compose up -d --build
```

4. フロントエンドの機能
 4-1. コンテナにログイン
```
$ docker-compose exec php /bin/bash
```
 4-2. フロント側の起動
```
$ cd /var/www/app
$ npm run dev
```
