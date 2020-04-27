# Adding a Volume for a Container In Docker Compose
To add a volume for a container in `docker-compose.yml`, it's simple!

We just need to add a `volumes` key with an array of values.

```zsh
version: '3'
services:
  react-app:
    build: ./
    ports:
      - 3000:3000
    volumes:
      - /app/node_modules
      - ./:/app
```
