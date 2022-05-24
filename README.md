## About

掲示板アプリケーション

## 使い方

npm パッケージのインストール

```
npm i
```

MySQLのDockerコンテナの接続先を設定
- .env
```
DATABASE_URL="mysql://root:okarin@hostname:3306/bulletin-board-db"
```

prismaの初期化

```
npx prisma migrate dev --name init

npx prisma generate
```

ビルド

```
npx tsc --build
```

サーバーの実行

```
node ./dist/server.js
```


## URI 設計

| メソッド | パスとクエリ | 処理               |
| -------- | ------------ | ------------------ |
| GET      | /posts       | 投稿一覧           |
| POST     | /posts       | 投稿とリダイレクト |
| POST     | /posts?{id}  | 削除               |
| POST     | /login       | ログイン           |
| GET      | /logout      | ログアウト         |

## テーブル設計

/prisma/migration/schema.prisma を参照
