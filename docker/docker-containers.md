## Docker containers



### Alpine
https://hub.docker.com/_/alpine


### Apache
https://hub.docker.com/_/httpd

*versions: httpd:2.4-alpine*

```
docker run -p 8080:80 httpd:2.4-alpine
docker run -p 8080:80 -v "$PWD":/usr/local/apache2/htdocs/ httpd:2.4-alpine
```

### Nginx
https://hub.docker.com/_/nginx

*version: 1.19-alpine, alpine*

```
docker run -p8080:80  -v "$PWD":/usr/share/nginx/html:ro -d nginx:1.19-alpine
```

### PHP/Apache
https://hub.docker.com/_/php

*versions: php:7.4-apache, php:7.2-apache*

```
docker run   -p 8080:80 -v "$PWD":/var/www/html php:7.4-apache
```
notes
https://stackoverflow.com/questions/29905953/how-to-correctly-link-php-fpm-and-nginx-docker-containers

### PHPMyAdmin
https://hub.docker.com/r/phpmyadmin/phpmyadmin/

```
docker run --name myadmin -d -e PMA_HOST=dbhost PMA_PORT=port -p 8080:80 phpmyadmin
```


### Mongo DB
```
$ docker network create net
$ docker run --network net -d -p 27017-27019:27017-27019 --name mongodb mongo:4.0.16
$ docker exec -it mongodb bash
$ docker run --network net  -d -e ME_CONFIG_MONGODB_SERVER=mongodb -p 8081:8081 mongo-express
```


### Postgres 
```
$ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgress
```

### Jenkins
```
$ docker run -p 8080:8080   -v /var/run/docker.sock:/var/run/docker.sock  --name jenkins jenkins/jenkins:lts
```




---