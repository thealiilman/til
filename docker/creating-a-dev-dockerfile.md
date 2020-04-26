# Creating the Dev Dockerfile
If we were to have a Dockerfile that has a different name such as `Dockerfile.dev`, we need to tell `docker build` which Dockerfile to use for building an image.

To do this, we simply pass a `-f` argument to the command. This argument is for specifying the Dockerfile we want to use.
```zsh
docker build -f Dockerfile.dev .
```
