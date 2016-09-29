---

date: 2014-07-24 13:55:10+00:00
layout: post
title: Cults of Personality and Software Process Improvement
---

I'm a fan of the [Cynefin framework](http://cognitive-edge.com/library/more/video/introduction-to-the-cynefin-framework/). I find it a great tool for understanding what type of problem you are trying to solve. The notion of complex/complicated/simple is quite helpful. You could do worse then to read [Dave Snowden's blog](http://cognitive-edge.com/blog/author/19/), as he explores each of the domains in the context (most often) of software projects.

Recently Mr Snowden [has been critiquing](http://cognitive-edge.com/blog/entry/6300/initial-thinking-on-scaling/) the [Scaled Agile Framework](http://scaledagileframework.com) (SAFe) put together by Dean Leffingwell. This attack on SAFe is not [unprecedented](http://kenschwaber.wordpress.com/2013/08/06/unsafe-at-any-speed/). It's hard to take attacks like this too seriously when their proponents don't put forth data, but merely theory.

One of the most difficult parts of doing research in Software Engineering is its inherently uncontrollable, one-off nature. Sure, in some cases---like websites for restaurants, for example---we see repeatability. But the most interesting projects, the ones SAFe is applied to, the complex or perhaps complicated ones, there is no repeatability (by definition). This makes it impossible to say with any degree of accuracy what factors are contributing to the success or failure of the project. 1

In particular, when you have strong, intelligent, experienced consultants like Mr Snowden, or Mr Leffingwell, or various other graybeards, I don't think you can control for the 'personality' factor. That is, what portion of the success of the initiative (say, applying [Sensemaker](http://www.sensemaker-suite.com/smsite/index.gsp) or SAFe or Scrumban or what have you) is due to the tool/process improvement/methodology, and what portion is due to the smart person effect of the consultant? This is made more difficult when that consultant has a very strong economic incentive to point to the methodology as the distinction, since their business is inextricably tied together with that methodology. Furthermore, just the fact that a company has reached out for help indicates some level of self-awareness.

My feeling is that given a successful team, led by an enlightened manager, it wouldn't matter what methodology they used (which [I mentioned previously](http://neilernst.net/2014/06/13/software-research-shouldnt-be-about-the-tools/) in the context of tools). And there is some evidence to support this: [Capers Jones suggests](http://www.infoq.com/articles/Jones-measuring-agile-adoption) RUP and TSP have higher quality than Scrum or other approaches. Now that is just one dataset, but it is exactly one more than Mr Snowden has produced, as far as I can tell (the plural of anecdote is not data).

Does all this mean it doesn't matter if we choose RUP, SAFe, Scrum, Kanban, Six Sigma, or Sensemaker? To some extent, I think that is true. I would guess that your measurable outcomes after implementing TSP would be similar to the outcomes after implementing SAFe. But the point is, one cannot measure these things in isolation! You will never know (Heisenberg-like) whether something else would have been better. The local project context is so important that the principles are more important than the specific practices (e.g., the agile manifesto, Cynefin domains, good organizational practices, etc).






* * *







  1. 
With one exception I am aware of: [this paper](https://www.simula.no/research/se/projects/moose/StudyData/reproducibility) from Simula in Norway. They paid 4 different companies to develop to the same set of requirements in order to understand the maintainability characteristics of different approaches. But even there, the results are difficult to generalize. Anda, B.C.D.; Sjoberg, D.; Mockus, A, "Variability and Reproducibility in Software Engineering: A Study of Four Companies that Developed the Same System," IEEE Transactions on Software Engineering, vol.35, no.3, pp.407,429, May-June 2009 doi: 10.1109/TSE.2008.89 ↩





