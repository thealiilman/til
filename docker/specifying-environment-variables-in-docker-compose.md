# Specifying Environment Variables in Docker Compose
To specify environment variables in a Docker Compose file, we use a key called `environment` in the relevant service.  
It is an array, and to specify an environment variable, the format is simply `VARIABLE=VALUE`.

E.g.
```yml
version: '3'
services:
  backend:
    environment:
      - CLIENT_HOST=https://example.com
```

We can also specify just `VARIABLE`, which will go through our shell for an environment variable that matches the name specified. It's best to be explicit by going with the first approach as our shell may not have the specified environment variable.
