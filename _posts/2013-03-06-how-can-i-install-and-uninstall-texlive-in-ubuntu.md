---
layout: post-layout
title: How can I install and uninstall TeXLive in Ubuntu?
tags:
- linux
- tex
---

### Installation

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

> Add `/usr/local/texlive/20xy/texmf/doc/man` to `MANPATH`.
>
> Add `/usr/local/texlive/20xy/texmf/doc/info` to `INFOPATH`.
>
> Most importantly, add `/usr/local/texlive/20xy/bin/x86_64-linux`.

### Uninstallation

    sudo tlmgr uninstall
    rm -rf /usr/local/texlive

**References**

- [http://www.tug.org/texlive/acquire-netinstall.html](http://www.tug.org/texlive/acquire-netinstall.html)
- [http://www.tug.org/texlive/debian.html](http://www.tug.org/texlive/debian.html)
