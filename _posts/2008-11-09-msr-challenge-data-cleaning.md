---

date: 2008-11-09 22:31:10+00:00
title: 'MSR Challenge: data cleaning'
tags:
- deskbar
- msr
- mysql
---

_This is part of the [MSR Challenge](http://www.neilernst.net/archives/tag/msr/) series._

I've been spending the last few days writing my parsing code for the Gnome data sets. Friday and Sunday have been dedicated to parsing mailing list data. I got a dump of a sample mailing list, the Deskbar Applet list. It's in MySQL format, so I loaded it into Mysql without any major trouble. I then imported the python MySQLdb (case matters!) library, and got to work.
I open a connection to the db with the 'deskbar' table, then run a query: `"SELECT message_body, original_date, subject FROM messages"`. I then do `cursor.fetchall()` to retrieve the rows (1091 rows). Since I used a `MySQLdb.cursors.DictCursor`, the resultset is a dictionary with the column names as the keys. Now it's a simple matter of passing those things into my GnomeDataObject schema (event, date, RSN) as appropriate. Again, simple, right?
Well, no. I usually try all this from the REPL environment in Python, and occasionally I would see this strange result for the message body: `'[<email.Message.Message instance at 0xb76e324c>, <email.Message.Message instance at 0xb769a90c>]'`. What puzzled me was that this is actually Python, using the email system library. At first I thought the mysql connector was doing type conversion, but sadly, this is really just a string.

So the message that is [supposed to be like this](http://mail.gnome.org/archives/deskbar-applet-list/2005-October/msg00034.html) is output into the db file as some sort of weird serialization result. From what I can tell so far, that's because the person who wrote the dump script against the list mbox files made a mistake when parsing some special type of message, threaded or something like that.

From inspection, this problem affects around 25% of the messages in the list. This is definitely a serious problem for validity, although if it is random (and not, for example, just occuring to one mailing list contributor, like one who is really interested in some NFR), then no biggy.

My next step will be to try and reproduce this with another mailing list dump file. If it's still a problem, I'll need to contact the person who produced the data or else just extract the data from the mbox files myself.
