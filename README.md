# Magento Database Docker Images

Magento MySQL database images, but with no volumes. Swap out the container for
different initial states. Commit and tag to create new initial states for
testing.

## How to build

1. Put a magento tarball into this directory.
2. Run `docker-compose run --rm build`.
3. Commit the resulting `db` container.

## Troubleshooting

- Make sure the db is new and empty.
- The Magento tarball has to be a tar.xz file. Pull requests welcome.
- This Docker Composition does not clean up images or containers after
itself. The point is for you to commit the db container.
