# Docker-Snippets

## Docker Run Image

`docker container run <CONTAINER NAME>`

## List Containers

`docker container ls -a`

## List Images 

`docker image ls`

## Start Container

`docker start <CONTAINER NAME>`

## Kill Container

`docker kill <CONTAINER NAME>`

## Start Container in Interactive Mode

`docker start -i <CONTAINER NAME>`

## DockerFile Example

```
FROM node:16

WORKDIR /usr/src/app

COPY ./index.js ./index.js

CMD node index.js
```

