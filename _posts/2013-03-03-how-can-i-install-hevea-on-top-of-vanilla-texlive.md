---
layout: post-layout
title: How can I install hevea on top of vanilla TeXLive?
tags:
- linux
- tex
---

I installed texlive-vanilla (2010-1~1). And, tried to install hevea with the
following command.

    sudo apt-get --no-install-recommends install hevea

But, I got the following message.

    The following NEW packages will be installed:
    
      hevea ocaml-base-nox tex-common

So, I checked the dependencies of the hevea in Ubuntu. The hevea package
requires "tex-common (>=2.00)". The "provides" section of the control file of
vanilla-texlive doesn't specify the versions of the virtual packages. So, I
thought all of the virtual packages get the version number 2010-1~1
automatically. Then, I used the following command to verify that "2010-1~1" is
indeed greater than "2.00" according to Ubuntu package formate rules.

    dpkg --compare-versions 2010-1~1 gt 2.00 ; echo $?

And, I got the value "0" on the console, which confirms that 2010-1~1 is greater
than 2.00. At this point, I concluded that the version number of the virtual
packages is unspecified. So, I decided to create my own version of tex-common. I
created a control file for my tex-common package called tex-common.ctl and
executed the following commands.

    equivs-build tex-common.ctl sudo dpkg -i tex-common_2010-1~1_all.deb

Having installed my own tex-common package, I was able to successfully install
hevea using the following command.

    sudo apt-get --no-install-recommends install hevea

