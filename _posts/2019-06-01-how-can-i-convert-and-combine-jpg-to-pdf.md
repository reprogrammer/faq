---
layout: post-layout
title: How can I convert and combine JPG to PDF?
tags:
- linux
---

    convert *.jpg output.pdf

If `convert` returns a `not authorized` error, edit
`/etc/ImageMagick-6/policy.xml` and change the PDF rights from `none` to
`read|write`.

**References**  

- [https://askubuntu.com/a/1081724](https://askubuntu.com/a/1081724)

