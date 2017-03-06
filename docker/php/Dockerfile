FROM php:7.0-cli

MAINTAINER Ya

RUN apt-get update
RUN apt-get install -y zip unzip curl git
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php --install-dir=/usr/bin --filename=composer
RUN php -r "unlink('composer-setup.php');"

ADD app /home

#CMD cd home/
#CMD ["php", "-a"]
#RUN cd home/
# docker build -t php-7 .
# docker run --name some-php --rm -it php-7 git --version
# docker run -v $(pwd):/app --rm -it php-7 php -S 0.0.0.0:8888 -t /app
# docker run --name some-php --rm -it php-7 bin/bash
# docker run --name some-php -d -it -v ~/Desktop/servers/docker/php/app:/ php-7 bin/bash
