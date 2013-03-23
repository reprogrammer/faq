---
layout: post-layout
title: How can I install TeXLive in Ubuntu?
tags:
- linux
---

    sudo apt-get install perl-tk
    wget http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz
    tar xvfz install-tl-unx.tar.gz
    sudo ./install-tl<tab>/install-tl -gui

Select the following two options:

- Use the _letter_ size instead of the default _A4_ size.
- Create symlinks in system directories.

The installer asks about the following directories. Leave the default settings.

    TEXDIR=/usr/local/texlive/<year>
    TEXMFLOCAL=/usr/local/texlive/texmf-local
    TEXMFSYSVAR=/usr/local/texlive/<year>/texmf-var
    TEXMFSYSCONFIG=/usr/local/texlive/<year>/texmf-config
    TEXMFHOME=~/texmf

The installer says the following, but the symlinks are enough.

> Add `/usr/local/texlive/2011/texmf/doc/man` to `MANPATH`.
>
> Add `/usr/local/texlive/2011/texmf/doc/info` to `INFOPATH`.
>
> Most importantly, add `/usr/local/texlive/2011/bin/x86_64-linux`.

**References**

- [http://www.tug.org/texlive/debian.html](http://www.tug.org/texlive/debian.html)
