
Run your django web before hit your browser with http or https


docker pull uzzal2k5/nginx-ssl-python3.5

or
Follow the git to build your image from git project


Above command download docker container successfully .
Run your container



docker run -it -p 80:80 -p 443:443 --name nginx_web  \
-v ./docker-web/var/www/html:/var/www/html:ro  \
-v  ./docker-web/var/log/nginx:/var/log/nginx  \
uzzal2k5/nginx-ssl-python3.5

 After successfully run container enter into the container yousing exec command and run you django app using folloing command

 python /var/www/html/nginx_web/manage.py runserver

 Now you can hit your browser to  browse your web.

