---

date: 2011-01-25 15:58:46+00:00
title: The industrial fallacy in software research
---

The **industrial fallacy**: the perception, common in research and industry, that industry always adopts the most efficient (and therefore correct) solution for a given need. E.g., use excel for requirements management because anything else falls into Agile's YAGNI/DRY principles.

My problem is that this assumes the need emerges context-free. In reality, the reasons for using excel have more to do with short-term constraints than a sustained analysis of business needs on a cost/value basis. Industry is rife with examples of companies who do something because that's how it has always been done, rather than a principled decision not to. The issue is that thought-leaders from the industrial side, such as Martin Fowler or 37 Signals or Joel Spolsky, are all located at the far right-end of the industrial maturity bell curve. Applying their ideas to companies at the other end, or even the middle, may not scale at all.

Should we abandon research on alternatives to SQL because it is so pervasive and useful? Or should we continue to challenge orthodoxy with new ideas and new tools, even when the immediate benefits are not obvious?


### Small examples


A lot of popular commentators, like Spolsky or 37 Signals, work on systems that are simple relative to the majority of business IT. There's a deceptive focus in the blogosphere on small-scale computing solutions, in particular early-stage startups. Even the challenge for Facebook, one of the largest websites in the world, has the benefit of a clarity of mission in which the software is ineluctably intertwined with the business mission. Other companies, such as large banks, face the challenge that the software is not the core competency, and subsequently must jockey for position with other business units, like accounting, marketing, human resources, etc. And yet IT is not really another business function, anymore, but central to the ability to deliver value to customers.

Look at [this article from the Economist](http://www.economist.com/node/16646044), which makes the point that IT systems at banks have to manage thousands of counter-party obligations and deliver answers in seconds as to whether the bank owes 3 billion $ or 30 billion $. There is just no way that lessons from 37 Signals have anything but the very broadest applicability in this case. [Scott Ambler](https://www.ibm.com/developerworks/mydeveloperworks/blogs/ambler/entry/agile_and_domain_complexity18?lang=en) and [David Anderson](http://www.agilemanagement.net/) are two people who work on so-called 'agility-at-scale', which deals with the unsexy but extraordinarily important issues of software development in complex, multi-stakeholder environments. The industrial fallacy, in this case, would have us believe that agile has won, that there is no need for requirements up-front, no need for software architecture and design (or rather, that Agile = Scrum or XP or ..). And yet I remain unaware of (even anecdotal) case studies of successful agile development for projects in the range of millions of dollars, which are common in industry. Note that I mean agile as in "follows an agile methodology", not agile as in "ad-hoc". I'm sure there is plenty of the latter happening!

It doesn't matter if you finish on-time and on-budget if you don't deliver value. And conversely, if you go over-budget but deliver tremendous value, isn't that acceptable? We need to get away from the view that software == file with code in it. Software is the system that enables the requirements to be satisfied. In the same way that ultimately the home owner must oversee that his/her requirements have been met by the various subsystems (plumbing, electrical, framing, etc.), so must the business customer take responsibility for the software requirements.
  *[DRY]: Don't Repeat Yourself
  *[YAGNI]: You Ain't Gonna Need It
