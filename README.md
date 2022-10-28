# yamdb_final
yamdb_final

Status of last Deployment:<br>
<img src="https://github.com/eltimccc/yamdb_final/workflows/yamdb-workflow/badge.svg?branch=master"><br>

### Адрес сайта
http://84.201.128.143/
### Пример запроса
http://84.201.128.143/api/v1/titles/
http://84.201.128.143/redoc/
## Описание
Сайт является - базой отзывов о фильмах, книгах и музыке.
Пользователи могут оставлять рецензии на произведения, а также комментировать эти рецензии.
Администрация добавляет новые произведения и категории (книга, фильм, музыка и т.д.)
Также присутствует файл docker-compose, позволяющий , быстро развернуть контейнер базы данных (PostgreSQL), контейнер проекта django + gunicorn и контейнер nginx
## Как запустить
#Необходимое ПО
Docker: https://www.docker.com/get-started
Docker-compose: https://docs.docker.com/compose/install/

# Инструкция по запуску
Для запуска необходимо из корневой папки проекта ввести в консоль(bash или zsh) команду:

docker-compose up --build
Затем узнать id контейнера, для этого вводим

docker container ls

Зайти в контейнер

docker exec -it <CONTAINER ID> sh

И делаем миграцию БД, и сбор статики

python manage.py migrate
python manage.py collectstatic

После запуска проекта, подробную инструкцию можно будет посмотреть 
по адресу http://84.201.128.143/redoc/

### Автор: Денис: https://github.com/Eltimccc/