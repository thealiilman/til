# What is a Container?
A container is a section in your hard-drive that _contains specific processes and resources within the section itself_.

## How does an image relates to a container?
An image is basically a **file-system snapshot** and a **startup command**. It consists of one-or-more files within itself.

When we create a container from the image, the Kernel will _isolate certain resources just for the container_.

When we tell the container to run a startup command, the file being executed in the command will be put as _one of the running processes in the container_, allowing it to _utilise resources within the container_ through the Kernel.
