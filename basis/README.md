# MySQL with No Volumes

This is a hack of the [official `mysql:5` image from Docker][1].
Docker currently does not provide a means to _undo_ a `VOLUME` directive
once set in an image. But we want to be able to snapshot the database.

## How does this work?

Four steps:

1. Create a container from `mysql:5`.
2. Export it to a tarball.
3. Import it to a new, flat image.
3. Re-apply all the environmental and configuration effects.

[1]: https://registry.hub.docker.com/_/mysql/ 
