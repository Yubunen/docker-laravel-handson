# MyLaravelProject

## How to startup

`pc>> git clone https://github.com/Yubunen/MyLaravelProject.git`

`pc>> cd MyLaravelProject`

`pc>> docker compose up -d`

`pc>> docker compose exec app bash`

`app>> chmod -R 777 storage bootstrap/cache`

`app>> composer install`

`app>> cp .env.example .env`

`app>> php artisan key:generate`

`app>> php artisan storage:link`

`app>> php artisan migrate`

データベースがある場合は以下を実行
(現在は不必要)\
`app>> php artisan db:seed`

`app>> exit`

## How to ResetAll

`pc>> docker compose down --rmi all --volumes --remove-orphans`
