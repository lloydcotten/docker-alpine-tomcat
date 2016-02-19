# Alpine-based Tomcat images
In this repo you will find minimal Tomcat images.

## Docker Hub
The public docker hub repository is here: https://hub.docker.com/r/lloydcotten/alpine-tomcat/

Images are built with the latest official Alpine linux base image, and include the following
additional packages by default

- curl (latest Alpine package available)
- tar (latest Alpine package available)

## Usage
```
CID=$(docker run -it lloydcotten/alpine-tomcat:tomcat8-jre8)
docker inspect --format '{{ .NetworkSettings.IPAddress }}' "${CID}"
```
Visit http://*<IPAddress>*:8080/ in a web browser on your host machine.


## Images

* Tomcat v8 / openjdk-jre8: `docker pull lloydcotten/alpine-tomcat:tomcat8-jre8`