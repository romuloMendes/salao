## Getting started

Para facilitar o seu início com o Salão project.


## Configurando .env
```
cp .env.example .env
```

## Initialization project docker
```
git clone https://github.com/laradock/laradock.git
cd laradock
cp .env.example .env
docker-compose up -d nginx mysql
docker-compose exec workspace bash
composer install
php artisan key:generate
sudo chmod 777 -R storage
exit
```

## Abra o arquivo .env do seu projeto e defina o seguinte:
```
DB_HOST=mysql
REDIS_HOST=redis
QUEUE_HOST=beanstalkd
```

## Create database:
```
CREATE DATABASE laravel;
```

## Abra o arquivo .env do seu projeto e defina o seguinte:
```
DB_PASSWORD=root
```

## Create migrate:
```
docker-compose exec workspace bash
php artisan migrate:refresh
```

## Start server project:
```
cd laradock
docker-compose up -d nginx mysql
```

## Stop server project:
```
cd laradock
docker-compose down 
```
