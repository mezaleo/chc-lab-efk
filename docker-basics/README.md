# Docker

## Listar contenedores

docker container ls

## Detener contenedores

docker stop <container id>

## Eliminar contenedor

docker rm <container id>

## Start nginx básico

docker run -it --rm -d -p 8080:80 --name minombre mitag:1

## Start nginx customizado

docker build -t mitag:1 .

# docker-compose

## Iniciar docker-compose.yml

docker-compose up

## Iniciar en background

docker-compose up -d

## Re construir

docker-compose up --build

## Re construir en background

docker-compose up --build -d