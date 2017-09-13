# spring-boot-docker

Example of using the transmode gradle Docker plugin to run a Spring Boot Applicationin Docker.

## Building

    $ ./gradlew buildDocker

    $ $ docker images
    REPOSITORY                       TAG                 IMAGE ID            CREATED             SIZE
    caseydunham/spring-boot-docker   latest              7c68a25f0dc9        40 seconds ago      132MB
    develar/java                     latest              edc8788ce767        15 months ago       118MB

## Running

    $ docker run -d -p 8080:8080 caseydunham/spring-boot-docker
    feab9f9b39c731082c69ba9300ce834af8a6fff0ec56481e1fb4999baeda5451

    $ docker ps
    CONTAINER ID        IMAGE                            COMMAND                  CREATED             STATUS              PORTS                    NAMES
    d9b49c158857        caseydunham/spring-boot-docker   "sh -c 'java $JAVA..."   2 seconds ago       Up 1 second         0.0.0.0:8080->8080/tcp   admiring_hermann

Now you should be able to connect to `localhost:8080` and see the `Hello World` message.

Built from instructions from the Spring docs here: https://spring.io/guides/gs/spring-boot-docker/
