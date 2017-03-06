FROM nginx:latest
COPY www /usr/share/nginx/html

# статический запуск
#  docker build -t mynginx .
#  docker run --name some-nginx -p 8080:80 -d -v ~/Desktop/servers/docker/nginx/www:/usr/share/nginx/html mynginx
#  docker run --name some-nginx -p 8080:80 -d -v ~/Desktop/servers/docker/nginx/www:/usr/share/nginx/html nginx:latest запуск без билда статический html
#  docker exec -it some-nginx /bin/bash


# запуск с php http://172.17.0.2/
# docker run --name some-nginx -v ~/Desktop/servers/docker/nginx/www:/var/www/html -d richarvey/nginx-php-fpm
