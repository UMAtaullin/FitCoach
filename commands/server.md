# docker-compose
sudo docker -f docker-compose.production.yml exec -it foodgram-nginx-1 sh
sudo docker-compose up -d

sudo docker compose -f docker-compose.production.yml down && sudo docker compose -f docker-compose.production.yml up --build -d

sudo docker compose -f docker-compose.production.yml up -d

sudo docker compose -f docker-compose.production.yml exec backend python manage.py makemigrations && sudo docker compose -f docker-compose.production.yml exec backend python manage.py migrate && sudo docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic && sudo docker compose -f docker-compose.production.yml exec backend cp -r /app/static/. /backend_static/static/ && sudo docker-compose -f docker-compose.production.yml run backend python manage.py createsuperuser


# Очистка
sudo docker-compose -f docker-compose.production.yml down
sudo docker-compose -f docker-compose.production.yml down -v
- sudo docker volume prune
- sudo docker system prune -a
sudo kill $(sudo lsof -t -i :80)
npm cache clean --force
sudo apt-get clean
sudo journalctl --vacuum-time=1d


# Nginx
sudo nano /etc/nginx/sites-enabled/default
sudo systemctl reload nginx
- sudo service nginx reload


# Сервер
ssh -i /home/ural/.ssh/Diploma/yc-ataullinural yc-user@158.160.64.245
ssh -i /home/ural/.ssh/yandex/yc-ataullinural yc-user@158.160.7.223
umataullin.hopto.org
umataullin.dynnamn.ru
login: yc-user passphrase: NRjeSf
