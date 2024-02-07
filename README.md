# django-compose-template

1. **イメージを作成する**  
```
docker build -t <image_name> .
```

1. **プロジェクトを作成する**  
```
docker-compose run --rm web django-admin startproject <project_name> .
```

1. **アプリ（機能）を作成する**  
```
docker-compose run --rm web python manage.py startapp <app_name>
```

1. **アプリを起動する**  
```
docker-compose up
```

### 備考
- 適宜settings.pyのデータベース情報を更新する必要がある。
- 初期設定のまま起動すると、db.sqlite3ファイルが自動作成される。
- デタッチドモードで起動する場合はオプションで`-d`をつける
