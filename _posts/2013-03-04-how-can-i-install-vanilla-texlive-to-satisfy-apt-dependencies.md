---
layout: post-layout
title: How can I install vanilla TeXLive to satisfy APT dependencies?
tags:
- linux
- tex
---

I used
[texlive.ctl](https://gist.github.com/reprogrammer/5228178#file-texlive-ctl) to
create a vanilla TexLive package. I removed `tex-common` from
[texlive.ctl](https://gist.github.com/reprogrammer/5228178#file-texlive-ctl)
because the original texlive.ctl file didn't have it and I had to remove it to
install hevea. The hevea package is not included in TeXLive.  And, I had to
install `tex-common` in order to install hevea. Also, to let my own installation
of TeXLive locate the style files of the hevea package installed through Ubuntu,
I had to set the following environment variable.

    export TEXMFHOME=/usr/share/texmf/

I used the following command to set the "Standards-Version" field in
`texlive.ctl`.

    apt-cache show debian-policy | grep Version

Then, I executed the following commands to create and install my vanilla
package.

    equivs-build texlive.ctl sudo dpkg -i texlive-vanilla_2010-1~1_all.deb

Finally, I used the following command to install kile.

    sudo apt-get --no-install-recommends install kile

See
[http://manpages.ubuntu.com/manpages/maverick/man5/deb-control.5.html](http://manpages.ubuntu.com/manpages/maverick/man5/deb-control.5.html)
to learn more about the format of Ubuntu package control files. Specifically,
the "Provides" section lists virtual packages that could be provided by the
normal package.

**References**

- [http://www.tug.org/texlive/debian.html](http://www.tug.org/texlive/debian.html)
- [http://superuser.com/questions/134125/vanilla-tex-live-2009-on-ubuntu](http://superuser.com/questions/134125/vanilla-tex-live-2009-on-ubuntu)
- [http://tex.stackexchange.com/questions/1092/how-to-install-vanilla-texlive-on-debian-or-ubuntu/1094#1094](http://tex.stackexchange.com/questions/1092/how-to-install-vanilla-texlive-on-debian-or-ubuntu/1094#1094)
