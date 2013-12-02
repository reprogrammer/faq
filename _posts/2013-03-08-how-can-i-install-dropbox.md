---
layout: post-layout
title: How can I install Dropbox?
tags:
- linux
---

First, run the following command to add the Dropbox repository.

    sudo add-apt-repository "deb http://linux.dropbox.com/ubuntu $(lsb_release -sc) main"

Next, run the command `sudo apt-get update`. You should get an error message
similar to the following:

> W: GPG error: http://linux.dropbox.com precise Release: The following
> signatures couldn't be verified because the public key is not available:
> NO_PUBKEY FC918B335044912E

Follow the instructions at
[{{site.url}}/2013/02/24/how-can-i-install-ubuntu-repository-public-keys/]({{site.url}}/2013/02/24/how-can-i-install-ubuntu-repository-public-keys/)
to add the necessary keys. While following the instruction, note that the
Dropbox's key server is `pgp.mit.edu`.

Finally, run the following commands to install Dropbox.

    sudo apt-get update
    sudo apt-get install dropbox python-gpgme

**References**

- [http://askubuntu.com/a/127187](http://askubuntu.com/a/127187)

