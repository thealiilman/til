# Stopping a Container
There are two commands.
```
docker stop container-id
docker kill container-id
```

`docker stop` sends **_SIGTERM_** to the main process running in the container, telling the process to stop.
But if the process doesn't stop **within 10 seconds**, `docker stop` will fallback to `docker kill`.  
`docker kill` sends **_SIGKILL_** to the process, forcefully stopping the container.
