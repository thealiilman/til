# Commands To Run a Container
`docker run image-name` actually executes these two behind-the-scenes.

```
docker create image-name
=> container-id

docker start -a container-id
=> output
```

`docker create` takes an image and creates a container from it. Running this command will return the id of the container.  

`docker start -a` takes the id of a container and starts the container. `-a` tells Docker to watch for output from the container to print the output to our terminal. If we exclude `-a`, the only output we will see is the id of the container.
