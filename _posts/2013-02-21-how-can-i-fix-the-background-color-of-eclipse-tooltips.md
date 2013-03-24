---
layout: post-layout
title: How can I fix the background color of Eclipse tooltips?
tags:
- linux
- eclipse
---

Open the file at `/usr/share/themes/Ambiance/gtk-2.0/gtkrc`. Locate
`tooltip_fg_color` and `tooltip_bg_color` in the file and change their values as
follows:

    tooltip_fg_color:#000000
    tooltip_bg_color:#f5f5c5

**References**

- [http://www.vogella.com/blog/2012/12/04/eclipse-papercut-10-eclipse-on-ubuntu-fixing-the-black-background-color-in-hover/](http://www.vogella.com/blog/2012/12/04/eclipse-papercut-10-eclipse-on-ubuntu-fixing-the-black-background-color-in-hover/)
- [http://wiki.eclipse.org/IRC_FAQ#Black_background_color_for_tooltips_on_Linux.2FUbuntu.2FGTK](http://wiki.eclipse.org/IRC_FAQ#Black_background_color_for_tooltips_on_Linux.2FUbuntu.2FGTK)

