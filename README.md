# Django simple landing project

### Для запуска требуется Postgresql >13 версии, и Python >3.9 версии.

### Подключение к PostgreSQL прописывается в landing/settings.py файле.


*Создаем виртуальную среду Python*

```
python3 -m venv landing_venv && source landing_venv/bin/activate
pip3 -i requirements.txt
```

*После запуска PostgreSQL необходимо произвести миграции в БД PostgreSQL*

```
python manage.py migrate
python manage.py makemigrations
```

*Создаём администратора для доступа к админке по адресу хост:порт/admin*

```
python manage.py createsuperuser
```

*Запускаем dev-сервер*
```
python manage.py runserver 127.0.0.1:8000 
```
<sub>Хост и порт опционально</sub>

Также можно сбилдить Docker-образ с помощью команды
```
docker build -f Dockerfile -t landing_django:v0.1 .
```

<hr></hr>

### Готовый простой лэндинг

![alt text](https://github.com/sarekuwa/django_landing/blob/main/github_img/img.png)

<hr></hr>
