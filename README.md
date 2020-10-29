# Laboratorio EFK

## 1 Microservicio Java

````shell
docker-compose -f docker-compose-java.yml up --build
````

## 2 Java + Fluentd stdout

1. Descomentar docker-compose-java.yml
2. Iniciar Microservicio Java
    ````shell
    $ docker-compose -f docker-compose-java.yml up --build -d
    ````
3. Iniciar fluentd

    ````shell
    $ docker-compose -f docker-compose-fluentd.yml up --build
    ````
4. Llamar healthcheck microservicio http://localhost:8081/actuator/health

5. Revisar log fluentd

## 3 Java + Fluentd + Elastic & Kibana

1. Detener ejecucion de fluentd
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml stop
    $ docker-compose -f docker-compose-fluentd.yml rm -f
    ````
2. Modificar archivo Dockerfile del directorio fluentd

    Antes:
    > COPY conf/fluent.conf /fluentd/etc/fluent.conf

    Después:
    > COPY **conf/fluent.conf.1** /fluentd/etc/fluent.conf

    ````shell
    $ vi/nano fluentd/Dockerfile
    ````
3. Iniciar elastic
    
    ````shell
    $ docker-compose -f docker-compose-elastic.yml up --build -d
    ````

4. Iniciar fluentd con nueva configuracion
    
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml up --build -d
    ````
5. Llamar healthcheck microservicio http://localhost:8081/actuator/health

6. Acceder al puerto 5601 de la instancia
    
    * Crear indice
    * Revisar datos

## 4 Java + Fluentd pattern + Elastic & Kibana 

1. Detener ejecucion de fluentd
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml stop
    $ docker-compose -f docker-compose-fluentd.yml rm -f
    ````
2. Modificar archivo Dockerfile del directorio fluentd

    Antes:
    > COPY conf/fluent.conf /fluentd/etc/fluent.conf

    Después:
    > COPY **conf/fluent.conf.3** /fluentd/etc/fluent.conf

    ````shell
    $ vi/nano fluentd/Dockerfile
    ````
3. Iniciar fluentd con nueva configuracion
    
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml up --build -d
    ````
4. Llamar healthcheck microservicio http://localhost:8081/actuator/health

5. Acceder al puerto 5601 y revisar datos

## 5 Java + Fluentd specific pattern + Elastic & Kibana 

1. Detener ejecucion de fluentd
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml stop
    $ docker-compose -f docker-compose-fluentd.yml rm -f
    ````
2. Modificar archivo Dockerfile del directorio fluentd

    Antes:
    > COPY conf/fluent.conf /fluentd/etc/fluent.conf

    Después:
    > COPY **conf/fluent.conf.4** /fluentd/etc/fluent.conf

    ````shell
    $ vi/nano fluentd/Dockerfile
    ````
3. Iniciar fluentd con nueva configuracion
    
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml up --build -d
    ````
4. Llamar healthcheck microservicio http://localhost:8081/actuator/health

5. Acceder al puerto 5601 y revisar datos

## 6 Java + Fluentd remove fields + Elastic & Kibana 

1. Detener ejecucion de fluentd
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml stop
    $ docker-compose -f docker-compose-fluentd.yml rm -f
    ````
2. Modificar archivo Dockerfile del directorio fluentd

    Antes:
    > COPY conf/fluent.conf /fluentd/etc/fluent.conf

    Después:
    > COPY **conf/fluent.conf.5** /fluentd/etc/fluent.conf

    ````shell
    $ vi/nano fluentd/Dockerfile
    ````
3. Iniciar fluentd con nueva configuracion
    
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml up --build -d
    ````
4. Llamar healthcheck microservicio http://localhost:8081/actuator/health

5. Acceder al puerto 5601 y revisar datos

## 7 Java + Fluentd (parse Log4j + Json log) + Elastic & Kibana 

1. Detener ejecucion de fluentd
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml stop
    $ docker-compose -f docker-compose-fluentd.yml rm -f
    ````
2. Modificar archivo Dockerfile del directorio fluentd

    Antes:
    > COPY conf/fluent.conf /fluentd/etc/fluent.conf

    Después:
    > COPY **conf/fluent.conf.6** /fluentd/etc/fluent.conf

    ````shell
    $ vi/nano fluentd/Dockerfile
    ````
3. Iniciar fluentd con nueva configuracion
    
    ````shell
    $ docker-compose -f docker-compose-fluentd.yml up --build -d
    ````
4. Llamar healthcheck microservicio http://localhost:8081/actuator/health

5. Acceder al puerto 5601 y revisar datos

