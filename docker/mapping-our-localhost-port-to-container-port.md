# Mapping Our Localhost Port to Container Port
By default, a request to a localhost port isn't mapped to the port within the container. To do this, it's as simple as using the `-p` flag when executing `docker run`.
```
docker run -p port-on-our-localhost:port-in-the-container image-name

docker run -p 8080:8080 aliilman/nodeapp
```
