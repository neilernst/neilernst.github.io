---

date: 2005-02-01 22:38:45+00:00
layout: post
title: Notes from GADG meeting
---

This week we looked at [transforming goal models](http://www.cs.toronto.edu/gadg/#g2a) into architectures.  A number of interesting issues arise:  

	
  * most interesting for me, at what point does the operator markup one adds to a goal modeling language become overwhelming?

	
  * if you have too many soft goals to satisfy, the problem could generate into a Constraint Satisfaction task - which is challenging

	
  * to accurately reflect the user's preferences, some sort of feedback loop is helpful, which might  allow adaptive interface generation - like [Horvitz is ](http://www.research.microsoft.com/adapt/)doing at Microsoft.

	
  * I theorized that perhaps my IJHCS paper could be used to generate a goal model (using [OpenOME](http://www.cs.toronto.edu/~yijun/OpenOME.html/OpenOME.html)) that would perhaps serve as a case study for generating architectures for advanced visual interfaces in the KE area.

	
  * the key insight in the Goals, Skills, Preferences framework is to decouple the soft goals from each other (remove dependencies eg. between performance and usability) and show their connections to hard goals, e.g. windowing toolkits

	
  * one must be careful when decomposing goal models to architectures (is decomposing the right verb?) that one doesn't get too much of an implementation bias from the process (or at least, that it happens at the right point).

	
  * where do aspects fit into this process?  and for that matter, what about agile methods?




We also discussed web services as a potential topic for next week, and mentioned the fact Sheila's group is working on similar stuff.  Frustrating trying to get interoperations happening!
