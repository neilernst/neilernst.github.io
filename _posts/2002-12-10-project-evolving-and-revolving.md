---

date: 2002-12-10 21:32:00+00:00
layout: post
title: Project evolving and revolving
---

Today was ok in terms of accomplishments. Dave gave a good presentation on PROMPT. There are many interesting problems to work on in that space.
I have now started using a wireless connection after the tech guys spent some frustrating time debugging the system. Seems just about as fast as the wire. But YMMV.

So, the project. I have validated the 3 rdf files at the RDF validator site which is good. I also looked for some kind of text extraction tool in order to parse the mail messages. I have settled on a really simple one, Lucene from the Jakarta project. It is merely a text index and query tool. I hope to extract some keywords from our group emails and use that to create some "Document" objects for the instance store. On the "Person" side, I will create some more people, perhaps first designing a web UI to do this automatically and allow my group to update their pages individually. So this is progressing fine. Finally, Dave Manning has compiled PHP with the Java libraries, so I will endeavour to use this rather than servlets to communicate with Jena.
Ow, my  arms are sore..
