# cobol-todo

COBOLの知識・実践的な開発経験を得ることを目的としたTodoアプリケーション開発リポジトリ。

モダンなWeb技術とCOBOLを組み合わせ、COBOLによる業務ロジックの実装やデータベース操作、Web APIとの連携について学習。

## 技術スタック

### フロントエンド

- **Next.js**
  - TodoアプリケーションのUIを担当
  - ユーザーからの入力・操作を受け付ける
- **TypeScript**
  - フロントエンドの開発言語

### バックエンド

- **NestJS**
  - REST APIの提供
  - リクエストの受け付け・入力値の検証
  - COBOLプログラムの実行・連携
  - フロントエンドとCOBOL間の橋渡し

### 業務処理・データベース操作

- **GnuCOBOL**
  - Todoに関する業務ロジックの実装
  - データベースへの登録・取得・更新・削除
  - SQLを利用したデータベース操作

### データベース

- **PostgreSQL**
  - Todoデータの永続化
  - データベーススキーマ・テーブルの管理

### 開発環境・ツール

- **Docker / Docker Compose**
  - PostgreSQLの開発環境構築
- **pnpm**
  - JavaScript / TypeScriptのパッケージ管理
- **Git / GitHub**
  - ソースコードのバージョン管理
- **Visual Studio Code**
  - 開発エディタ

## アーキテクチャ

```text
[ Next.js ]
     |
     | HTTP / REST API
     v
[ NestJS ]
     |
     | プロセス起動・JSON連携
     v
[ GnuCOBOL ]
     |
     | SQL
     v
[ PostgreSQL ]
```

### 各レイヤーの責務

| レイヤー | 主な責務 |
|---|---|
| Next.js | UI・ユーザー操作 |
| NestJS | API・入力検証・COBOL連携 |
| GnuCOBOL | 業務ロジック・DB操作 |
| PostgreSQL | データ永続化 |

※ NestJSからTodoデータベースを直接操作せず、データの登録・取得・更新・削除はCOBOL側で実行する方針です。

## 開発方針

- COBOLの基本構文から実践的な業務処理まで段階的に学習する
- COBOLとPostgreSQLを連携させる
- COBOLとNestJSを連携させ、Web APIから業務処理を実行できる構成にする
- モダンなWebアプリケーション開発とCOBOLによる業務システム開発の両方を経験する
