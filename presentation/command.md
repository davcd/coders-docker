[Introducción]

docker info
docker version
docker --help

docker container run --help
docker container run -d --name test -p 80:80 nginx
docker container run -d mysql
docker container list
docker container rm (docker container list -q)
docker image rm (docker image list -q)
docker container inspect test
docker container inspect -f '{{.NetworkSettings.IPAddress}}' test
docker container stop test
docker container list
docker container list -a
docker container start test
docker container exec test ls
docker container cp test:/.dockerenv .
docker container logs test
docker container stats test
docker system prune

docker run --help
docker run -d --name test -p 80:80 nginx
docker run -d mysql
docker ps
docker rm (docker ps -q)
docker rmi (docker images -q)
docker inspect test
docker inspect -f '{{.NetworkSettings.IPAddress}}' test
docker stop test
docker ps
docker ps -a
docker start test
docker exec test ls
docker cp test:/.dockerenv .
docker logs test
docker stats test
docker system prune



[Imagenes]
cd /imagenes/flask-ubuntu
docker build -t davcd/coders:ubuntu .
docker push davcd/coders:ubuntu
docker run -d -p 5000:5000 davcd/coders:ubuntu
docker stop  davcd/coders:ubuntu

cd ../flask-alpine
docker build -t davcd/coders:alpine .
docker push davcd/coders:alpine
docker run -d -p 5000:5000 davcd/coders:alpine

cd ../go-worker
docker build -t go-worker:latest .
docker run go-worker:latest



[Contenedores]

cd ../../contenedores/flask-redis
docker-compose up -d

cd ../go-tests
docker-compose build
docker-compose run --rm test

cd ../mysql-wordpress