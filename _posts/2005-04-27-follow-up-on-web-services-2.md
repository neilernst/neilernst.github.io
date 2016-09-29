---

date: 2005-04-27 17:25:48+00:00
layout: post
title: Follow-up on "Web Services"
---

Further to the [previous post](http://www.neilernst.net/blog/archives/2005/apis-and-messages/):



[Bosworth's Web of Data](http://www.onlamp.com/pub/a/onlamp/2005/04/22/bosworth.html) by Daniel H. Steinberg -- Google's Adam Bosworth's keynote at the 2005 MySQL Users Conference was a call to audience members to "do for information what HTTP did for user interface." The web was successful because it offered a simple, sloppy, standards-based, scalable platform, and the challenge is to take a database and do the same. 



I guess 2 things come to mind.

1. It's a little tiresome to hear intelligent people (ok, [Wolfowitz ](http://www.thewashingtonnote.com/archives/000383.html)is 'intelligent' too, perhaps that word is losing all meaning) continue to mischaracterize the [Semantic Web vision of Berners-Lee](http://www.w3.org/2001/sw/) as some kind of 'ontology of everything'.  It's pretty obvious that's almost the opposite of what it's about -- notwithstanding some folks who would like to do that.  Danny Ayers has a [good comment](http://www.onlamp.com/cs/user/view/cs_msg/60311) on this below the original Steinberg article.

2. Admittedly, simple is best, and [Postel's law](http://essaysfromexodus.scripting.com/postelsLaw) seems pretty effective.  But the model of "loose agreement, loose coupling" seems misleading.  Sure, if all you want to do is consume Google services, or Amazon, or some other major provider (defined as 1 to many, many users), then this model works.  After all, who's going to mess with Amazon?  If the majority are happy, the data model stays.

But I think the SW vision looks a little further down the road than this.  It's looking ahead to a time when peer-to-peer data and service sharing is more commonplace.  Then the interaction model is 1 to several, or even 1 to 1.  In that case, we need a more tractable and comprehensible way of exchanging service specifications than just publishing a totally random schema in XML.

I think.


[edit] More [interesting discussion](http://www.dehora.net/journal/2005/04/rsq_really_simple_querying.html) from Bill de Hora.
