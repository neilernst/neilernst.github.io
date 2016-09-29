---

date: 2005-05-27 22:17:45+00:00
layout: post
title: Really Simple Requirements
---

There are numerous requirements models and frameworks floating around.  Often, in a pique of mathematical frenzy, researchers (often with an AI background) will have shoehorned requirements into some logical, well-defined formalism (viz. [KAOS](http://www.info.ucl.ac.be/research/projects/AVL/ReqEng.html), [TELOS](http://sherry.ifi.unizh.ch/mylopoulos90telos.html)).  Is software development a formal process?  Well, it may well turn out that's what works best, but for now, formal specs and rigid requirements are often useless paper, intended to fulfill contractual obligations.  Someone once wrote that software right now is exploratory, rather than defined -- we're still looking for where to put the bridge, not how to build it.

Yet requirements are important, indeed, central to success.  Your software may be successful without meeting any requirements, but probably not because you did anything right.  What isn't central are the formality of the requirements.  The FogCreek intern project, [Project Aardvark](http://www.projectaardvark.com/posts/pollack/may/26.html),
made mention that the most important tool used was the weighty and complete specification, which clearly detailed how the user would interact with the app, what interface it should provide and expect, and so on.  However, a key point was that the spec was also deliberately flexible: 

<blockquote>Questions that cannot be easily answered without running prototypes are prominently flagged so that we know where we will experience potential problems and can prepare for them with flexible code.</blockquote>

 Clearly someone at FogCreek put a lot of work into defining the spec, based on requirements.  But they can afford to use the[ program manager concept](http://www.joelonsoftware.com/articles/fog0000000034.html); not everyone can, especially students in 3 month programming courses (although arguably they should, they won't.  We all know it.)

What software development needs is Really Simple Requirements (RSR).  RSR would define lightweight objectives to be met, in a semi-formal way (we want to avoid ambiguity and stave off the question, "What did you mean by this?").  RSR would allow one to easily identify test cases to be created in order to validate the product to the spec (so RSR should be iterative, then).  Tests are subsets of RSR.  There would be parts of RSR that are non-functional (soft goals the system needs to try and satisfy).  RSR would also be flexible enough to be changed when new issues arose -- e.g. if using an agile process.  But unlike [XP](http://c2.com/cgi/wiki?SimplifyTheRequirements), for example, RSR would try and define overarching purposes for the system (recognizing that XP often fails to see the big picture, particularly in large projects)

The best part?  RSR might actually be used.  A used requirements method is more important than a totally correct one.  We need simple tools that make life easier, like CVS, or PHP, or AJAX.  Who is going to use KAOS for real?  Unless some manager somewhere says they need documentation, and the programmers decide that, in order to justify this, they should use a paper-intensive documentation strategy, and so they pick KAOS and the Rational Unified Method to document stuff they won't do anyway.

One of the key areas for research is the gap between requirement and specification.  This is the area the UML fuzzily covers: is it a requirements doc, or a product spec?

Essential ingredients in RSR:


  1. Demonstrably better than 'just code it'


  2. As easy to use as given programming language syntax


  3. Live with the code (if you change either code or requirements,  the other must change).


  4. Have well-defined schema


  5. Written in XML


  6. Flexible and adaptive (to new concerns, to new requests)


  7. Relatively unambiguous


  8. Extractable from the source to allow for XSLT transforms: e.g., to present to managers


This is starting to sound somewhat like [literate programming](http://www.literateprogramming.com/), Knuth's suggestion that TEX be embedded in code as a living document.
