# fastAPI-veutify-template
FastAPI+Vuetify+Nginx+Dockerのテンプレート

## 環境構築
1. ビルド&起動
```
$ docker compose up -d --build
```

2. http://localhost:3000 にアクセス(viteの開発環境へのアクセス)

3. フロント側のビルド
```
docker compose exec front yarn build
```

4. http://localhost:8000 にアクセス(NGINXによる本番環境へのアクセス)