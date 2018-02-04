# bitcoind for lightning-node

This container is modified to use multi-stage builds. See [original Dockerfile](https://github.com/dougvk/lightning-node).

With this approach the image size is reduced to 34 MB (compressed) and 86 MB (uncompressed).

[Final images from this repository can be found from Dockerhub](https://hub.docker.com/r/vtorhonen/bitcoind). Dockerhub automated builds are active.
