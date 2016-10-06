---

date: 2006-01-29 22:26:14+00:00
title: More latex tips
---

After some more LaTeX mucking around, I've collected the following tips.  What I wanted was an article with centered sections, no section/subsection numbers, and 1 inch margins with 12 pt text.  This was for a particular conference with no provided .cls file.

To center sections:

`\section{\protect \centering Introduction}`

To center a bibliography (can also rename the section):

`\renewcommand{\refname}{\protect \centering References}}`

To remove section numbering:

`\setcounter{secnumdepth}{-1} `

To fix margins (note, dangerous because this is what LaTex is good at):

`\setlength{\textheight}{9in}
\setlength{\topmargin}{-0.5in}
\setlength{\evensidemargin}{0.0in}
\setlength{\oddsidemargin}{0.0in}
\setlength{\textwidth}{6.5in}`

To reduce separation between bibitems:

`\setlength{\bibsep}{1pt}`

To make a new list type which isn't as spaced out:

`\newenvironment{myd}{
\begin{description}
\setlength{\itemsep}{1pt}
\setlength{\parskip}{0pt}
\setlength{\parsep}{0pt}}
{
\end{description}
}`
