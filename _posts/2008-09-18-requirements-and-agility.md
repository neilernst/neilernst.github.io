---

date: 2008-09-18 00:46:24+00:00
title: Requirements and agility
tags:
- agile
- fowler
- vicente
---

In [ObservedRequirement](http://martinfowler.com/bliki/ObservedRequirement.html), Martin Fowler makes the following comment: "the word 'requirement' is inherently waterfallish" (in relation to a quote about [BRUF](http://www.agilemodeling.com/essays/examiningBRUF.htm)). A lot of these claims are unsupported by rigorous empirical study: either they refer to closed-data, proprietary reports (Standish), or base their experiences on anecdote. Does agile scale to projects that have more than 10 people involved and exist for several years? Could the Air Force be agile? We don't have very good answers to these questions, yet. Nonetheless, the 'agile' movement has a lot of experienced, seasoned developers and consultants behind it, and it would be foolish to assume it was irrelevant because the data wasn't there.

Fowler's solution to adaptive software is to study what people are doing, and update the system accordingly. There are two problems with this. One, it assumes the software you build has people as direct users. Plenty of software is only indirectly used by people; for example, software to connect wireless modems, software to run microwaves. In general, the software Fowler seems to be talking about is one niche in the entire ecology: admittedly a big and sexy one. The second problem is that it falls into the _task-artifact cycle [1], _that is, it will only reveal those problems made manifest by that artifact. Logs will never be able to show what problems people had that were caused by missing features, or those things which they wished they could do.

If we want to build evolving software, this approach would be useful to tell us what bottlenecks there were, what paths people took through our software, and so on. But presumably we would have to build this agility into the tool to begin with: the monitoring framework, the reporting functionality, the self-* systems _autonomous computing_ talks about. In this case, aren't we now doing stable software engineering? It may be cumbersome to elicit all the requirements at once, and likely not even possible, but perhaps what people like Suzanne Robertson are arguing for is to try and get as many as possible early on. If someone tells us to do something, do we not want a sense of the purpose, a teleological explanation? The knowledge to help motivate our efforts, that even if we start by digging holes in an empty field, we may be building the Taj Mahal?

[1] See Vicente, [Cognitive Work Analysis](http://www.bibsonomy.org/bibtex/2074614e71dd5d50057cd7a198bf8d41f/neilernst), p. 103-104. The term is often used positively, in the sense that good iterative design can accommodate the changing requirements involved. However, Vicente makes the case for escaping the tyranny imposed by the initial design: "Prototyping and usability testing could iterate an existing design, but couldn't suggest wholly new directions (Beyer and Holtzblatt).
