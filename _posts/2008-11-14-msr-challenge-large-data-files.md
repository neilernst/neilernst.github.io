---

date: 2008-11-14 15:03:09+00:00
layout: post
title: 'MSR Challenge: large data files'
tags:
- bugzilla
- msr
- xml
---

_This is part of the [MSR Challenge](http://www.neilernst.net/archives/tag/msr/) series._

This week's challenge was to tackle the Bugzilla logs. The data I have is a complete dump of the Gnome bugzilla database, which is enormous -- 3.5 gigs. Of course, I don't need all of this data, just the data that relates to particular projects (e.g., Deskbar).

I think there are two approaches. One is bottom-up, so to speak, where I focus on the details of a specific bug. For this study, I need to extract the date the bug was filed and the subject and comment for that posting. Bugzilla allows follow-up comments, so I am going to extract those as separate GnomeDataObjects as well. For now, I am discarding metadata such as the bug's status and whether it is an error or enhancement (other researchers are working there). I'm just focusing on  the bug comments/description and the date of that comment. If the comment is a system event, such as "BUG XXX is a duplicate of YYY" then I ignore those events.

So I have some hacky code that reads in my sample xml file and parses the relevant nodes to extract that data. Hacky, because I'm too lazy to write a search for the node I want, and I'm just using list positions (e.g., `entry.ChildNodes[4].childNodes[0].data` where entry is a bug).

As I was doing this, I realized that this isn't going to scale too well on a 3 gigabyte file. Rather than do a time-consuming iteration over all the bugs, throwing out those that aren't in the appropriate project, I need to do some sort of stream processing ... which is where SAX comes in.

My other consideration was whether I should just munge this all into a huge database, but I can't find a simple enough way to do that online. The third alternative would be to write XSLT to split the file or reject the unwanted elements, but I don't know XSLT at all. And from all accounts, I'm better off that way :)

SAX is like an impoverished event-processor: it calls specific methods (e.g., beginElement) when that event occurs (e.g., it encounters an XML element). This is cool, in that it's like just-in-time processing, and avoids a huge in-memory data structure; on the other hand, your code (at least MY code) is full of `if` statements and switches, which is crapulent. But it looks to be working, for now.
Here's some sample data as an illustration:

    
    
    
    
        2002-05-28 16:29:00
    
    
        scaffold
    
    
    
    
    
    
    
           xxxx@hotmail.com
    
    
            2002-05-28 15:31:00
    
    
    
            Package: anjuta2
    Severity: normal
    Version: 0.11.3
    Synopsis: The Matrix
    Bugzilla-Product: anjuta2
    Bugzilla-Component: shell
    
    Description:
    I was in the site www.thematrix.com and the browser crached !
    
    Thkz
    
    
    Debugging Information:
    [some stack trace]
    
    
    
    
           xxxx@hmc.edu
    
    
            2002-07-29 14:03:00
    
    
    *** This bug has been marked as a duplicate of 59361 **
    
    
    
    
    
