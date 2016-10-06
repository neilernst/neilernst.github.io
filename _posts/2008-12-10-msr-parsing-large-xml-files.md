---

date: 2008-12-10 15:36:32+00:00
title: 'MSR: parsing large XML files'
tags:
- python
- unicode
- xml
---

_This is part of the [MSR Challenge](http://www.neilernst.net/archives/tag/msr/) series._

The Gnome bugzilla dump is an <del>XML file</del> file that is supposedly valid XML that is approximately <del>3.21 Gigawatts</del> 3.5 gigabytes in size. Needless to say this is an impressively sized amount of data. There's a common belief in the community that scale changes everything, and my recent encounters bear this out.

I've designed my parser to extract data from the file using SAX, which is a stream-based XML parser. It doesn't try to load the model into memory like DOM, or elementTree, in other words. I tested my SAX approach on some sample data I extracted, and got that working no problem. Next step was to test it on the real thing, which is (I think) an overnight run.

Some of the lessons I've since learned:



	
  * Run long-running processes from the command-line, not Eclipse. That way you can log in from home to check the status, kill the process, etc. 

	
  * Generate progress information, e.g., bugs processed, so one can tell that something is happening.

	
  * Write data to a file immediately, so that you can check the output remotely.

	
  * Code inspection is your friend. Errors that didn't exist in my example (e.g., misformed dates) do exist in the data file.

	
  * Character handling is hard. I got some malformed data (line 50 million, usefully), which killed the parser. Now I have to figure out how to work around this. 

	
  * The `time` command is your friend. It gives a tiny bit of profiling data, which is often enough.



My recent difficulty was in handling ill-formed character data. In XML, [certain characters are invalid](http://http://www.w3.org/TR/2006/REC-xml-20060816/#charsets), and encountering one of them causes the parser to halt. Apparently one cannot simply route around it either. So, I've had to extend my codebase to filter out these annoying characters first, then parse the XML.

My first approach was a [regular expression](http://www.w3.org/International/questions/qa-forms-utf-8.en.php) mentioned by Sam Ruby, which seems to work fine --- on small files. It died on my large dataset, mainly due to my ignorance of [UTF-8 and the BOM mark](http://evanjones.ca/python-utf8.html), so I moved on to a better method: the `tr` unix tool, as follows:

`tr -d [:cntrl:]  out.xml`

On my machine (3 gigs RAM, P4 2.4), this took 5 minutes to process the file. Nice.

If you have trouble with a file's encoding or characters, I recommend just looking at it with a [hex editor like GHex2](http://live.gnome.org/Ghex), since this will show all the strangeness; and the useful [UTF-8 decoder page](http://www.ltg.ed.ac.uk/~richard/utf-8.cgi) to see what these hex code points mean.
