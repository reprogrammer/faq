---
layout: post-layout
title: How can I install a recent version of gcc?
tags:
- linux
---

    sudo add-apt-repository ppa:ubuntu-toolchain-r/test
    sudo apt-get update
    sudo apt-get install gcc-4.8
    sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 50

**References**  

- [http://askubuntu.com/a/271561](http://askubuntu.com/a/271561)

