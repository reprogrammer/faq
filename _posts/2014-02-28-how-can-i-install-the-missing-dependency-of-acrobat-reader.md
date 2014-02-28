---
layout: post-layout
title: How can I install the missing dependency of Acrobat Reader?
tags:
- linux
---

Install Adobe Reader 9 using [its .deb file](http://get.adobe.com/reader/).

If you run Adobe Reader, you may get the following error message:

    /opt/Adobe/Reader9/Reader/intellinux/bin/acroread: error while loading shared
    libraries: libxml2.so.2: cannot open shared object file: No such file or
    directory

If you get the above error message, run the following command:

    sudo apt-get install libxml2:i386 libstdc++6:i386

**References**  

- [http://askubuntu.com/a/410648](http://askubuntu.com/a/410648)

