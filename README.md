# Windows 10 の Docker コンテナ環境をきれいにする
## 開発環境
- Windows 10 Home Ver. 1909
- Docker Toolbox

## 起動中のコンテナの確認
docker ps でプロセスの状態を確認

```console
docker ps
```
## 停止中のコンテナの削除

docker rm コンテナIDもしくはコンテナ名 ですべてのコンテナを削除できます。

次のコマンドは、docker ps -q で全コンテナのIDを取得し、それをdocker rm に渡しているコマンドです。

```console
docker rm $(docker ps -aq)
```

実行結果例：
```
330ddbe7aee0
8aef7f9046fa
a542eca70416
5225b7609af9
c495fdee1b2b
0fd1dd889b0a
0f68c8d2e932
c44cde856cf2
```

## イメージの削除

docker images でローカルに保存されている全てのイメージを表示できます。

```console 
docker images
```

```
REPOSITORY                                           TAG                 IMAGE ID            CREATED             SIZE
aspnetcorejwtvue_db                                  latest              951174b03a8c        3 months ago        1.35GB
disaster-stock-master-app_db                         latest              951174b03a8c        3 months ago        1.35GB
disasterstockmaster_db                               latest              951174b03a8c        3 months ago        1.35GB
mssqlserverlinux_db                                  latest              77415daff16b        3 months ago        1.35GB
explainhow_to_start_dotnet_apiwith_efwith_mssql_db   latest              ca683416b3b3        3 months ago        1.35GB
<none>                                               <none>              54846e230fdd        3 months ago        1.35GB
<none>                                               <none>              040216db7bb4        3 months ago        1.35GB
<none>                                               <none>              662778c57f37        3 months ago        1.35GB
<none>                                               <none>              5056808239a9        3 months ago        1.35GB
mssql-server-linux-sample_db                         latest              e10d64f06cd0        3 months ago        1.35GB
<none>                                               <none>              1e921655411b        3 months ago        1.35GB
<none>                                               <none>              2a74262944cf        3 months ago        1.35GB
<none>                                               <none>              e5c6fcdd8623        3 months ago        1.35GB
<none>                                               <none>              c3f398f5c824        3 months ago        1.35GB
<none>                                               <none>              0924d659d556        3 months ago        1.35GB
<none>                                               <none>              31ec89abbb29        3 months ago        1.35GB
docker-compose-laravel-lemp_backend                  latest              cd771e279fba        4 months ago        481MB
calender-app_api                                     latest              fa5ac8abaaf6        4 months ago        89.3MB
calender-app_nginx                                   latest              13dbc2293f61        4 months ago        133MB
php                                                  7.4-fpm             89cffc06d538        4 months ago        405MB
mac_app                                              latest              a80d1a1fe4b7        4 months ago        423MB
nginx-php-mysql-docker-compose_app                   latest              a80d1a1fe4b7        4 months ago        423MB
php-for-android-firebase-notification_app            latest              a80d1a1fe4b7        4 months ago        423MB
mysql                                                5.7                 ef08065b0a30        4 months ago        448MB
mysql                                                8.0                 e1d7dc9731da        4 months ago        544MB
mysql                                                latest              e1d7dc9731da        4 months ago        544MB
adminer                                              latest              b0101225da58        4 months ago        90.5MB
mariadb                                              latest              b28df07deb6c        5 months ago        407MB
nginx                                                alpine              6f715d38cfe0        5 months ago        22.1MB
nginx                                                latest              4bb46517cac3        5 months ago        133MB
node                                                 lts-alpine          18f4bc975732        6 months ago        89.3MB
php                                                  7.4.0-fpm           0203f6c79234        13 months ago       405MB
microsoft/mssql-server-linux                         2017-latest         314918ddaedf        2 years ago         1.35GB
microsoft/mssql-server-linux                         latest              314918ddaedf        2 years ago         1.35GB
```
