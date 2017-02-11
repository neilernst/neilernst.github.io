---

date: 2004-09-14 11:28:42+00:00
title: Latex Hints, Tips, Links
---

Notes on LaTeX:


#### Writing letters

See [this page](http://www.tex.ac.uk/cgi-bin/texfaq2html?label=letterclass) for more details.  In general, though, the default letter package blows, and the package [newlfm ](http://www.tex.ac.uk/tex-archive/macros/latex/contrib/newlfm/)is the way to go.  You should be able to install directly using MiKTeX, indeed, if you use this template, it will do it all for you.

Template (from newlfm manual):
`\documentclass[stdletter]{newlfm}
\nameto{George Bush} \addrto{\parbox{2in}{The White House \ Washington, DC}}
\namefrom{Paul Thompson} \addrfrom{\parbox{2in}{The Pink House \ Belleville, IL}}
\begin{document}
\closeline{Sincerely yours,} \greetto{Dear Mr. Bush,}
\begin{newlfm}
How are the azaleas?
\end{newlfm}
\end{document}`



#### Figures

As part of a paper I co-authored we've included .eps figures in the TEX source.  For some reason I was getting the error `! LaTeX Error: Cannot determine size of graphic in _{some image}_(no BoundingBox).`  After some digging on Google, I found a solution [on this thread](http://aa11.cjb.net/miktex/2000/12/0162.html).  What worked for me was to open the image in Ghostview, then use Ghostview's ps to eps option to add the EPS bounding information.  I'm not sure why the image program (Illustrator, I think) wasn't adding this, but now it seems to be working.

Figure insertion code:
`\begin{figure*}
	\centering
	\includegraphics[width=7in]{mtg-sched-ah}
	\caption{Abstraction-Decomposition Hierarchy for the meeting scheduler domain}
	\label{fig:AH}
\end{figure*}`
Use figure* environment to get 2 col floats.



#### Links


[The TUG FAQ](http://www.tex.ac.uk/cgi-bin/texfaq2html)
[Goddard TeX manual (invaluable)](http://www.giss.nasa.gov/latex/ltx-2.html)
[IEEE style how-to (pdf)](http://computer.org/author/transguide/IEEEtran_HOWTO.pdf)
