Setup Docker Laravel 10 com PHP 8.1
Assine a Academy, e Seja VIP!

Passo a passo
Clone Repositório

git clone -b laravel-10-com-php-8.1 https://github.com/especializati/setup-docker-laravel.git app-laravel
cd app-laravel
Crie o Arquivo .env

cp .env.example .env
Atualize as variáveis de ambiente do arquivo .env

APP_NAME=EspecializaTi
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=nome_usuario
DB_PASSWORD=senha_aqui

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
Suba os containers do projeto

docker-compose up -d
Acesse o container app

docker-compose exec app bash
Instale as dependências do projeto

composer install
Gere a key do projeto Laravel

php artisan key:generate
Acesse o projeto http://localhost:8989
