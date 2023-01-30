# fastAPI-veutify-template
FastAPI+Vuetify+Nginx+Dockerのテンプレート

## DevContainer でリポジトリを開く
1. リポジトリをクローン後、VSCodeで開く
2. コマンドパレットで DevContainers: Reopen Folder Locally を選択


## 環境構築
1. ビルド&起動
```
$ docker compose -f docker-compose.dev.yml --build
```

2. http://localhost:3000 にアクセス(viteの開発環境へのアクセス)

3. フロント側のビルド
```
docker compose exec front yarn build
```

4. http://localhost:8000 にアクセス(NGINXによる本番環境へのアクセス)