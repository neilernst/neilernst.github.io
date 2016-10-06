---

date: 2009-04-17 23:40:24+00:00
published: false
title: Why software engineering in science is important
tags:
- gnome
- msr
- mysql
- scientific software
---

Well, one data point, anyway.

As part of my work on mining the Gnome data repositories, I run Mysql queries against a set of tables that contain 'events', things like mailing list messages and bug reports, associated with a date. For historical reasons, there are two main tables (one bugs, one mailing lists). I wrote a python script to extract the data from these tables (using MySQLdb in Python), normalize it, then plot it using MatPlotlib.

The take-away, from my perspective, is that *only I* know this bug exists. I cannot see any of the reviewers taking the time to delve into the code at this level. We only see that level of -- fanaticism, really -- in very controversial papers or bold claims (climate change, cancer research). Hell, in software engineering, you're lucky to get the data, let alone the source code.

Code audits and review
