---

date: 2007-07-06 20:19:24+00:00
layout: post
title: Agile software development and military procurement
tags:
- agile
- military
---

Can agile methods for software development be applied to military-scale projects? There was an interesting talk on this subject by [Tony Shepard](http://www.rmc.ca/academic/elec/staff/shepard_e.htm) [(papers)](http://www.informatik.uni-trier.de/~ley/db/indices/a-tree/s/Shepard:Terry.html),  emeritus Professor at Kingston's Royal Military College and Queen's. Although retiring, Dr. Shepard is keen to continue research on agile methods (there's a lesson in there somewhere...). The talk was full of interesting anecdotes about various military procurement problems. The most discussed were the Canadian Forces [Land Forces Command and Control System](http://www.gdcanada.com/content/detail.cfm?acronym=LCSS) (LFCCS) and the [US Coast Guard's Deepwater](http://www.uscg.mil/deepwater/) program.

LFCCS is a 50 year old project to automate the way that military commanders manage assets (soldiers, tanks, artillery etc.). Delivered in 2000, it was completely unusable on delivery because it didn't meet performance or UI requirements. Recently a few pieces have apparently been used successfully. In short, a software failure. Shepard's question is whether [agile principles](http://agilemanifesto.org/principles.html) would have helped. He delineated these principles as 1) customer-centric 2) win-win between contractor and customer 3) iterative development (I may be remembering wrong on the last point).

He then outlined the challenges military projects face. It can be difficult to get customer representation -- it's often not wanted or not available. In the LFCCS example, field commanders who would use the system never got to try it out and provide feedback. Because there are very few military contractors available, the contracting model can be very adversarial -- "you want a change, it'll cost you".  Agile processes would define needs, and both parties would be expected to work towards providing a successful project. Finally, the LFCCS system was never tested until delivery, when performance problems became obvious.

The typical knock on agile development models is that they don't scale well -- as in, "agile -- yeah, that's good for small companies".  There have been several [debates](http://c2.com/cgi/wiki?ExtremeProgrammingMayScaleUp) [on](http://www.agilenetwork.ca/ws2003/) the topic. Shepard mentioned Prof. [Phillipe Kruchten](http://en.wikipedia.org/wiki/Philippe_Kruchten), who pioneered the Rational Unified Process. Apparently he applied RUP to the design of the Canadian Air-Traffic Control System overhaul. Breaking teams into architects and designers, he attempted to scale agility to a several hundred person team at IBM.

A colleague claimed that because military systems have fixed requirements, are often safety-critical, and there are very few capable contractors, agility is inappropriate in this context. I'm not so sure. Interestingly, Shepard mentioned that the US military is actively interested in leveraging open-source development practices, as well as software, because it would force contractors to standardize and alleviate lock-in. An argument, and a strong argument, in favour of agility is that the current model clearly works very poorly, if at all. I don't see why the agile manifesto can't be applied to software of any size.  For example, favouring 'working software' over documentation is a good idea in every case I can see. There's no need for the software to actually be doing anything, but even a prototype of the LFCCS would have been a huge improvement.

One component of the [XP agile method](http://en.wikipedia.org/wiki/Extreme_Programming) is to use user stories to generate the goals for each cycle of development. I asked Dr. Shepard about using user stories instead of 'big requirements up-front'. While not all that familiar with them(!), he seemed skeptical one could generate enough detail to make development feasible, and avoid the Deepwater problems (in Deepwater, the Coast Guard turned requirements gathering over to the contractor, so the contractor was responsible for both requirements and implementation - and did neither one well). I think, though, that a goal elicitation technique, maybe similar to [Neil Maiden's work](http://hcid.soi.city.ac.uk/research/Rescue.html), could be more useful than reams of paper requirements. To me, the days of defining requirements by analysts sitting in offices has to be coming to a close. These systems are so enormous, and so important, that more flexible, change-adaptive techniques are required.

There are a number of interesting master's theses being produced at RMC Kingston. The neat thing about RMC is that many of the students have access to large-scale military systems, like LFCCS. Paul Mondroux is apparently writing a thesis on traceability and risk analysis. He looks at a military system  which has 3000 requirements and assesses, retrospectively, how well those requirements can be traced to defects. He favours an approach that first classifies requirements based on risk, and then either does full traceability (manual), semi-automatic (like [Jane Cleland-Huang's](http://facweb.cti.depaul.edu/jhuang/) work), or none at all (if the defect risk is minimal). This seems like a sound approach.

All in all, it was a very instructive talk. It's too bad, really, that it can be so hard to get access to military data - it's ripe for empirical analysis.

By the way, did you realize there's a [14th Software Engineering Squadron](http://www.airforce.forces.gc.ca/14wing/squadron/14ses_e.asp) in Canada? Neat.