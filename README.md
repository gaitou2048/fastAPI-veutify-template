# fastAPI-veutify-template
FastAPI+Vuetify+Nginx+Dockerのテンプレート

## 環境構築
1. コンテナのビルド&起動
```
$ docker compose up -d --build
```

2. 開発環境起動
```
$ docker compose exec front yarn dev
```

3. http://localhost:3000 にアクセス(viteの開発環境へのアクセス)

4. フロント側のビルド
```
docker compose exec front yarn build
```

5. http://localhost:8000 にアクセス(NGINXによる本番環境へのアクセス)