---

date: 2006-07-25 17:18:30+00:00
title: More helpful LaTeX tips
---

Well, I find them helpful.

To figure out the word count of random PDFs, someone suggested

`pdftotext 'filename' ` then ` wc -w`. Piping it didn't work for me.

The other helpful tip concerns NatBib. It always published URLs for my references, and since I use [CiteUlike](http://www.citeulike.org), all my refs have URLs. It's handy, but not appropriate in most academic articles.

So, I did a barebones hack on the file abbrvnat.bst to remove all the commands that insert URLs, DOIs, ISBN, etc. Really there should be an option to remove them, but I didn't have the energy to do that -- I can barely decipher the TeX commands as it is. Here is the new file I created, [abbrvnat-nourl.bst](http://www.neilernst.net/docs/abbrvnat-nourl.bst).
