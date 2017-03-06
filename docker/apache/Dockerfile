FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get -y install apache2 php7.0 php7.0-mysql libapache2-mod-php7.0 curl lynx-cur

RUN a2enmod php7.0
RUN a2enmod rewrite

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid

EXPOSE 80

ADD www /var/www/html
CMD /usr/sbin/apache2ctl -D FOREGROUND

# docker build -t mysite .
# docker run -p 8080:80 -d mysite
# docker run -p 8080:80 -d -v ~/Desktop/servers/docker/apache/www:/var/www/html mysite
# docker run --name some-php --rm -it -v ~/Desktop/servers/docker/php/app:/home php-7 bin/bash