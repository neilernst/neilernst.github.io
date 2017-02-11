---

date: 2015-01-15 20:17:07+00:00
title: The Gap Between User Requirements and Software Capabilities as Technical Debt
---

One of my favorite graphics is from [Al Davis](http://www.reqbib.com/adavis/), in 1988. Aside: it is depressing how often we re-invent the wheel in this business.

![Al Davis requirements growth](https://fink08.files.wordpress.com/2015/01/davis88.png?w=660)

The nice thing is how one can map various software development concepts to parts of the diagram. I actually think there is another thing you can grab there. Well, two things. One, the environment is not captured in this picture, but only user needs and the specification. In most cases (maybe this is what wasn't clear in 1988) the user requirements are constrained by the environment, that is itself changing. This is part of our re-definition of the [requirements problem](http://neilernst.net/2008/09/22/the-requirements-problem-defined/) of Zave and Jackson.

Two, I think you can use this to show how the rate of growth in the gap between needs and system (what Davis calls "inappropriateness", the shaded area) is also an issue. I think this captures the technical debt problem more succinctly. You will see a growth if, for example, you chose a technology solution that constrains your use of web browser (eg. Activex controls mandating IE8). That forces your red line (development/specification/software) to grow slower. Now the question becomes, at what point do you refactor/reengineer so that the rate of adaptability (the slope) increases again?

(I don't actually know where I got this -- maybe [Steve Easterbrook](http://www.cs.toronto.edu/~sme/CSC2106S/), he likes Comic Sans a LOT -- or the original source for this but maybe [here](http://www.sciencedirect.com/science/article/pii/0164121288900131).)
