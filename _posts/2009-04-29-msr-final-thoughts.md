---

date: 2009-04-29 02:56:53+00:00
title: 'MSR: final thoughts'
tags:
- bugzilla
- msr
- software quality
---

## Source and data


Here's [my source code and extrapolated data](http://github.com/neilernst/gnome-quality-mining/tree/master). It's hosted at Github. I have the raw data, but it's in the gigabyte range. [Email me](mailto:nernst@cs.toronto.edu) if you'd like it. Rather than the painful exercise of parsing giga-lines of XML, I'd recommend checking out a project like [Bicho](http://tools.libresoft.es/bicho), which can extract Bugzilla data from numerous repositories (wish it'd been available for me!).


## Where to go from here


I started out with the rough conjecture, based on Lehman's Seventh Law, that as a software project matures (please say that "Maw-Toors", not "match-yoors", kthx) the percentage of time devoted to discussing software quality ought to increase. That is, less time is spent on 'feature A isn't working' and more on 'let's make the GUI more swell'. The data doesn't support this conjecture.

One problem is that the taxonomy I was using to seed my signifiers, ISO9126, is very high level, and covers a range of qualities. For example, it includes the notion of 'correctness', as in, the program will behave as expected. Well, clearly such issues would be a concern from day 1. I didn't find any useful correlation between project age and discussions of software quality. R**2 values were very low, indicating, in my linear model, anyway, that there was no relationship. I also tried with a cyclical model based around release windows, but this also had low correlation.  My final conclusion was this: there is definitely some signal to be extracted from these datasets (mailing lists, bug reports, commit messages). That is, these qualities *are* being discussed by software project participants (I haven't determined _who_ is discussing them yet).

I think this is an interesting result. Certainly, it suggests that software quality discussions are not stagnant, that there is some type of response. The question is, to what? The last experiment I conducted looked at specific peaks in the curves to determine what external events (discovered from mailing lists, source code, etc.) might have caused a spike. Of course, here we tread into the uncertain but possibly richly rewarding area of qualitative research. What I mean is, there is no way to prove, given a particular event, that it _caused_ the spike -- just the chance for a high degree of certainty. But really, that's all an experiment gives anyway.

A colleague, [Jorge Aranda](http://www.cs.toronto.edu/~jaranda), made the comment that experiments in software engineering aren't that useful, giving one a false sense of learning something but making little contribution to an overarching theory. I certainly agree that this can be the case, but I also think one of the best ways of using experiments is via contradiction of established/cherished opinions. For the contextual settings, this experiment, for example, has shown that there isn't a linear relationship between software age and discussions of software quality. It is a useful result because it helps me to refine a theory for how software is evolving over time. It can help me design good case studies, for example (what not to look for; what explains the result).

I guess I don't think experimentation is only useful for limited tests of a richly developed theory (not that Jorge is saying this). It can also be useful in an exploratory sense. The real question for my result is this: does the fact that there was no pattern seen overwhelm the generalizability problems of selecting eight projects from one Linux-based desktop suite? That is, is it possible that these patterns exist in other sets of data? It could always be the case, but I believe not.

[Meir Lehman](http://en.wikipedia.org/wiki/Meir_M._Lehman) believes that software needs to be constantly improved if it isn't to suffer bit-rot and fail to meet user needs. I think a useful extension of this work is to break software into finer-grained components. One might examine the evolution of particular features, such as journaled file systems; particular aspects, like user accounts; particular qualities, like usability; and even more fine-grained details. I suspect that each of these components evolves more or less independently of the others. I plan to do a re-examination of the [Linux study of Mike Godfrey and Qiang Tu](http://www.bibsonomy.org/bibtex/2290390167f71426da0a1de4998f4e57c/neilernst) with that in mind.


## Final thoughts


I think to do research, one has to assume some element of risk at the outset of the project. There has to be a reasonable chance that your efforts will have been wasted, that the data won't show what you expected. I think this is what often bothers me  about papers that propose frameworks, or taxonomies, or methodologies. There's no risk involved in a new framework. How can it go wrong? All I can think of is that the proposer doesn't refer to prior work or is logically inconsistent. And I don't mean _theory_ here; new theories are welcome. It's just I don't think there are many legitimate, explain/predict theories in (software) research (see [Gregor, 2006](http://www.bibsonomy.org/bibtex/268d4e2635a5ab93fdd83f021c799251f/neilernst) for a description I like of the nature of theory in information systems research).

I guess research doesn't need an empirical basis, but I think it helps. Empirical evidence is like an acid test for a hypothesis or theory -- it gives reviewers a way of evaluating the work independent of what the paper claims. Frameworks, on the other hand, are pretty circular, and for me at least, hard to review. Most framework papers use trivial examples as a way of establishing that they 'work', but I reject this. This is argument from experience, and it's pretty meaningless. Really, all I have to do as a reviewer is show one example your framework claims to handle, but cannot, and the paper is bunkum.

At any rate, this project was one of the first in which I wrote a fair bit of code, and took a bit of a risk with my mental model of what the data would show. I highly recommend the process.
