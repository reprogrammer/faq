---
layout: post-layout
title: How can I update my TeXLive installation?
tags:
- linux
- tex
---

### Updating the updater itself

`sudo tlmgr update --self`

### Updating the updater itself and all the packages

`sudo tlmgr update --self --all`

### Updating the TeXLive distribution

`sudo tlmgr -gui`

You can check if a package is installed by using the `locate` command.
Sometimes, a package is installed but the symlink to it in system directories is
missing. You can update the symlinks through the `tlmgr` program.
