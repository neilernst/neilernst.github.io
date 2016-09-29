---

date: 2009-02-07 04:54:21+00:00
layout: post
title: Matplotlib and Mac OS 10.5.6 compiler error resolved
tags:
- macports
- matplotlib
- osx
---

Just for future reference, and others in the same situation:

I tried to install [MatPlotLib](http://matplotlib.sourceforge.net/) (0.98.5.2), the Python graphing library, on my Mac. I was initially trying 'easy_install'; when it failed I tried it from source. My problem seems to be that the [MacPorts](http://www.macports.org/) project installs libraries that aren't necessarily compatible with other applications not using Ports.

In order to get the compile to work, I had to uninstall my libpng macPorts files (and with them the Ghostscript and TeTex libraries), and finally, since I had the same error [as reported here](http://www.mail-archive.com/matplotlib-users@lists.sourceforge.net/msg09474.html), my fontconfig and freetype libraries. Once they were uninstalled, I downloaded freetype from the [sourceforge page](http://freetype.sourceforge.net/download.html), ditto libpng. After that, I no longer received the error.  The advice given on the Matplotlib mailing list scared me (edit all my Python config files!?), so I just scanned the linker error and thought the freetype library might have been the problem. Sure enough ...

Matplotlib does have an abnormal number of dependencies, as I recall one of the reasons it wasn't used with DrProject.

I also have been finding that MacPorts is less than useful: most software is available as a package for Macs, and it introduces too many conflicting libraries. It's a good effort, but really, these types of package managers only work really well when used exclusively, like I do on Ubuntu.
