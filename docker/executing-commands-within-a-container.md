# Executing Commands in Running Containers

Say, we have a container running Redis.
```
docker run redis
```
To execute the Redis CLI and access the Redis server within the container, we can execute a command that relays our given command to the container.

`docker exec -it container-id redis-cli`

What is happening here?
1. `exec` is the command for running a command within a container.
2. We're telling Docker to tell the container that we want to provide input to the container by passing the `-it` flag.
3. We're telling Docker to tell the container that we want to execute `redis-cli`.
