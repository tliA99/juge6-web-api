# juge6-web-api

軽量な Play Framework (Scala) ベースの Web API サンプル/プロジェクトです。

**概要**
- **プロジェクト名**: `juge6-web-api`
- **言語 / フレームワーク**: Scala, Play Framework
- **目的**: サンプルのコントローラ、ビュー、設定を含む Web アプリケーション／API の参考実装

**リポジトリ構成（抜粋）**
- `app/` : Play アプリケーションのソース（`controllers`, `views`）
- `conf/` : `application.conf`, `routes` 等の設定
- `public/` : 静的アセット（JS/CSS/画像）
- `test/` : ScalaTest などのユニットテスト（例: `test/controllers/HomeControllerSpec.scala`）
- `build.sbt` : sbt ビルド定義
- `docker/scala/Dockerfile` : Scala/Play 用の Dockerfile
- `docker-compose.yml` : 開発用の Docker Compose 構成

要件
- Java JDK 8 以上（プロジェクトで使用されているバージョンに合わせてください）
- sbt
- （Docker を使う場合）Docker と docker-compose

ローカルでの実行（sbt）
PowerShell での例:

```powershell
# 依存解決と起動
sbt run

# テストを実行
sbt test
```

Docker を使った実行
- Docker と docker-compose がインストールされていることを確認してください。

```powershell
# ビルドしてコンテナ起動
docker-compose up --build

# バックグラウンドで起動
docker-compose up -d --build

# コンテナ停止
docker-compose down
```

設定
- アプリケーション設定は `conf/application.conf` にあります。開発環境や本番環境に合わせて編集してください。

テスト
- 単体テストは `sbt test` で実行します。テストは `test/` 配下にあります。

開発のヒント
- Play のホットリロードを利用するとソース変更後すぐに反映されます（`sbt run` 実行中）。
- ルート定義は `conf/routes` を確認してください。

貢献
- Issue や Pull Request は歓迎します。小さな改善やドキュメントの修正も助かります。

ライセンス
- 本リポジトリにライセンスファイルが含まれていない場合は、使用前にリポジトリのオーナーに確認してください。

その他
- 質問や実行で問題が出たら、使用している Java / sbt / Docker のバージョン情報とともに Issue を作成してください。

---

作成日: 2025-12-06
