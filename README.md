[![.github/workflows/main.yml](https://github.com/inferno681/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/inferno681/kittygram_final/actions/workflows/main.yml)
## Описание:
Сайт для желающих поделиться информацией о своих кошках.
### Возможности:
Публикация имени, цвета, года рождения, фото и достижений своего питомца.
### Инструменты:
- Python - язык программирования, на котором написан проект. [Python документация](https://docs.python.org/3.9/)
- Django - веб-фреймворк для разработки веб-приложений. [Документация](https://docs.djangoproject.com/)
- Django REST framework - библиотека для создания RESTful API на основе Django. [Документация](https://www.django-rest-framework.org/)
- Docker - открытая платформа для разработки, доставки и эксплуатации приложений.[Документация](https://docs.docker.com/)

## Запуск проекта на сервере под управлением ОС Linux:

1. Подготовка виртуального окружения в директории проекта:
```bash
nano .env
```

2. Содержание файла виртуального окружения:
Для корректной работы проекты не изменяйте строки, помеченные '!'
```nano
POSTGRES_USER=django_user (имя пользователя для СУБД)
POSTGRES_PASSWORD=mysecretpassword (пароль пользователя для СУБД)
POSTGRES_DB=django (имя базы данных)
DB_HOST=db (контейнер с базой данных) - !
DB_PORT=5432 (порт для PostgreSQL) - !
SECRET_KEY =... (SECRET_KEY для settings.py)
ALLOWED_HOSTS =127.0.0.1,localhost (список разрешенных хостов)
DEBUG=False (включение или выключение режима отладки)
SQLITE_ACTIVATED=False (Если True, то будет использоваться SQLite вместо PostgreSQL)
```

3. Установка утилиты Docker Compose:
```bash
sudo apt update
sudo apt-get install docker-compose-plugin
```

4. Копирование файла `docker-compose.production.yml` в директорию проекта и запуск Docker Compose:
```bash
sudo docker-compose up
```
## Авторы:
Василий Стакроцкий https://github.com/inferno681
