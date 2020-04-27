# Specifying a Dockerfile in Docker Compose
To specify a Dockerfile, we need to utilise two properties of `build`.

They are `context` and `dockerfile`.  
`context` is for letting Docker know where to look for a Dockerfile.  
`dockerfile` is for letting Docker know the name of the Dockerfile.
```yml
version: '3'
services:
  container-name:
    build:
      context: ./
      dockerfile: NameOfDockerFile
```
