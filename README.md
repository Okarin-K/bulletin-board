## About

掲示板アプリケーション

## 使い方

npm パッケージのインストール

```
npm i
```

ビルド

```
npx tsc --build
```

サーバーの実行

```
node ./dist/server.js
```

以上  
npm scripts の定義は後日やります

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
