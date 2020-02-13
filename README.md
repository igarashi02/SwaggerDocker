# SwaggerDocker

docker-composeでSwaggerの開発環境を用意する。

## 概要
srcディレクトリ内の分割されたSwaggerファイルを更新するとswagger-watchコンテナが変更を検知して分割ファイルをマージし、distディレクトリに書き出す。  
swagger-ui, swagger-apiコンテナはdistディレクトリを参照し、Swaggerファイルを元に、APIドキュメントとモックサーバを起動する。  

分割したSwaggerファイルをvimで編集して、自動マージしてWebUIでAPI仕様を確認するためのもの。  

## コマンド一覧
起動  
`$ docker-compose up -d`

停止  
`$ docker-compose down`

ログ  
`$ docker-compose logs -f swagger-watch`  
swagger-watchはコンテナ名  

## コンテナ一覧
### swagger-editor
WebUIでSwaggerファイルを編集できる。  
Port: 8081

### swagger-ui
WebUIでSwaggerのAPI仕様を確認できる。  
Port: 8082

### swagger-api
Swaggerファイルを元に実際に実行できるAPIモックを作成。  
Port: 8083

### swagger-watch
分割したSwaggerファイルを検知して結合する。  
