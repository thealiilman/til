# Setting up Docker Compose
From what we know at the moment, the Docker Compose file consist of two root keys.

1. version
2. services

`version` is for us to specify the Docker Compose version.
`services` is for us to specify services we want to run **in the form of Docker containers**.

Example. (from [this app](https://github.com/thealiilman/i-learn-docker-and-k8s/tree/master/visits)).
```yml
version: '3'
services:
  redis-server:
    image: redis
  node-app:
    # build will look for
    # the Dockerfile within
    # the current directory
    build: ./
    ports:
      - 4001:8081
```
