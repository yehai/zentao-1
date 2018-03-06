# Docker Image for Zentao
[![Docker Build Status](https://img.shields.io/docker/build/yehai/zentao.svg)](https://hub.docker.com/r/idoop/zentao/)
[![Docker Pulls](https://img.shields.io/docker/pulls/yehai/zentao.svg)](https://hub.docker.com/r/yehai/zentao-pro/)
[![Docker Automated build](https://img.shields.io/docker/automated/yehai/zentao.svg)](https://hub.docker.com/r/yehai/zentao/)
[![ImageLayers Size](https://img.shields.io/imagelayers/image-size/yehai/zentao/latest.svg)](https://hub.docker.com/r/yehai/zentao/)
[![ImageLayers Layers](https://img.shields.io/imagelayers/layers/yehai/zentao/latest.svg)](https://hub.docker.com/r/yehai/zentao/)

Auto build docker image for zentao(禅道).

DockerHub:[https://hub.docker.com/r/idoop/zentao/](https://hub.docker.com/r/idoop/zentao/)

Zentao
- Version: `9.8.1` *Linux_X64*


### QuickStart

```bash
docker run -d -p 80:80 -p 3306:3306 \
        -e USER="root" -e PASSWD="password" \
        -e BIND_ADDRESS="false" \
        -v /opt/zbox/:/opt/zbox/ \
        --name zentao-server \
        idoop/zentao
```

Note: Make sure your Host feed available on either port `80` or `3306`.

### Environment configuration

* `USER` : sets the web login database Adminer account.
* `PASSWD` : sets the web login database Adminer password. 
* `BIND_ADDRESS` : if set value with false,the Mysql server will not bind-address.

Note: The zentao administartor account is **admin**,and init password is **123456**.
      And MySQL root account password is **123456**,please change password when you first login.


### Building the image

Clone this git,modify `Dockerfile` or `docker-entrypoint` if you want.
Then execute the following command:

```bash
docker build -t zentao .
```
        
        
