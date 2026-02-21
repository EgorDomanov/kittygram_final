### Kittygram 
## Описание
Kittygram — это веб-приложение для публикации фотографий кошек, их описаний и достижений.
## Технологии
- Python 3.12
- Django + Django REST Framework
- PostgreSQL
- Docker + Docker Compose
- Nginx
- Gunicorn
- GitHub Actions (CI/CD)
##Проекты доступны онлайн:

- Kittygram:  
  https://wwwteam.work.gd  
- Taski:  
  https://wwwteam.redirectme.net 
## Установка и запуск
# Клонировать репозиторий
git clone https://github.com/<ваш_логин>/kittygram_final.git
cd kittygram_final
# Создайте файл .env в корне проекта
POSTGRES_DB=django
POSTGRES_USER=django_user
POSTGRES_PASSWORD=your_password
DB_HOST=db
DB_PORT=5432
SECRET_KEY=your_secret_key
# Запуск контейнера 
docker compose up -d --build
# Сбор статики 
docker compose exec backend python manage.py migrate
docker compose exec backend python manage.py collectstatic --noinput
## Примеры запросов к API:
>GET — возвращает все подписки пользователя, сделавшего запрос. Возможен поиск по подпискам по параметру search.

>POST — подписать пользователя, сделавшего запрос на пользователя, переданного в теле запроса. При попытке подписаться на самого себя, пользователь должен получить информативное сообщение об ошибке. Проверка должна осуществляться на уровне API.
