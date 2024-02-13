# django-compose-template

1. **イメージを作成する(省略可能)**  
```
docker-compose build
```

2. **プロジェクトを作成する**  
```
docker-compose run --rm web django-admin startproject <project_name> .
```

3. **アプリ（機能）を作成する**  
```
docker-compose run --rm web python manage.py startapp <app_name>
```

4. **アプリを起動する**  
```
docker-compose up
```

### 備考
- 適宜settings.pyのデータベース情報を更新する必要がある。
- 初期設定のまま起動すると、db.sqlite3ファイルが自動作成される。
- デタッチドモードで起動する場合はオプションで`-d`をつける
- イメージの作成はrunで自動作成されるため、手順1は省略可能

### MySQLを使う場合
- [Repository](https://github.com/hiroki1242/django-mysql-template/tree/main "django-mysqlのリポジトリ")
