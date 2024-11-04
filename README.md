# About the application

This is an invironment built for php with Laravel framework.
The app connects to 2 different database; Mysql and Mongdb.
The app is built with docker, so before we start the set up make sure you have docker installed.

# Installation guide

RUN `docker-compose up -d --build`

RUN `docker-compose exec app composer install`

RUN `docker-compose exec app cp .env.example .env`

RUN `docker-compose exec app cp .env.example .env.testing`

RUN `docker-compose exec app php artisan key:generate`

RUN `docker-compose exec app php artisan storage:link`

# DB setup guide

RUN `docker exec -it mysql bash`

RUN `mysql -u root -p`

RUN `root`

RUN `create database my_sql_db;`

RUN `exit;`

RUN `exit;`

RUN `docker-compose exec app php artisan migrate:refresh --seed`

# Run unit Tests

RUN `docker-compose exec app php artisan test`

# Run python script

RUN `docker-compose exec python-app python my_python_script.py`

# Stop Container

RUN `docker-compose down`

# App urls

app url: `http://127.0.0.1:8080/`

phpmyadmin url: `http://127.0.0.1:3400/`

mysql url: `http://127.0.0.1:3306/`
