## DigitalOcean + grsecurity

This repo aims to document a well-working minimal Linux kernel + grsecurity
config that works on DigitalOcean VMs. DigitalOcean allows you to deploy your
own kernel using grub for certain newer VM types (Ubuntu 15.04 Vivid, Debian
8). You can use this kernel config to get started compiling your own kernel
from scratch, without a lot of unwanted modules that take a lot of time to
compile. This config works with a vanilla Linux 4.2.6 kernel and the grsecurity
patches.

**This is work in progress!**

## Current features

- Works fine on DigitalOcean with Ubuntu 15.04
- Works with Docker (storage backend: Overlay FS)
- No modules
- Small kernel config (fast recompile + deploy)

## Docker instructions
When building a kernel, you can use this script to make sure you have the
necessary options enabled in your kernel config:
[check-config.sh](https://github.com/docker/docker/blob/master/contrib/check-config.sh)

You also have to change the storage driver in `/etc/default/docker` like this:
```
DOCKER_OPTS="--storage-driver=overlay"
```

## TODO

- The "general" section could use some manual review.
- I haven't tested this extensively, there could be vital options missing.

## RFC

If you run this kernel and notice that something is missing please file an
issue or create a pull-request. This is not a promise that I'll blindly accept
those pull-request if they don't cater to (what I believe to be) a common
application.
