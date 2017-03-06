FROM ubuntu:latest
RUN apt-get update \
    && DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server

EXPOSE 3306
CMD ["mysqld"]
# docker build .
# docker build --tag=private/mysql . присвоить имя
# docker run -i -t --rm private/mysql bash внутри контейнера и попасть в консоль /usr/sbin/mysqld
# docker volume create --name=mysql5-7-data сделать том /var/lib/docker/volumes/mysql5-7-data
# docker run -v mysql5-7-data:/var/lib/mysql private/mysql true - запуск контейнера с монтрованием томов
# sudo ls /var/lib/docker/volumes/mysql-data/_data данные из контейнера в томах
# docker volume ls | rm инфо или удалить том
# docker volume inspect mysql-data подробнее о томе
# docker exec -it  /bin/bash