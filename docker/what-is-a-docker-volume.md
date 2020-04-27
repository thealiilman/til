# What is a Docker Volume
When we have a running container, any changes we made to the codebase won't be reflected automatically. We'd have to rebuild the image.

So how do we ensure that our container is running latest changes without rebuilding an image? This is where **Docker Volumes** come into play.

When we build a docker image, we take a **filesystem snapshot** of the directory we specified to be included in the image.

Instead of the usual `docker run xxx` command, we can add certain arguments to utilise Docker Volumes. Docker Volumes can be thought of as mapping our local directory to the working directory within our container.

Here's the command.
```zsh
docker run -v $(pwd):/path-to-working-directory-in-container image-id
```
