# Notes for Docker



### Mongo DB

`$ docker network create net`

`$ docker run --network net -d -p 27017-27019:27017-27019 --name mongodb mongo:4.0.16`

`$ docker exec -it mongodb bash`

`$ docker run --network net  -d -e ME_CONFIG_MONGODB_SERVER=mongodb -p 8081:8081 mongo-express`



### Postgres 

`$ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgre`s



### Jenkins

`$ docker run -p 8080:8080   -v /var/run/docker.sock:/var/run/docker.sock  --name jenkins jenkins/jenkins`:lts



### Nginx

`$ docker run -p 8080:80  -v /home/myself/docker/php/src:/var/www/html nginx:alpine`

`$ docker run -p 8080:80  -v /home/ajcm/git/react-material-ui:/usr/share/nginx/html:ro nginx:alpine`







**eof**