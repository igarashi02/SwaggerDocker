# SwaggerDocker

docker-composeでSwaggerの開発環境を用意する。

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
