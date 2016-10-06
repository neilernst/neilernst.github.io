---

date: 2005-04-21 20:06:25+00:00
title: APIs and messages
---

I've been following the REST vs. WS-* debate for a while, but one thing still confuses me.  As Tim Bray [mentions](http://www.businessweek.com/technology/content/apr2005/tc20050421_1855.htm), "Web services are an agreement to work with XML messages instead of APIs."  I just don't grok the distinction between an API and a message format.  Ultimately someone has to agree on the format, right?  If you're Amazon, you still define the interface the messages adhere to, or no?

I guess my current feeling is that regardless of whether CORBA, DCOM, REST, etc. are used, two things have to happen.  One is that parties involved (consumer and provider) have to agree on a format for the request/message/function call - is it ASM, other protocols, SOAP over XML, etc.  There seems to be a big win now that people generally use XML over HTTP for the bits in the message - interoperability wins.  The second thing is that the two parties have to agree on what can be done with the service/function/object.  E.g., can I get the book ISBN?  How is it formatted?  What if there are two different editions?

This can be distinguished as agreement on syntax, and agreement on semantics.  Rephrased, How can I get something, and what can I get.   Then, almost secondary to those negotiations, one can decide how to actually invoke the service.  That seems to be where REST, WS-*, CORBA debates happen.  Should it be XML over HTTP, or should I add more structure to the message (security, identity, choreography,etc.)?  Should I act directly on the object, or abstract it into a message/service architecture?

I'm likely mis-characterizing something, but I can't honestly see what the disagreements are.  Perhaps, as Tim says, the problem was getting people to agree on syntax, in order to have the other arguments.
