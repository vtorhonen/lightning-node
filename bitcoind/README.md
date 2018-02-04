# lightning-node

Relates to blog post by @dougvk: https://medium.com/@dougvk/run-your-own-mainnet-lightning-node-2d2eab628a8b

This container is modified to use multi-stage builds. Final image size is about 34 MB (compressed) and 86 MB (uncompressed).

[Final images can be found from Dockerhub](https://hub.docker.com/r/vtorhonen/lightning-node/). Automated builds are active.

I've also created a repository for automated deploying of lightning nodes on [vtorhonen/lightning-node-ansible](https://github.com/vtorhonen/lightning-node-ansible).
