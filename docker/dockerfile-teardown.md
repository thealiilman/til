# Dockerfile Teardown
Dockerfile Teardown
```dockerfile
FROM alpine

RUN apk add --update redis

CMD ["redis-server"]
```

`FROM` is the command to specify the base image.  

`RUN` is the command to download and install programs.  

`CMD` is the command to specify the command to execute when a container has started.
