---
layout: post-layout
title: How can I install an SSH server?
tags:
- linux
---

```
sudo apt-get install openssh-server
```

When an old client tries to connect to the server, it complains that the server
has changed its identity. Remove the `~/.ssh/known_hosts` to have the client
receive the new identity of the server.

**References**

[https://help.ubuntu.com/6.06/ubuntu/serverguide/C/openssh-server.html](https://help.ubuntu.com/6.06/ubuntu/serverguide/C/openssh-server.html)
