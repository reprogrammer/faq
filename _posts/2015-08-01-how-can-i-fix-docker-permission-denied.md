---
layout: post-layout
title: How can I fix docker permission denied?
tags:
- linux
---

Docker may give you the `permission deniend` error on Linux:

    $ docker run busybox date
    2015/08/01 15:37:42 Post
    http:///var/run/docker.sock/v1.12/containers/create: dial unix
    /var/run/docker.sock: permission denied

Run the following command and log out to fix the above error.

    sudo usermod -a -G docker ${USER}

**References**  

- [https://cloud.google.com/container-registry/#install_docker](https://cloud.google.com/container-registry/#install_docker)

