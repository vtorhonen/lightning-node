# lightningd for lightning-node

Modified version of `cdecker/lightningd` (see [Dockerfile](https://github.com/cdecker/dockerfiles/blob/master/lightning/node/Dockerfile) and [Dockerhub](https://hub.docker.com/r/cdecker/lightningd/)).

Uses multi-stage builds on Debian Strech slim images. Results for image size:

- Modified: 34 MB (compressed), 93 MB (uncompressed)
- Original: 215 MB (compressed), 544 MB (uncompressed)

[Final images from this repository can be found from Dockerhub](https://hub.docker.com/r/vtorhonen/lightningd). Dockerhub automated builds are active.
