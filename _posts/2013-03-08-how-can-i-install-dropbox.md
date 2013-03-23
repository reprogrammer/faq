---
layout: post-layout
title: How can I install Dropbox?
tags:
- linux
---

Add the following repository:

`deb http://linux.dropbox.com/ubuntu lucid main`

Then, refer to
[https://www.dropbox.com/downloading?os=lnx](https://www.dropbox.com/downloading?os=lnx)
for updated installation instructions.

    gpg --keyserver pgp.mit.edu --recv-keys 3565780E
    sudo apt-get update

    W: GPG error: http://linux.dropbox.com karmic Release: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY FC918B335044912E

    gpg --keyserver pgp.mit.edu --recv-keys FC918B335044912E
    sudo apt-key list

At this point, the keys are not added to apt.

`sudo gpg --armor --export 3565780E | sudo apt-key add -`
or
`gpg -a --export 3565780E | sudo apt-key add -`

    sudo gpg --armor --export FC918B335044912E | sudo apt-key add -
    sudo apt-key list

At this point, the keys are added to apt.

    sudo apt-get update
    sudo apt-get install nautilus-dropbox
