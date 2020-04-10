# Specifying a Working Directory

It's not a good practice to copy the files on our machine to the root directory of our container. We can specify a **working directory** to place the files instead.  

To specify a working directory, it's as simple as running the following command.
```dockerfile
WORKDIR /working/directory
```

One of the practices is to place your files inside of `/usr/app`.
```dockerfile
WORKDIR /usr/app
```
