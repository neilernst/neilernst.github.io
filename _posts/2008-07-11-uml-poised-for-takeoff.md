---

date: 2008-07-11 15:32:53+00:00
title: UML - Poised for takeoff?
tags:
- microsoft
- uml
---

There has been [some](http://catenary.wordpress.com/2006/11/13/uml-usage-survey/) talk about the 'pending death' of UML. Industry consensus seems to be that it is mainly useful for sketching designs or communicating use cases to stakeholders. However, some of the modeling community have taken heart from recent remarks from Microsoft. In a [recent keynote](http://www.microsoft.com/presspass/exec/billg/speeches/2008/06-03teched.mspx) address, Bill Gates was asked the following question (via [the Register](http://www.theregister.co.uk/2008/06/17/microsoft_uml_oslo/)):


<blockquote>**QUESTION:** I'm (Sheila Shovelin ?) from FedEx.

I have a question. You mentioned modeling tools as being a focus. Is there any effort being made to couple with the initiatives of the object modeling group?

**BILL GATES:** Yeah, which standards is object modeling group in?  OMG, is that the --

**QUESTION:** UML.

**BILL GATES:** UML, okay.

**QUESTION:** Like the class diagrams you have in Visual Studio, they're not quite UML.

**BILL GATES:** Right. Yeah, we'll have additional support for UML in Visual Studio 10 for the specific modeling tools that are there. Then as we move forward and take the modeling platform to the next layer, we'll get even more ability for you to create your own models.

So, you're absolutely right that the modeling world is fairly disparate today. Even at Microsoft our people who do our business applications have some of their modeling environment. Excel in a sense is a pretty limited modeling type environment.

The thing that we've recognized is that by bringing those things together we can actually enable new things like what you do across the lifetime of an application. And underneath these models we actually use UML.

We think it's very rare -- a very rare person would actually want to look directly at the UML because it's so kind of abstract, but underneath, both in terms of exchange with other people's products and some of the exchange we're doing between our own products, we do have UML based subscriptions of these models.

I'm not actually a UML expert. Hopefully, we have some breakouts where we can get more into that -- okay, I guess (Brian Harry ?) will do that, where you'll get more of a sense of this modeling roadmap, and how we connect up to all the modeling standards.</blockquote>


My interpretation of this is not quite so rosy... first, I think it's clear UML is hardly on the radar for Microsoft's senior executives. Secondly, it seems like UML is used mainly as the backend representation format, and not the user-facing modeling language -- "a very rare person would actually want to look directly at the UML".

What is positive is that Microsoft seems to be acknowledging the need for some form of hierarchical abstraction mechanism. They would like to enable developers to work with models of the architecture that are automatically created from source. This certainly seems to support the value of modeling, but I'm less certain it's an endorsement of model-driven architecture or formal UML. And let's keep in mind the vast numbers of developers Microsoft works with.  Perhaps my colleague Jorge, now at Microsoft for the summer, can shed some light on this issue.
