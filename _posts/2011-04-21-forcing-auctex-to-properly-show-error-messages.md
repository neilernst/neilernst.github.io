---

date: 2011-04-21 17:07:52+00:00
title: Forcing AucTex to properly show error messages
---

From the very-detailed-information dept:

I use Auctex with Emacs.app on my Mac to write papers. It's the best editor I've come across for Latex support.

I was having trouble with one feature, however. If your source file contains an error (e.g., an unescaped underscore), the engine via Auctex will complain when you try to compile. In my case, I always use pdflatex to generate PDF output.

At that point you will get `"Latex errors in `Document.tex output'. Use C-c ` to display"`. If you type C-c ` (TeX-next-error), the idea is that Emacs splits into two windows, with one window showing the error message, and the other showing the location of the problem in the source file. For some reason this wasn't working on my machine, and I kept getting this strange blank window.

After some digging, I've determined the problem to be that pdflatex does not report errors using file-name, only line number. This means Auctex cannot determine the proper source file to open.

Following information on [this mailing list post](http://old.nabble.com/2010-05-24--LaTeX-error-parsing-fails-due-to-closing-brackets-in-pdflatex-output-td28664402.html), the following steps should fix it (on a Mac):



	
  1. Edit the file `/usr/local/texlive/2010/texmf.cnf`. This is where user-specific customizations to the general config file for TexLive live.

	
  2. Add the line `file-line-error = t` at the end. This forces pdflatex to output the file name for each error.

	
  3. Update TexLive using `sudo tlmgr update -all` which, in addition to updating all the packages in your installation, will recognize your new config option. Possibly there is a shorter way to do this, but who doesn't want to update their packages?

	
  4. Done!


