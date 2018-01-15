
Run your django web before hit your browser with http or https


This is my first test based docker image, where httpd server installed into centos 7. As Dockerfile written like bellow,


docker run -dit -p 80:80 --name webserver uzzal2k5/httpd:latest /bin/bash


Above command run docker container successfully .
Dockerfile:

FROM centos
MAINTAINER uzzaluzzal2k5@gmail.com , Mobile: +8801715519132
RUN yum -y install httpd
RUN echo "Follow me on LinkedIn ( https://www.linkedin.com/in/uzzal2k5 )" > /var/www/html/index.html
EXPOSE 80
CMD ["-D","FOREGROUND"]
ENTRYPOINT ["/usr/sbin/httpd"]

