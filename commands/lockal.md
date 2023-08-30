# Главные вопросы:
ural207@mail.ru, gfhjkm_2023 #ADFF2F

# Частые команды:
## Установки
!!!Убедись, что все сохранено!!!
1. docker-compose down -v && docker-compose up --build
2. docker-compose exec backend python manage.py makemigrations
3. docker-compose exec backend python manage.py makemigrations && docker-compose exec backend python manage.py migrate && docker-compose exec backend python manage.py collectstatic --no-input && docker-compose exec backend cp -r /app/static/. /backend_static/static/ && docker-compose exec backend python manage.py createsuperuser
4. docker-compose exec backend python manage.py createsuperuser

 1996  docker build -t umataullin/food_gateway .
 1996  docker build -t umataullin/food_frontend .
 1998  docker build -t umataullin/food_backend .
 1999  cd ..


docker push umataullin/food_frontend && docker push umataullin/food_backend && docker push umataullin/food_gateway

## Удаления и остановки
docker-compose down -v
- docker-compose down
- docker volume prune
- docker system prune -a
- docker system prune --volumes
- sudo kill $(sudo lsof -t -i :80)
- docker compose stop && docker compose up --build
### для очистки всего   одной строкой -
docker stop $(docker ps -qa) && docker rm $(docker ps -qa) && docker rmi -f $(docker images -qa) && docker volume rm $(docker volume ls -q) && docker network rm $(docker network ls -q)
sudo docker stop $(sudo docker ps -qa) && sudo docker rm $(sudo docker ps -qa) && sudo docker rmi -f $(sudo docker images -qa) && sudo docker volume rm $(sudo docker volume ls -q) && sudo  docker network rm $(sudo docker network ls -q)
Остановка всех контейнеров  docker stop $(docker ps -qa)

Удаление всех контейнеров  docker rm $(docker ps -qa)

 Удаление всех образов  docker rmi -f $(docker images -qa)

Удаление всех томов  docker volume rm $(docker volume ls -q)

Удаление всех сетей  docker network rm $(docker network ls -q)


### Удалить все базы данных:
- python manage.py flush

неизвестные команды
- docker-compose rm -v database
- docker-compose run web python manage.py migrate



# Nginx
- sudo service nginx reload



# Ошибки
## Логи
- docker logs --tail <number> <container_id>


# Запуск проекта
- python3.11 -m venv env
- source env/bin/activate
- python -m pip install --upgrade pip
- pip install -r requirements.txt
- pip freeze | grep -v "pkg-resources" > requirements.txt
- python manage.py createsuperuser
- python manage.py runserver

# Миграции
- python manage.py migrate <app_name> <migration_name>
- python manage.py makemigrations <app_name>
- python manage.py migrate <app_name>

# Git
git log
git reset комит в котором изменения совершены
git push --force
