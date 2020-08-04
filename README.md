# devops
## Docker [![Docker version](https://img.shields.io/badge/Docker-v19.03.8-blue.svg)](https://www.docker.com/)
To achieve modularity means based on need add lib, apps, etc.
### Terms which is used in docker
  - **Containers**<br />
    Image run on containers and containers are isolated from outside world.
  - **Images**<br />
    Applications run on image
### Commands
  - Docker file for build image<br />
    Ex: Run spring boot app on container<br />
    ```
    FROM openjdk:11
    VOLUME /tmp
    COPY build/libs/helloworld*.jar /tmp/hellowworld.jar
    CMD [ "java", "-jar", "tmp/hellowworld.jar"]
    ```
    Where as,<br />
    **FROM** - for download libs<br />
    **VOLUME** - to create a folder and store our data into that<br />
    **COPY** - Copy the file from source to destination<br />
    **CMD** - Execute commands inside of docker image<br />
  - Docker build<br />
    When trigger build that time it will build image based on docker file configuration.<br />
    ```
    docker build -t helloworld .
    ```
  - Check whether docker image is getting created or not
    ```
    docker images
    ```
  - Run docker image on contaier
    ```
    docker run --rm -d -p 8989:3434 image_id
    ```
    Where as,<br />
    **-p** - 3434 port is nothing but spring boot runing port and expose port is 8989<br />
    **-d** - Detach mode(While run image, exit from container)<br />
    **image_id** - Either can give image id or image name with flag<br />
  - Check wheter the container is running or not
    ```
    docker ps
    ```
  - Test application using exposed port
    ```
    192.168.99.100/docker/
    ```
  - Stop docker container
    ```
    docker container stop container_id
    ```
