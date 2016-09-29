---

date: 2011-09-30 19:54:01+00:00
layout: post
title: 'Ultra-large-scale systems: fundamentally different?'
tags:
- lscits
- software-engineering
- ulss
---

An emerging trend in software research is a focus on complex software systems. These systems are typically:



	
  * decentralized: a lack of hierarchical control.

	
  * display emergent behaviour: unexpected behaviour arising from unexpected interaction effects.

	
  * subject to network effects: a rich mixture of human and computer agents.

	
  * large-scale: millions of lines of code, thousands of agents.


An example of such a system is the stock market, or the US military's [future soldier program](http://en.wikipedia.org/wiki/BCT_Modernization). Two major initiatives have been developed to focus on these systems: the Software Engineering Institute's [ULSS program](http://www.sei.cmu.edu/uls/index.cfm) and the [Large-Scale Complex IT Systems](http://lscits.cs.bris.ac.uk/index.html) (LSCITS) program in the UK. According to these programs, there is a "Software Problem", and the tools and techniques we use today must be radically improved if they are to manage these new challenges.

But as Peter Norvig illustrates [in this article](http://blogs.scientificamerican.com/at-scientific-american/2011/08/23/systems-analysis-look-back-1966-scientific-american-article/#), we have managed to scale from the half-million instruction programs of the 1970s to the hundred-million instruction programs of today. So why do we expect not to handle the billions of instructions in a ULS system? I'm not suggesting we build software perfectly today. There are many improvements possible. But I'm not sure I agree there is some fundamental challenge we cannot currently address.

One thing I think is important is the ability to fail gracefully. One lesson that seems to have been learned over the years (and the idea surfaces from the start in SE) is that iteration is fundamental. That means building systems such that failure is not fatal. Naturally, in some places that isn't possible ([medical devices perhaps](http://www.theregister.co.uk/2010/07/27/buggy_pacemaker_code/)). But even in these seemingly obvious examples, it should be possible to fail usefully: to alert someone to the problem, supporting remote software updates, or incorporating more adaptation capability.

The point of this post is to ask whether the statement: "[Our ability to develop, maintain and manage such systems is falling behind the growth in their complexity](http://lscits.cs.bris.ac.uk/overview.html#rational)." has any evidence behind it. Standish reports need not apply.
