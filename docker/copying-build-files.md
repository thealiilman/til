# Copying Build Files
When we run our Docker image, there will always be commands that require files / folders in the current directory on our machine.  

To copy the content of our current directory to the container, we can use the `COPY` command.
```dockerfile
COPY ./ ./
```

The first `./` refers to the current directory **on our machine**.  
The second `./` refers to the current directory **on the container**.
