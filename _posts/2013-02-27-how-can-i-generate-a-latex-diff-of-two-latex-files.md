---
layout: post-layout
title: How can I generate a LaTeX diff of two LaTeX files?
tags:
- linux
- tex
---

Make sure `old.tex` and `new.tex` have a place to insert the preamble.

    latexdiff --type=UNDERLINE --subtype=SAFE --floattype=FLOATSAFE old.tex new.tex > difference.tex
