---

date: 2006-10-06 15:38:44+00:00
layout: post
title: Bibtex tip
---

This problem crops up every so often with my Bibtex files:

`This is BibTeX, Version 0.99c (Web2C 7.5.4)
The top-level auxiliary file: oss07.aux
The style file: plainnat.bst
Database file #1: neilernst.bib
Sorry---you've exceeded BibTeX's buffer size 5000
Aborted at line 14636 of file neilernst.bib
(That was a fatal error)
`
Now, I initially thought this meant my bibtex file was too long (15k lines). But really, [the issue](http://www.tug.org/pipermail/macostex-archives/2005-February/013286.html) is that one line of the file -- identified by the parser above as line 14636 -- is over 500 characters. Once I'd trimmed this (an abstract from Amazon) everything worked as it should.
``
