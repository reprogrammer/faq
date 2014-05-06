---
layout: post-layout
title: How can I install the Opera browser on Ubuntu?
tags:
- linux
---

    sudo bash -c 'echo "deb http://deb.opera.com/opera/ stable non-free" > /etc/apt/sources.list.d/opera.list'
    sudo apt-get install debian-archive-keyring
    wget -O - http://deb.opera.com/archive.key | sudo apt-key add -
    sudo apt-get update
    sudo apt-get install opera

**References**  

- [http://deb.opera.com/](http://deb.opera.com/)
- [https://help.ubuntu.com/community/OperaBrowser](https://help.ubuntu.com/community/OperaBrowser)

