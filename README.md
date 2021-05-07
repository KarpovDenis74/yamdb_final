# api_yamdb
Проект api_yamdb реализует API-сервис проект YATUBE
- авторизация пользователей
- запрос информации из базы проекта
- запись информации в базу проекта
подробнее о реализованных запросах можно посмотреть в файле templates/redoc.html

Запуск 
1. развернуть образ из docker-файла
2. Сделать миграции
docker-compose exec web python manage.py makemigration
docker-compose exec web python manage.py migrate --noinput
3. Создать суперпользователя
docker-compose exec web python manage.py createsuperuser
4. Собрать статику проекта 
docker-compose exec web python manage.py collectstatic --no-input 