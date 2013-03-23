---
layout: post-layout
title: How can I configure my SSH client to connect to a server?
tags:
- linux
---

    ssh-keygen -C "key-identifier" (without quotes)  
    scp ~/.ssh/id_rsa.pub server.example.org
    cat ~/id_rsa.pub >> ~/.ssh/authorized_keys

Create or open the file at `~/.ssh/config` Add the following lines:

    Host server.example.org
    User git
    Hostname server.example.org
    PreferredAuthentications publickey
    IdentityFile [local path to private key half of the public key you provided]

The main ssh config file is at `/etc/ssh/ssh_config`.
