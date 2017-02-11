---

date: 2005-06-29 03:52:29+00:00
title: Software complexity and design
---

Here's some interesting reading on software engineering:



<blockquote>The general consensus is that when real engineers get through with a design, no matter how complex, they are pretty sure it will work. They are also pretty sure it can be built using accepted construction techniques. In order for this to happen, hardware engineers spend a considerable amount of time validating and refining their designs. Consider a bridge design, for example. Before such a design is actually built the engineers do structural analysis; they build computer models and run simulations; they build scale models and test them in wind tunnels or other ways. In short, the designers do everything they could think of to make sure the design is a good design before it is built. The design of new airliner is even worse; for those, full scale prototypes must be built and test flown to validate the design predictions.</blockquote>



This is from Jack W. Reeves, "[What is Software Design?](http://www.developerdotstar.com/mag/articles/reeves_design.html)".  Reeves's point is that software code is the design.  I find it interesting that although this was written in 1992, the above paragraph clearly presages test-driven development.  How often is software tested to the same standard as bridges?  Rarely.  This arises, he writes, because the 'build' cycle of software is free, particularly compared with aviation engineering.

One of the problems any requirements methodology, such as [RSR](http://www.neilernst.net/blog/archives/2005/rsr-implementing-really-simple-requirements/), faces in getting adopted is overcoming this frequent build mentality.  It's much easier in SE to do incremental development than in other engineering disciplines; as a result, people are less inclined to invest in up-front analysis.
