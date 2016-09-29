---

date: 2009-07-06 17:37:07+00:00
layout: post
title: Some thoughts on lean software development
tags:
- kanban
- lean
---

Lean software development is an attempt to take ideas from lean manufacturing, popularized by the Toyota Production System, and apply them to software development. Here are a few of my thoughts after skimming the surface of the field.

Lean optimizes a system to eliminate waste. Waste in software production is undeveloped features, stories, requirements. If you have a backlog of requests, or user stories, then you have waste.

A corollary is that 'time is money'. A lean software team seeks to optimize development to reduce the Lead Time, or time it takes to move a work item from idea to implemented (tested, accepted) feature.

A lean organization will have access to useful quantitative measurement tools, like cumulative flow diagrams. It is important to always understand how the process is moving: is the work item backlog too large? Where are the bottlenecks?

Lean sofware is built with a battery of tests. You cannot reliably develop software without testing. Constant refactoring is necessary to reduce complexity. My feeling is that this complexity is largely accidental, e.g. poor library choice, bad implementations, rather than essential. Presumably the essential complexity cannot be 'refactored' away (unless you are a rabid NIH fanboy).

There are several workflows that might help this process. Corey Ladas has an interesting set of posts on [conceptualizing workflows as petri nets](http://leansoftwareengineering.com/2009/06/08/workflow-patterns/).

Limiting work in progress (WIP) can be a useful way to enforce lean principles (e.g., focus on lead time rather than feature completeness). One way to do this is to use a signalling mechanism, popularized as a Kanban board, that indicates when a work item can be pulled from the previous work phase.

Lean is not waterfall. Waterfall is the antithesis of lean: plan and estimate _everything_ ahead of time. The problem for  people new to lean is that the lean process diagram _looks_ very waterfall, in that it is a sequential series of steps. However, iteration and incrementalism are at the heart of lean. We don't pretend to finish the entire product, but rather, a useable portion of it. If that portion is not to order, the appropriate work item goes back in the queue. Because everything is sequential at some level of granularity (a byproduct of the arrow of time!).

Estimation is evil and forces premature commitment; it is often treated by clients as set in stone guarantee, while the developers see it as a rough, and almost certainly changeable, guideline.

A challenge in a lean system is how to decide what subtasks constitute a work item. There is a time cost involved in assessing what a particular story demands (architecture, infrastructure, human resource). I've often seen this glossed over in discussions about lean or kanban, as the authors seem to assume that one has a useful backlog on hand.

Since time is the paramount cost, it often makes sense to apply what the Poppendiecks refer to as 'set-based' design: develop several competing options simulateneously, until circumstances force a choice. While there are other costs involved, the opportunity benefit from having the 'right' option available is typically higher.This is also known as deferring a choice until the 'last responsible moment' or real options theory.

The biggest risk in a lean initiative is that the organization will not engage completely with the dramatic change in thinking lean requires. Lean is not about tools or artifacts, it requires a paradigmatic shift in software development.

I still would like to see some studies on when lean **isn't** applicable or useful. Can it work with the JPL processes? Embedded software?

A related question concerns how to teach lean in undergraduate software courses. At the University of Toronto, we've tried to introduce agile techniques, typically Scrum sprints, to mixed results (in my opinion). The cycle times and project sizes seem too small to make [cowboy coding](http://en.wikipedia.org/wiki/Cowboy_coding) impossible. This is subject matter for another post, however.

Some references:



	
  * the blog [Lean Software Engineering](http://leansoftwareengineering.com/)

	
  * David Anderson: [agile management blog](http://www.agilemanagement.net/index.html) and [book](http://www.amazon.com/exec/obidos/ISBN=0131424602/thelairdorganisaA)

	
  * Derek Bailey's [article on the Theory of Constraints](http://www.lostechies.com/blogs/derickbailey/archive/2009/07/03/theory-of-constraints-productivity-metrics-in-software-development.aspx) in software

	
  * [Implementing Lean Software Development](http://www.amazon.com/Implementing-Lean-Software-Development-Addison-Wesley/dp/0321437381/ref=pd_sim_b_2) by Mary and Tom Poppendieck

	
  * [#kanban](http://search.twitter.com/search?q=%23kanban) on Twitter


