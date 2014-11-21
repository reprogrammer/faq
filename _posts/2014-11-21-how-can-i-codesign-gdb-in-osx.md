---
layout: post-layout
title: How can I codesign gdb in OS X?
tags:
- osx
---

- Use the Keychain Access application to create a certificate with the following
  properties: self signed root, code signing, system, and always trust.
- Run the `command codesign -f -s  "gdb-cert" $(which gdb)`.

**References**  

- [https://gcc.gnu.org/onlinedocs/gnat_ugn/Codesigning-the-Debugger.html](https://gcc.gnu.org/onlinedocs/gnat_ugn/Codesigning-the-Debugger.html)

