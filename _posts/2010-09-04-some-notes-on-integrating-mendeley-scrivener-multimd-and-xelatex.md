---

date: 2010-09-04 20:01:33+00:00
layout: post
title: Some notes on integrating Mendeley, Scrivener, MultiMarkdown and (Xe)Latex
tags:
- mendeley
- multimarkdown
- scrivener
- xslt
---

I'm using [Scrivener](http://www.literatureandlatte.com/scrivener.html) for my thesis. It has good outlining options, full-screen mode, rich text, and this neat feature that lets you mark things as comments (annotations). I can use [Multimarkdown](http://fletcherpenney.net/multimarkdown/using_multimarkdown_with_scriv/) to mark up the text (commonly ** to do italics) and lists are much simpler than \begin{itemize}\end{} format of Latex.

To manage my references I have been using [Mendeley](http://www.mendeley.com/). It's a little alpha still. <del>There's no way to search for specific fields, for example</del> Actually, it is possible: either use search fields or click the arrow dropdown menu. Yay! And it doesn't integrate at all with Scrivener, although it will with other editors. There is, however, a web API and it uses a SQLite backend, so hacking is possible.

For example, if there's one thing I hate it is trying to remember the citation key for a reference - it completely kills my flow. So I've hacked up an Apple automator script that will take the highlighted text, search Mendeley's SQLite db for that text, and return a list of possible matches (yes, this is how I procrastinate about actually writing). Then I can stick that in. [Here's the gist (code).](http://gist.github.com/565427)

Generally the Latex export works quite well. You must set an XSLT transform in Scrivener which takes the MultiMarkDown export and converts it to Latex. The [code I have online](http://gist.github.com/565443) shows how to export this to the [UofToronto thesis class](http://www.ctan.org/tex-archive/macros/latex/contrib/ut-thesis/).

A few tips:

-- generally Latex code, e.g. math mode, is passed through with no problems. However, I've found that it is a good idea to surround complex Latex with HTML quotes comments.
-- special characters like % and & get escaped, which is not always what you want, particularly if you have cut and paste.
-- you can't use double-dash inside HTML comments, so switch to using single dash or Mac's en-dash (Opt-dash). If you use XeTex, you can specify a font like Times New Roman which will display this properly.
-- You can't directly show characters like \phi too easily in Latex, yet. You are better off with $\phi$ until math fonts improve.
