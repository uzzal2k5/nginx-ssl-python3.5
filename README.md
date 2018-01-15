
Run your django web before hit your browser with http or https


docker exec -it nginx_web bash
cd /var/www/html/ngin_web
python manage.py runserver
