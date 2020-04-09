# Building an Image from a Dockerfile
The command we we use to build an image from a Dockerfile is `docker build`.  
Ensure that you're in a directory with a Dockerfile, and then execute the following.
```
docker build .
```

This means, take the Dockerfile that exist within the directory and build an image from it. The last step returns the id to be used to start a container from the image. E.g.
```
aliilman$ docker build .
Sending build context to Docker daemon  2.048kB
Step 1/3 : FROM alpine
latest: Pulling from library/alpine
aad63a933944: Pull complete
Digest: sha256:b276d875eeed9c7d3f1cfa7edb06b22ed22b14219a7d67c52c56612330348239
Status: Downloaded newer image for alpine:latest
 ---> a187dde48cd2
Step 2/3 : RUN apk add --update redis
 ---> Running in 6d80578c72fe
fetch http://dl-cdn.alpinelinux.org/alpine/v3.11/main/x86_64/APKINDEX.tar.gz
fetch http://dl-cdn.alpinelinux.org/alpine/v3.11/community/x86_64/APKINDEX.tar.gz
(1/1) Installing redis (5.0.7-r0)
Executing redis-5.0.7-r0.pre-install
Executing redis-5.0.7-r0.post-install
Executing busybox-1.31.1-r9.trigger
OK: 7 MiB in 15 packages
Removing intermediate container 6d80578c72fe
 ---> ac86e595d162
Step 3/3 : CMD ["redis-server"]
 ---> Running in 3e1ebdb3bdc5
Removing intermediate container 3e1ebdb3bdc5
 ---> 09a042168b2f
Successfully built 09a042168b2f

docker run 09a042168b2f
```

How do we name the image to something more specific?
We can use `docker build -t` to specify the name. The `-t` flag is for tagging.
```
aliilman$ docker build -t aliilman/redis-image:latest .
Sending build context to Docker daemon  2.048kB
Step 1/3 : FROM alpine
 ---> a187dde48cd2
Step 2/3 : RUN apk add --update redis
 ---> Using cache
 ---> ac86e595d162
Step 3/3 : CMD ["redis-server"]
 ---> Using cache
 ---> 09a042168b2f
Successfully built 09a042168b2f
Successfully tagged aliilman/redis-image:latest

docker run aliilman/redis-image:latest
```
