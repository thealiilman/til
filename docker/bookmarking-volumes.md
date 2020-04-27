# Bookmarking Volumes
We can bookmark a volume within our docker container without mapping it to a file/folder within our local directory.  

This can be useful. For an example, our local directory may not have `node_modules`, but our working directory in our docker container, `/app` does have `node_modules` folder.  

To bookmark a volume within our docker container, run the following command with this argument.

```zsh
docker run -v /app/node_modules image-id
```
