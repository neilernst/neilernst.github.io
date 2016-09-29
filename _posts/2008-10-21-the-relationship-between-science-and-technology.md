---

date: 2008-10-21 16:38:13+00:00
layout: post
title: The relationship between science and technology
tags:
- aircraft
- jackson
- nasa
- normal design
- vincenti
---

_Vincenti, Walter, 1990. "[What Engineers Know and How they Know It](http://books.google.com/books?id=zXJTAAAAMAAJ&q=What+Engineers+Know+and+How+They+Know+It:+Analytical+Studies+from+Aeronautical+History&dq=What+Engineers+Know+and+How+They+Know+It:+Analytical+Studies+from+Aeronautical+History&ei=OFz3SICjMZPyMsnOidQI&pgis=1): analytical studies from aeronautical history". Johns Hopkins University Press._

At [RE08](http://sites.upc.edu/~www-gessi/re08/) in Barcelona, [Michael Jackson](http://mcs.open.ac.uk/mj665/) mentioned this book as a must-read for people in requirements engineering, and respecting my elders, I dutifully picked it up.

The first contribution of this book (most important?) is to highlight that engineering (and I sort of unthinkingly lump software engineering in there, for the moment) is NOT just the application of scientific principles to real-world problems. They are 'separate spheres of knowledge'.  Anyone who has tried to construct the most rudimentary technology -- e.g., a tree-fort, change a tire, etc. can verify this. While on paper the solution is obvious, in harsh light of day, the nail doesn't go in deep enough, the lugnuts are seized, and so on.

I found the book often went into excessive detail, of interest only to aeronautic buffs, but there were sections at the beginning and conclusion of each chapter that were highly interesting. Perhaps most relevant to my research, and to software engineering, was the chapter on aircraft qualities. Qualities include aspects like how 'heavy' the control stick is, how stable the plane flies, etc. Anyone who has driven several different types of car can relate to these properties, I would think: does the car shimmy at high speeds (like my first car, an 89 Toyota Tercel)? Do the brakes feel squishy? Does the door have a convincing _thunk_ when closing, or a tinny _clang?_

For early aircraft design, these qualities were secondary to functional aspects: 'With the essential proviso, of course, that an airplane can be reasonably and safely flown by the pilot, its utility depends crucially on these other characteristics [speed, range, ceiling, carrying capacity ...]'. He goes on to add that only when these functional properties were largely satisfied (and here I assume he means that there were diminishing returns on further research into these functional characteristics) was flying quality considered. Eventually, specs for new aircraft came to include sections on flying qualities, encapsulating 'the notion that desired subjective perceptions of pilots could be attained though objective specifications for designers'. Because these qualities were subjective, the specs tended to be design guides to assess tradeoffs rather than objective, measurable requirements (much like in NFRs and software design).

Vincenti argues that engineering knowledge grows via an evolutionary variation-selection process; as a result, 'technology's failures require examination as well as its successes'. The important lesson is that approaches that attempt to design something perfectly from the beginning seem doomed to failure. The best we can do is prepare to throw one version away, until we have a good body of evidence to support one particular solution. For example, NASA tries to re-use Mars expedition software and hardware as much as possible; e.g., the particular circuit board, the software language, and so on. The reason for this, as Jackson explained in his keynote, is to leverage the benefits from "Normal design" and [specialization.](http://sites.upc.edu/~www-gessi/re08/PUBLIC_SLIDES/michaelJacksonKeynote.pdf)The characteristics are known and well-tested; keeping these things constant allows for incremental specialization at the margins (e.g., improved science packages, new rocket engine, etc.)

My take-away is that the most important thing to understand in approaching a new problem is what pieces of that problem are normal and what pieces radical. Focusing on the radical is key, because we can assume this is where the failures and iteration will need to happen.
