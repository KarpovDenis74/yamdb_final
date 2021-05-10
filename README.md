# yamdb_final
Текущий статус github.actions:
https://github.com/KarpovDenis74/yamdb_final/actions/workflows/yamdb_workflow/badge.svg



Проект yamdb_final реализует API-сервис проекта YATUBE
- авторизация пользователей
- запрос информации из базы проекта
- запись информации в базу проекта
подробнее о реализованных запросах можно посмотреть в файле templates/redoc.html

Проект реализоан на фреймворке Django
Фреймворк Django rest framework использован для реализации REST API

Посмотреть проект можно по адресу http://84.201.141.161
Примеры можно посмотреть по следующим эндпойнтам:
    http://84.201.141.161/admin/
    http://84.201.141.161/redoc/

Автор: Карпов Денис






Запуск 
1. развернуть образ из docker-файла
2. Сделать миграции
docker-compose exec web python manage.py makemigration
docker-compose exec web python manage.py migrate --noinput
3. Создать суперпользователя
docker-compose exec web python manage.py createsuperuser
4. Собрать статику проекта 
docker-compose exec web python manage.py collectstatic --no-input