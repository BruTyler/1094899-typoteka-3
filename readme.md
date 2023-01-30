# Личный проект «Типотека» [![Build status][travis-image]][travis-url]

Для запуска проекта:
1. Необходим инстанс Postgresql
1.1 Локально развернутый Postgresql
1.2 Или Установить Docker и воспользоваться скриптами в проекте

npm run start-db-docker

Будет скачан образ postgresql и смонтирован volume для хранения данных, запущен контейнер для дальнейшей работы

npm run stop-db-docker

Остановит контейнер

2. Конфигурирование окружения - необходимо создать в корне проекта файл с настройками ".env"
Описание настроек приведено в environments.md

3. Первичное наполнение БД данными и пользователями
npm run start --- --filldb 10

где 10 - количество статей (необязательный параметр)

4. Запуск серверов

npm run start-servers

Запуск фронтенд и api серверов из 1 консоли.
или запуск серверов в отдельных консолях:

npm run start-front-server:dev
npm run start-api-server:dev

5. Адреса серверов после заапуска:
http://localhost:8080/ - фронтенд сервер
http://localhost:3000/ - api сервер

6. Запуск тестов
npm run test
