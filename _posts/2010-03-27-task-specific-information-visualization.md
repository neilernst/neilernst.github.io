---

date: 2010-03-27 19:06:38+00:00
layout: post
title: Task-specific information visualization
tags:
- analytics
- cognitive support
- infoviz
---

I [previously](http://neilernst.net/2010/02/12/some-thoughts-on-information-visualization/) [mentioned](http://neilernst.net/2006/10/24/when-the-visual-information-seeking-mantra-fails/) my doubts about general purpose information visualization techniques. Too often these seem to make a pretty picture for a [conference](http://vis.computer.org/), where the focus is the novelty of the visualization -- e.g., a new way to display a [fisheye view](http://portal.acm.org/citation.cfm?id=22342) -- rather than a sober focus on how that picture aids understanding. It is the [cognitive support](http://dx.doi.org/10.1007/3-540-36235-5_10) an infoviz offers that is its _raison d'etre_. It should show you something about the data you didn't know before, some hidden pattern. But too often revealing that pattern requires knowing about it, a paradox. How do we reveal without knowing what we are looking for?

There's a newish sub-discipline in computing called visual analytics.  From a [key resource](http://nvac.pnl.gov/agenda.stm):


<blockquote>Technologies are needed that will support the application of human judgment to make the best possible use of this information... [we need to] define a long-term research and development (R&D) agenda for visual analytics to address the most pressing needs in R&D to facilitate advanced analytical insight.</blockquote>


But why presuppose visual analysis is the most important/cutting edge  thing to do? I speak with the experience of three years working with a [ visual tool for ontology understanding](http://webhome.cs.uvic.ca/~chisel/projects/jambalaya/jambalaya.html) (analysis, if you will). My  experience was that the visual aspect of the tool got in the way of  answering the questions. Now, granted, the tool may not have been  professionally designed, it had bugs, it used Swing, etc. But I  haven't been convinced by the later pretty pictures from other tools. What we are about is answering questions. I worry that when we  come at this from a visualization perspective, we are essentially  carrying a giant hammer around looking for nails.

I think the first thing to do is start with good, old-fashioned user  centered design. Ask them what they want. Then brainstorm some  solutions. Come up with some new interfaces. Iterate, allowing their  reactions to the prototype to inform any new questions they might have. Don Norman [casts some doubt](http://jnd.org/dn.mss/technology_first_needs_last.html) on the capacity for this process to produce innovative design, but I think that's fine in this context: we are answering existing questions. I agree that UCD can be held back by what Vicente calls the [task-artifact cycle](http://books.google.ca/books?id=n7lgV8PnW8oC&lpg=PA103&ots=27__YMfgy7&dq=vicente%20task-artifact&pg=PA103#v=onepage&q=vicente%20task-artifact&f=false). Nonetheless, it is more important to identify what to look for (particularly given the high failure rate of innovative designs).

The problem is that to be effective, a cognitive aid has  to be able to get out of the way. It should be completely unobtrusive.  This is, for me, what Apple is so good at doing. You start off  complaining about their design choices, but almost always it turns out  to be really effective.

Here's an example I was given once. Every police radio car has a  laptop  now, and it is here the officer punches in your licence and   registration when he or she stops you. It queries the database and   returns any information it might have on you -- outstanding warrants,   prior arrests, who knows. Well, a friend of mine told me that this   screen is nearly always filled with useless information. Most of the   time it is either empty, as you are not "known to police", or it comes   back with reams of data. If he stops someone he knows is a 'bad guy', it   will report arrests back many many years. But that isn't what he wants   to know. He wants to know a) can I arrest him for anything outstanding   b) what exactly has he been up to (recently). And right now that's all   they can find out. But I can think of many other questions: who has he   been arrested with? Has he got any recent weapons offences? When was  he  stopped before but not arrested? And so on.

The challenge then is to



	
  1. answer the standard questions officers ask of the machine now;

	
  2. **then** look for other questions they didn't know they had.


It would really  surprise me if a well-tailored SQL report wasn't sufficient  at this point. To paraphrase a famous quote, if the answer to your  analysis question is "use my infovis tool" now you have two problems.  You still need to answer the original question, but also to learn this  tool.
