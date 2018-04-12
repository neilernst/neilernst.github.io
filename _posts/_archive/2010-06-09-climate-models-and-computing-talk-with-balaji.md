---

date: 2010-06-09 14:44:25+00:00
title: Climate models and computing talk with Balaji
tags:
- climate
- computational thinking
- hpc
- physics
---

Yesterday the U. Toronto [Atmospheric Physics group](http://www.atmosp.physics.utoronto.ca/) hosted a talk by [Balaji](http://www.gfdl.noaa.gov/~vb/index.html)1, head of the modeling systems group at the Geophysical Fluid Dynamics Lab (GFDL) at Princeton University, a school in New Jersey. Balaji's interests include High Performance Computing (HPC) and computer modeling. His Ph.D. is in Physics but I get the impression he is 'computationally-oriented'.2 I don't have his slides, but it looks as though he posts talks on his website.

The gist of his talk was that climate modeling, while of critical importance to the world, is facing several challenges:



	
  * Scale: increasing the resolution of the model in X/Y dimensions means a factor of 4 increase in problem size, and often we want to increase the temporal resolution as well (for a factor of 8 increase).

	
  * Climate models need to integrate new science components. For example, we should model hurricane formation by integrating sea-temperature models with atmospheric models. These integrations pose several challenges.

	
  * Models need to be reproducible, according to current scientific dogma, but this is a tough challenge when a model run can take many days to run, and is subject to hundreds if not thousands of parameter choices. There are research efforts underway to understand what 'reproducibility' ought to mean at this scale: is probabilistic reproducibility enough? One challenge is that even understanding the results of the model run can be challenging.

	
  * More and more, products of climate modeling are being sought as input into other models or decision-making. For instance, policy makers need to know drought predictions for the next 50 years in order to do land-use planning. The problem is that a) there are more of these requests than GFDL, for instance can handle; b) the models are not suitable for these predictive tasks, and require expert interpretation; c) selecting a single model is not desirable when the average of all models gives better results. Balaji mentioned a proposal to create a 'climate service', akin to the weather service, for doing this sort of thing.


A few other notes:

Balaji described the [FRE](http://www.gfdl.noaa.gov/fms-fre-usage?_rewrite_sticky=~fms/fre), a configuration management system (of sorts) for recording experimental parameters and workflows. This is how GFDL tries to keep track of model runs, and maintain reproducibility. He did mention that the system can still be tweaked at the instance level, so the FRE may not capture everything that was done for that run.

I asked Balaji why these research centres were so intent on building and maintaining supercomputer clusters. After all, it isn't something they should be experts in. I suggested the real experts were companies like Google and Amazon who routinely operate thousands of processors in data centres around the world.

His response was that they needed the control. The models need control over configuration, for reproducibility (after all, they are interested in bit-level reproducibility); they also needed control over core cycles, so that the models could run uninterrupted. He gave as an example the Department of Energy supercomputer centre, where other needs (more processing intensive) would bump climate models from the queue. Furthermore, he thought it likely that running on Google App Engine, for example, might cost even more than maintaining and running your own cluster.

That answer is understandable, but it does seem solvable. These are essentially business problems that can be negotiated: cost of cpu time, service level guarantees, etc. It's hard to see how GFDL can compete with Google's engineers in maintaining and building massive clusters. As an example, DNA sequencing is[ now taught on Amazon EC2 'machines'](http://ivory.idyll.org/blog/jun-10/ngs-course-with-aws).

Finally, I would think from a reproducibility standpoint that relying on knowledge of specific machine configurations is way too detailed. It shouldn't matter to your model that this machine runs VMS 3 while this other machine ran Linux 2.6.24. I know it *does* currently matter; but it shouldn't.

It was a fascinating talk; he managed to tailor it to the diverse group of people listening in very well. I wonder if Steve Easterbrook will get to visit the GFDL lab as part of his [sabbatical research.](http://www.easterbrook.ca/steve/?p=1701)

BACK 1. I believe this is his last name, but used in the Brazilian fashion, a la Ronaldo/Pele.

BACK 2. I apologize for being sleepy mid-way through!
