---

date: 2007-08-17 13:47:37+00:00
title: 'As-is and to-be: an argument against ''kitchen-sink'' modeling'
tags:
- istar
- models
- requirements
---

Like the [is-ought problem](http://en.wikipedia.org/wiki/Is-ought_problem) expressed by David Hume, we should be careful in making models not to merge tenses and verbs. One major purpose of modeling is to create a clear and accurate picture for decision-making. But in some models this clarity is obscured by including information on not just what the current state of the world is (indicative, is), but also what would be desirable (ought, optative - see Jackson in "[Software Requirements and Specifications](http://www.amazon.com/Software-Requirements-Specifications-ACM-Press/dp/0201877120)", p. 125).

[i* models](http://www.cs.toronto.edu/km/istar/) are used for capturing agent-oriented intentional properties in a domain. One purpose of i* modeling is to enumerate alternatives and design opportunities. But the purpose is also to cast new light on the _existing_ state of affairs -- who depends on whom, etc. When these two states are combined, it becomes difficult to evaluate a design alternative: are we assuming Situation A will still hold; how can we be sure the Environment will still be the same; when is the shift in mood going to happen. For example, if I'm considering whether to introduce a technical wiki for storing common solutions in a business, does my i* model reflect the existing situation (no wiki) or the desired situation (wiki).  How can I distinguish between the two versions? Often we want to [evaluate](http://www.cs.utoronto.ca/~jenhork/MScThesis/Thesis.pdf) models to see how well certain decisions achieve strategic goals. How can we do this in a repeatable way if the same model is used for both current and desired conditions?

Another confusion is between _structures _of the domain and _actions _in the domain. We often say that a certain task satisfies a particular goal; but we really want to enumerate, initially, these structural properties of the domain -- what exists **now** -- and allow the designer to choose the implementation path. The tasks that are possible depend on the objects in the domain and certain basic constraints (time/space, physical laws, etc.). If we try to describe tasks that are necessary, or that exist already, we fall into a trap of descriptive analysis, where what already _is_ confines our new design. [Cognitive Work Analysis](http://www.me.toronto.edu/labs/cel/research/frameworks/cwa.htm), for one, insists that structural properties in the domain be enumerated first, followed by tasks and strategies for accomplishing those tasks.

We should have 2 i* models: one enumerating the indicative, structural constraints the work domain imposes; the other providing rationale and alternatives for optative desiderata in the Machine-to-be.
