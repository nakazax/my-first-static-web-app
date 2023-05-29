# my-first-static-web-app
Static Web Apps と Data API Builder のテスト用のリポジトリ

## Data API Builder のローカル実行方法
- 参考
    - https://learn.microsoft.com/ja-jp/azure/data-api-builder/data-api-builder-cli
    - https://learn.microsoft.com/ja-jp/azure/data-api-builder/get-started/get-started-azure-cosmos-db

### Static Web Apps CLI インストール
```bash
npm install
```

### Data API Builder のインストール
```bash
dotnet tool install --global Microsoft.DataApiBuilder"
```

### Cosmso DB の接続文字列を環境変数に設定
```bash
export DATABASE_CONNECTION_STRING='AccountEndpoint=https://cosmos-lingoai-dev.documents.azure.com:443/;AccountKey=xxx==;'
```

```bash
cd swa-db-connections && dab start --config staticwebapp.database.config.json
```

### GUI での GraphQL 開発
以下にアクセス、SSL証明書に関するエラーが出るが無視して問題ない

https://127.0.0.1:5001/graphql/