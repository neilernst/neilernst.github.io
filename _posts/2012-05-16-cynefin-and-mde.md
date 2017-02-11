---

date: 2012-05-16 19:51:45+00:00
title: Cynefin and MDE
---

Watching [Dave Snowden talk about Cynefin](http://www.youtube.com/watch?v=N7oz366X0-8&feature=related) (thanks to [@**dsg22**](https://twitter.com/#!/dsg22) for the reminder), it occurred to me that this sense-making approach might explain some of my discomfort with [model-driven engineering](http://en.wikipedia.org/wiki/Model-driven_engineering) (MDE). I will readily admit to bias: we built a research project, [OpenOME](https://se.cs.toronto.edu/trac/ome),  using model-driven engineering with [GMF](http://www.eclipse.org/modeling/gmp/), and in my opinion, it was completely the wrong approach for the job (keeping in mind that [MDE pays off in subsequent projects](http://modeling-languages.com/mdd-pays-mid-term-industrial-experiment/)).

I think my conceptual problem is that MDE encodes a specific process in a tool. At least one central selling point is that the models can be independent of the context in which they are used. That is, we have this process for desiging graphical editors in Eclipse (with a hard-coded architectural approach), and we have encoded this into the GMF framework.

[caption id="" align="aligncenter" width="200"]![](http://upload.wikimedia.org/wikipedia/commons/4/45/Cynefin_framework_Feb_2011.jpeg) Cynefin framework (via Wikipedia)[/caption]

It isn't that this can never be useful. But if we turn to [Cynefin](http://en.wikipedia.org/wiki/Cynefin), we can see why it might be problematic. I would characterized MDE as working well in "complicated" or "simple" domains, where the appropriate response to a problem is to use best practices or 'good' practices - exactly what MDE is doing. However, much of the work we do in software development is in the complex, if not chaotic domains, where best practices simply don't exist. I would characterize my experience with GMF this way. The tool we built had unclear requirements, and we didn't understand the technological landscape properly. A better approach, if we go by Cynefin, would be to "probe" the problem by building prototypes, and then determine what our response to the experiement would be.

In other words, if you are in a simple or complicated domain, then MDE tools should work great. They will allow you to deploy your app to multiple platforms, greatly reduce re-engineering effort, and much else. But if you don't understand the domian very well, or you are in a chaotic system, you should put the MDE aside. And it's my opinion that most software development occurs in the complex domain.
