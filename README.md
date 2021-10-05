# docker_compose_djangocms_nginx_postgresql_gunicorn

Скачиваем репозиторий в папку в домашней директории. 

### Находясь в ней, запускаем docker-compose: 

> docker-compose -f docker-compose.prod.yml up -d --build

### Запускаем миграцию:

> docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput

### Собираем статику:

> docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear

### Ваше приложение будет по адресу: http://localhost:1337/media/IMAGE_FILE_NAME
