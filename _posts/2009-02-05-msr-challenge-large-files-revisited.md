---

date: 2009-02-05 17:08:59+00:00
layout: post
title: 'MSR Challenge: large files revisited'
tags:
- msr
- mysql
- vim
- xml
---

_This is part of the [MSR Challenge](http://www.neilernst.net/archives/tag/msr/) series._

Ignore my earlier advice with respect to handling large XML files. My new favorite tool is Vim. Although it takes a few minutes to do it, Vim can easily go to the correct line to fix problems. So if your XML is non-validating, just figure out the line number (should be printed in the `SaxException`), then open Vim with `vim +<line_num> <file_name>`. It thinks for a while, but opens to the correct line without trouble. Then you can delete the offending characters (highlighted for me as ^S) and save the file (wait a few more minutes).

My first problem was the non-valid characters (control characters); the second problem was a very lengthy string that MySQL won't accept (exceeds the buffer size). I'm storing the data in MySql for scale. At first, I tried increasing the buffer size for MySQL, which didn't work. I'm not sure if this was because I didn't set the correct variable (I'm using the MySQL administrator panel for OSX), but now I'm thinking it's just a ridiculous amount of text: if you check out the [bug report](http://bugzilla.gnome.org/show_bug.cgi?id=360318) you can see the person with the problem posted 100,000 lines of empty stack trace. Thanks buddy! I'm doing a horrible string concatenation thing to eliminate newlines, which is horribly inefficient, but seems to work on small-scale bug reports.

This type of MySQL error won't print the line number, but fortunately my parser prints the bug ids as it goes, so I could look for that id and retrieve the line number that way. My tool of choice was sed, and I just looked for:

`sed -n '/[ ]360318/{=;p;}'  <file_name>`, where 360318 is the bug id. [Here's where](http://www.unix.com/unix-dummies-questions-answers/11005-large-file-search.html#post39435) I got the syntax. The -n command suppresses output; then I look for a space followed by the bug id as the regular expression; finally the {=;p:} portion prints the match and the line number. I used a space in the regex because you would be surprised how often that six-digit number occurs in a 3 gig file.

I think I could have done this with a complicated sed program -- you have to store the bug_id, and only operate on the content in that bug, and since sed is not aware of xml elements, it would involve searching for other regexs as needed. I didn't feel like becoming a sed hacker, particularly. And yes, I suppose Emacs can manage this as well, but I haven't tried it. I actually considered ed, since it's line-based, but I couldn't figure out how to get it to go the line I wanted. I'm thinking one of my programming maxims will be, "If you are considering a solution involving ed, think of another solution."
