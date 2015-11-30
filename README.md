## Digitalocean + grsecurity

This repo aims to document a well-working minimal Linux kernel + grsecurity
config that works on Digitalocean VMs. Digitalocean allows you to deploy your
own kernel using grub for certain newer VM types (Ubuntu 15.04 Vivid, Debian
8). You can use this kernel config to get started compiling your own kernel
from scratch, without a lot of unwanted modules that take a lot of time to
compile. This config works with a vanilla Linux 4.2.6 kernel and the grsecurity
patches.

**This is work in progress!**

## Current features

- Works fine on Digitalocean with Ubuntu 15.04
- Works with Docker (storage backend: Overlay FS)
- No modules
- Small kernel config (fast recompile + deploy)

## TODO

- The "general" section could use some manual review.
- I haven't tested this extensively, there could be vital options missing.

## RFC

If you run this kernel and notice that something is missing please file an
issue or create a pull-request. This is not a promise that I'll blindly accept
those pull-request if they don't cater to (what I believe to be) a common
application.
