---

date: 2011-07-27 14:48:11+00:00
title: Writing Complex Latex Documents with Scrivener 2.1 and MultiMarkDown 3
tags:
- mmd3
- scrivener
- thesis
---

I [have another post](http://neilernst.net/2010/09/04/some-notes-on-integrating-mendeley-scrivener-multimarkdown-and-xelatex/#comment-362) that discusses my approach to writing my thesis using Scrivener. It's out of date now because I transitioned to [MultiMarkdown 3 (MMD3)](https://github.com/fletcher/peg-multimarkdown).

The Latex support in MMD3 is much simpler than the previous version. Instead of complicated XSLT transforms from the HTML formatted Markdown output, the new approach is to transition from the Markdown directly to Latex. It makes customizing the output much simpler - no more editing XSLT files. In the following, I assume you have a Scrivener document that contains the body of your work (e.g., Introduction, Related Work, Observations, Conclusions). Here's how to get started:

1. Scrivener still ships with MMD2, so you will need to install MMD3 on your Mac. Fortunately this is straightforward. Go to the [download page](https://github.com/fletcher/peg-multimarkdown/downloads) and download MultiMarkdown-Mac-3.0.1.pkg.zip and MultiMarkdown-Support-Mac-3.0.1.pkg.zip (as of July 2011). The support files will seamlessly integrate MMD3 with Scrivener. <del>I'm not sure how easy it is to revert, however, so be careful</del>  _(update: pretty easy - see[ this note](http://www.literatureandlatte.com/forum/viewtopic.php?f=21&t=14379#p102615))._ I do think it is ultimately easier to work with MMD3.

2. Now we need to add custom metadata to Scrivener to add the ancillary files for MMD3. I've found the easiest approach to be adding a Meta-Data text document as the first document in your Scrivener project (right-click the top folder in the Binder, Add-> New Text). Now we will tell MMD3 where to find the extra files for our Latex output. Here's what mine looks like:

` Base Header Level: 2
Bibtex: IEEEabrv,../../bibtex/thesis-new
Latex footer: ut-thesis-end
Bibliostyle: plainnat-nourl
Title: My Big Thesis
Author: Neil Alexander Ernst
Latex input: ut-thesis-begin
`

Order matters here. See [Fletcher's guide on metadata in MMD3](https://github.com/fletcher/peg-multimarkdown/wiki/How-do-I-create-a-MultiMarkdown-document%3F).

_Base header level_ is telling MMD3 that we want to create Chapters for each first-level Scrivener folder (I think [Base level 1 is "Part"](http://en.wikibooks.org/wiki/LaTeX/Document_Structure#Sectioning_Commands)). _Bibtex_ is the location of the bibtex files, relative to where we will run the "latex" or "pdflatex" commands. _Latex footer_ will be inserted at the end of the last piece of your Scrivener file using the Latex command \input{}. There is also _Latex header_, but as we will see that doesn't work well. The next command, _Bibliostyle_, will define the bibliography style for use with Bibtex. _Title_ and _Author_ are obvious, and I finish with _Latex input_. This is the beginning Latex of my thesis document, including packages, newly defined commands, etc. Now, because MMD3 will turn the metadata entries into variables in Latex, it is important that the input come **after** the definition of the title and author (otherwise there is an error). This is also why I avoid the use of the _Latex header_ metadata.

Now it is up to you to define what document class etc. to use for your document: MMD3, nicely, will just stick whatever is in input/footer/header into the appropriate place in the Latex file. There are some nice pre-defined input sections Fletcher Penney created, that you can download as well [on the Github site.](https://github.com/fletcher/peg-multimarkdown-latex-support)

Now in Scrivener, compile your document using the File->Compile.. and setting "Compile For..." at the bottom to "Multimarkdown->Latex". Note that it is important to disable conversion of two hyphens to an en-dash, otherwise HTML comments don't work, and you cannot escape the Latex properly.

Note: to escape Latex, surround the Latex (e.g., tables, math) with HTML comments (<!-- -->). The most useful MMD features, for me, are lists, which are just numbers or bullets (see the [Markdown syntax guide](http://daringfireball.net/projects/markdown/syntax)). Much simpler than the cumbersome \begin{itemize} syntax.

To use citations with MMD3, you can use the [#citename;] or [#citename] syntax for \citet{} or \citep{} Natbib commands, respectively. You can also do MMD footnotes with [^foot1] and [^foot1]:Footnote text. I haven't used any other advanced features of Markdown. The number one wish I have is for easy \ref \label syntax, <del>but I don't know how to do it</del> _(edit: see the [helpful post here](http://www.literatureandlatte.com/forum/viewtopic.php?f=21&t=14379#p102686))_. MMD3 automatically creates a \label{} after each section heading, based on the section name with no spaces.

I don't mind writing raw Latex: emacs+Auctex+refTex makes it pretty painless. But I found, for my 60,000+ word document, that it was much easier to do revision and editing in Scrivener: moving sections around, for example. It also uses Mac native spell-check which is pretty nice (Emacs's spelling I find clunky and slow).

My files for reference:



	
  * [Thesis preamble](https://gist.github.com/1109471)

	
  * [Thesis end section](https://gist.github.com/1109480)

	
  * [Subset of MMD output](https://gist.github.com/1109490)

	
  * [Subset of Latex output](https://gist.github.com/1109478)


