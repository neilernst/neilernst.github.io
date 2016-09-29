---

date: 2010-02-12 15:25:56+00:00
layout: post
title: Some thoughts on information visualization
tags:
- infoviz
- shneiderman
---

First, must-read 'contrarian' posts on infoviz, in my semi-expert opinion:

"[Big Fat Graphs](http://eprints.ecs.soton.ac.uk/12911/1/the_pathetic_fallacy_of_rdf-33.html)" by mc schraefel and David Karger (why graphs are not the best way to visualize relational data).

[Information visualization and art](http://www.perceptualedge.com/articles/visual_business_intelligence/information_visualization_and_art.pdf) (PDF) by Stephen Few (how pretty pictures are not information visualization).

One popular way of understanding what information visualizations ought to support is [Ben Shneiderman](http://www.cs.umd.edu/~ben/)'s information-seeking mantra: "Overview first, then zoom-and-filter, then details on demand". This axiom proposes a fairly rigid set of tasks that a visualization must support. More generally, his mantra is applicable to visual interfaces that aim to be all things to all people.

However, my [Masters thesis](http://neilernst.net/pubs-2/#theses) showed that this set of actions isn't particularly useful unless you are new to a dataset. For example, ontology editors want to see their area of the model, not the overview. It's like being a worker on the Toyota assembly line and starting each day walking through everyone else's work station before getting to yours. There is some use, of course, to seeing what else is happening, but in general, the overview is hard to visualize and not particularly relevant to them. They need "task-specific visualization" as defined in [Lloyd Treinish](http://www.computer.org/portal/web/csdl/doi/10.1109/38.788803)'s work.

The obvious downside to task-specific visualization is that you need to know _a priori_ what tasks users will be interested in. The traditional way has been to support some form of query and history mechanism, like bookmarks or signposts to indicate relevant views. And the downside to this has been the inability of most users to formulate these queries in the language of the system. SQL, for example, was intended as a natural way to query data, and yet the complexity -- essential mathematical complexity -- of relation algebra prevents all but the simplest queries.

So how should we best support task-specific information visualization? And is infoviz even useful for end users, or is it condemned to be a pretty marketing picture?
