# Express Postgres Starter

> Стартовый проект для Node.js с Express и Postgres

## Установка

Запустите `docker-compose up` в корне проекта для запуска сервера.

По умолчанию сервер запускается по адресу `localhost:3000`, порт можно поменять с помощью параметра `API_PORT` в .env файле.

База данных по умолчанию запускается по адресу `localhost:35432` порт можно поменять с помощью параметра `POSTGRES_PORT` в .env файле.

PgAdmin по умолчанию запускается по адресу `localhost:5555` порт можно поменять с помощью параметра `PG_ADMIN_PORT` в .env файле.

Вы можете подключиться к Postgres используя psql клиент или PgAdmin:

```sh
psql postgres://user:pass@localhost:POSTGRES_PORT/db
```

Для избежания возможных ошибок лучше войти внутрь контейнера с помощью команды. 
```sh
docker-compose run app bash
```
И запустите команду для установки зависимостей (на всякий случай)
```sh
npm install
```

## Настройка и управление базой данных

Для работы с миграциями необходимо войти внутрь контейнера с помощью команды. 
```sh
docker-compose run app bash
```

Для работы с бд доступно 3 команды

`npm run migrate up` запуск всех миграций.

`npm run migrate down` откат миграций.

`npm run migrate:create <migration-name>`  создает новый файл миграции в каталоге [./src/migrations](./src/migrations).




