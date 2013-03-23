---
layout: post-layout
title: How can I recover Grub after installing Windows?
tags:
- linux
---

### grub

`sudo grub`

Tell Grub which partition to tell the MBR your Grub is on by entering:

`root (hd0,3)`

If Ubuntu was installed on the second partition of the first hard-drive.  Tell
GRUB which drive's MBR to fix:

    setup (hd0)
    quit

### grub2

**References**

[https://wiki.ubuntu.com/Grub2#Recover%20Grub%202%20via%20LiveCD](https://wiki.ubuntu.com/Grub2#Recover%20Grub%202%20via%20LiveCD)

