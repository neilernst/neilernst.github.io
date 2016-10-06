---

date: 2010-04-22 18:42:42+00:00
title: Should we care about evidence-based software engineering?
tags:
- evidence
- software
- theory
---

Time for some contrariness. The current rage in the academic software research community is evidence-based practice. It's in [popular magazines](http://www.computer.org/portal/web/csdl/doi/10.1109/MS.2010.75), [desirable in academic publications](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5452151&tag=1), and the [subject of a new book](http://pyre.third-bit.com/blog/archives/2910.html).




Does it matter? On the face, one would say of course. Why would you make decisions ignorant of the facts?  (set aside for now the reality that almost NO decisions in the world are made based on the facts!)




It would be nice if software researchers were in a position to present facts to people. In climate science, for example, the facts are pretty clear, and certainly much clearer than corresponding literature in software. That's why Al Gore, among others, probably sees [debates on climate change as pointless.](http://www.easterbrook.ca/steve/?p=1431) But the utility of model-driven development, among many others, is very much worth debating. I think there are five reasons why we shouldn't be too concerned about evidence in software development:





	
  1. The field with a long history of evidence-based practice, and the most to gain from it, **medicine**, often _doesn't adopt the recommended practices_, or the evidence chosen is irrelevant. Despite[ hand-washing](http://www.annals.org/content/141/1/I-38.full) or [checklists](http://www.newyorker.com/reporting/2007/12/10/071210fa_fact_gawande) being shown (proven?) to be very cost-effective practices to adopt, doctors still leave washrooms without cleaning their hands, and instruments still get left in patients. And in most software projects, there isn't anything like that sort of liability.

	
  2. People _don't understand statistical generalization_ very well. Is that new pill reducing my risk of heart disease 20% more than the other pill, or 20% more than a regimen of Big Macs? Was this experiment done with non-English speakers? There's a lot more to it than running a few t-tests and calling it a day. See e.g. "[Why most published research findings are false](http://www.plosmedicine.org/article/info:doi/10.1371/journal.pmed.0020124)" or a [series](http://scienceblogs.com/cortex/2008/06/science_criticism_fmri.php) of [critiques](http://www.mutuallyoccluded.com/2008/12/vul_fmri_cognitive_neuroscience_social_interaction/) on fMRI studies.

	
  3. _Small results don't say much_. A lot of research is evaluated on [small numbers of undergrads](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5076454&tag=1) or focused on [one particular organization](http://research.microsoft.com/pubs/74243/p557-cherubini.pdf) (pdf). That evidence is useless to most developers. There is a paucity of in-depth, detailed case studies that generalize to meaningful theories. Personally I am in favour of a moratorium on experimentation in software research until more of these case studies are done. Unfortunately, the lure of the easy number is a Siren-call to reviewers and funding agencies.

	
  4. SEMAT to the contrary, there is no _g_[_ood body of software theory_](http://catenary.wordpress.com/2007/03/12/theory-use-in-software-engineering-research/) that would provide explanatory power to go along with results. Without a theory facts are descriptive; with a theory they can be predictive.

	
  5. It simply _isn't that important_. Individuals and organizations do many things which research suggests is downright insane -- like embarking on projects without clear requirements, or maintaining 30 year old mainframes -- and get by. In fact, anecdotal evidence suggests that many excellent companies[ started with poor practices](http://www.theregister.co.uk/2009/04/01/twitter_on_scala/), then refactored as needed. Probably, this is because evidence-based software development is a [case of premature optimization](http://en.wikipedia.org/wiki/Program_optimization#When_to_optimize). For example, despite reams of studies suggesting model-driven development is the way of the future, industrial adoption is underwhelming. Is it because they haven't read the studies? Or that they evaluated the technology and concluded it wasn't necessary? As academics, we tend to undervalue the benefit of anecdote and gut feelings. Most of the time this is probably correct, but only if we have evidence to support generalization to common scenarios. Most developers were so burned by the [CASE tools](http://en.wikipedia.org/wiki/Computer-aided_software_engineering#History_of_CASE) of the 1980s that they have no interest in repeating the experience with UML.


I think my final point is that rationality is the exception, rather than the rule, in human behaviour. There's no reason to lose any much sleep over the fact that industry isn't following evidence-based software practices.

p.s. I'm a complete hypocrite with respect to experimentation.
