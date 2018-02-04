# lightning-node

Run your own Lightning Network (LN) node with two slim-sized containers. Based on work by @dougvk, but modified to use:

- Slim-sized containers (Debian Stretch slim) with least amount of layers
- Custom Dockerfile for lightningd to separate build and runtime requirements

With these you can either:

1) Follow [@dougvk's blog post](https://medium.com/@dougvk/run-your-own-mainnet-lightning-node-2d2eab628a8b) and setup your LN node manually
2) Use [my Ansible configuration](https://github.com/vtorhonen/lightning-node-ansible) to setup your Lightning Network node(s) by using automation

If you don't know what the Lightning Network is I suggest you read [this FAQ](https://medium.com/@AudunGulbrands1/lightning-faq-67bd2b957d70).
