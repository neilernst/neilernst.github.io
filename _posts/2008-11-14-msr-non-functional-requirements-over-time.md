---

date: 2008-11-14 16:55:36+00:00
layout: post
title: 'MSR: non-functional requirements over time'
tags:
- iso9126
- msr
- nfr
---

_This is part of the [MSR Challenge](http://www.neilernst.net/archives/tag/msr/) series._

The challenge I'm undertaking is to report on something 'interesting' (and novel) about projects under the Gnome umbrella. Since my thesis is on requirements evolution, I've tried to use the Challenge to help me understand the nature of the evolution problem. I suppose the first issue is to convince one that there is a problem. Are requirements changing over time? What factors are driving that change?

Rather than looking at functional requirements, which can vary tremendously across projects (I have my opinions about this but more later), I've chosen to look instead at software qualities, aka 'ilities' aka NFRs. These are notions such as usability, security, and maintainability. These concepts can be said, tentatively, anyway, to transcend software ecosystems. That is, every piece of software can be judged according to its fulfilment of these 'soft goals'. In particular, I've decided to use the [ISO 9126 standard](http://en.wikipedia.org/wiki/ISO_9126), which lists a brief taxonomy of software qualities. The advantage is that it is relatively well-known, and 'standard', for what that's worth. The problem with using it is that there are as many taxonomies of software qualities as corrupt bankers on Wall Street. Some might argue that even non-functional qualities are not universally applicable.

How am I going to apply this model to the corpus? I'm doing this somewhat iteratively, in that I'm going to start simple and build from there. So for now, my goal is to show how these qualities are discussed over time in a given project. My guiding framework is to model word use (and related terms) as events in the timeline of a project. So if a developer or user mentions 'usability' on a mailing list, that becomes an event in my system. Then I record these events and use a timeline to show how they occur over time. Not a terribly sophisticated NLP technique, but let's see where it gets us before delving into Markov models, naive Bayesian algorithms, and so on.

I have a few hypotheses about the presence of my events, relating to how NFRs are more or less important (as gauged by frequency of mention) at various lifestages of a software system, for numbers of developers, for project focus (media, utility, OS, etc.), and so on.  More on these later.
  *[NLP]: Natural Language Processing
