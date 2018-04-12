---

date: 2007-08-24 18:53:48+00:00
title: An explanation for UML usage statistics?
tags:
- complexity
- nasa
- scr
- software
- uml
---

[Julio Leite reported](http://amazinnggg.blogspot.com/2006/11/uml-usage.html) on UML usage statistics, showing penetration of UML is ~23%. In an upcoming publication, [Jorge Aranda](http://catenary.wordpress.com/) surveyed small-sized software firms and found their use of modeling to be quite low, and typically of the [UMLAsSketch](http://www.martinfowler.com/bliki/UmlAsSketch.html) variety. So...

Q. Why is UML so little-used, despite the fairly heavy-duty marketing and machinery behind it?

A. The long tail.  See the graph below.

My contention is that of software development teams, the vast majority are working on less complex projects. For example, a month-long website redesign, a custom CRM extension, etc., etc. There are comparatively fewer working on multi-month, disruptive software systems.

Some questions, other than where can we validate such a claim.



	
  1. How can we measure complexity? Time to completion? Size of written source code? Platforms targeted? Risk potential? Project budget? I would probably lean to project budget as a very rough guide -- we all use dollars, and the cost usually reflects an a priori assumption about complexity.

	
  2. What sorts of tools would the mushy middle of this tail need? I.e., those firms doing median complexity projects? Clearly the companies at the head of the curve don't need the Thor's hammer of UML or [DOORS](http://www.telelogic.com/index.cfm?) when the Owen's* hammer of technologies like Excel do just as well. But there must be a tipping point where these technologies start to get more and more useful and important. _But_

	
  3. Is there good empirical evidence that even the long-tail denizens need UML, DOORS, or Rational? Indeed, we might even expect that such large-scale firms would customize requirements management, configuration management and other helper technologies for their own purposes. This seems to be the case for Linux ([GIT](http://git.or.cz/)), NASA ([SCR](http://portal.acm.org/citation.cfm?id=76140), formal methods, etc.), and probably others.


[
![](http://services.alphaworks.ibm.com/manyeyes/static-resources/snapshot/89ade5ae14209c140114992b7644237d.jpeg)
![](http://services.alphaworks.ibm.com/manyeyes/images2/blog_this_caption.jpg)
](http://services.alphaworks.ibm.com/manyeyes/view/SIk76IsOtha6xB0FqhGaI2-)
* Thor's weaker and lesser-known half brother, an accountant in Little Wopping, England.
