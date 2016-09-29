---

date: 2003-10-21 13:20:48+00:00
layout: post
title: Assorted LaTeX tidbits
---

This entry will be updated periodically to reflect my experiences and tips for people using LaTeX.


* * *


I switched to LaTeX recently to format my thesis and large papers.  The chief advantage is that you can do diffs and use CVS with it, which is very handy for backups and collaboration.  The other advantage is that it seems to scale much better than Word.  I've never had a need for mathematical symbols or equations, but I'm told this is another big advantage.  Finally, there are numerous pregenerated styles for bibliographies and papers available, most at [CTAN](http://www.ctan.org), the comprehensive TeX archive.A disadvantage is that it has a not-so-gentle learning curve (but is really just like writing HTML), and it's difficult to coordinate journal writing with non-LaTeX folks.  Also, it can be tricky to do custom formats such as complex tables or figures.  My recommendation is to do these figures and complex graphics in something like Illustrator, and then insert it into the file as a PDF image.


First, I use the [WinEDT](http://www.winedt.com) (pronounced Wine Dit or Win ee-dee-tee or Win Edit) program as a front-end.  It's definitely not at the same level as Word (probably because there's one person working on it, which makes you wonder how many people it takes to make Word), but it can handle simple spellchecking, word counts, syntax highlighting, hotkeys, macros, etc.  I've never found it a hindrance.  It also has a neat table macro which can help you generate tables, which can be tricky.
[MikTex](http://www.miktex.org/) - a LaTeX distribution for windows, comes with a good GUI installer and update program.  Pretty painless really.
Hyperref (included in MikTeX distribution) - this package allows you to start at a specific page when compiling to PDF, which is very handy.  eg package[pdftex, pdftitle=..., pdfstartpage=20]{hyperref}.  You can also use it to add hyperlinks to references in the PDF, which is nice.  Good docs [reside here](http://www.tug.org/applications/hyperref/manual.html#x1-50003.1).
[Listening to:  Suite- Judy Blue Eyes (Radio Paradise - eclectic intelligent rock - music info & listener community at radioparadise.com)  -  Crosby Stills & Nash  -  (0:-1)]
