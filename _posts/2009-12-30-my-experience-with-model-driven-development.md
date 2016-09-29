---

date: 2009-12-30 19:08:32+00:00
layout: post
title: My experience with model-driven development
tags:
- eclipse
- gmf
- mda
- MDD
- openome
- osgi
---

The model-driven development paradigm seems to be undergoing an enormous increase in attention lately, with domain-specific languages (DSLs) and language workbenches seeing the most interest. Do these techniques merit the attention?

One problem in science is getting communities to question their base assumptions. I'm talking about the introductory remarks in a paper, things like "since software development is so hard, it is agreed that a model-driven approach (MDA) is needed". These remarks go unnoticed in reviews because the reviewers must agree with that remark, otherwise why participate in the community? And the people who disagree aren't reviewing these papers to question the assumptions. I'm not picking on MDA, it happens in every community - e.g. mining software repositories.

I'll just add a contradictory data point to the hype surrounding MDA and DSLs. My chief complaint is that an MDA solution, at least [the one I tried](http://www.eclipse.org/modeling/gmf/), shifts the burden of [accidental complexity](http://en.wikipedia.org/wiki/Accidental_complexity) to a new toolchain, but does little or nothing to address the essential complexity. It does seem axiomatic in software research that what we ought to focus on is the essential complexity.

Our experience was with developing a custom user interface for an open-source modeling tool we use as a base for our research - [OpenOME](https://se.cs.toronto.edu/trac/ome). Originally OpenOME code was completely customized, initially using Java and low-level libraries like Swing. Later, we determined that the four/five year old code base was too cluttered to support new improvements, so, in fine software developer fashion, we determined to [rewrite the entire thing](http://en.wikipedia.org/wiki/Not_Invented_Here).

We wanted to leverage the Eclipse ecosystem, so we committed to the Eclipse platform and tooling. By itself, though, Eclipse is just a plugin architecture, so we had a good deal of flexibility in development choices. Had we wanted, we could have written a tool based solely on the plugin extensions and registries, using something like SWT to customize the entire GUI, develop our own data store, etc. This is the approach similar tools like [TAOM4E](http://sra.itc.it/tools/taom4e/) and [jUCMNav](http://jucmnav.softwareengineering.ca/ucm/bin/view/ProjetSEG/WebHome) took.  Instead we used the GMF model solution. GMF asks you to create a domain model in EMF and then a graphical (UI) model to manipulate these domain elements. This is intuitively appealing, and indeed, in just a few minutes you can get a pretty slick UI working, complete with layout, export, zooming, etc. Writing this from scratch would take a lot longer, I think it is safe to say.

The problem is that if you have a UI that is not similar to the one GMF comes with (e.g., manipulating simple boxes and arrows), you suddenly find yourself in the perilous situation of one foot in the canoe and one on the dock. You must make customizations (e.g., adding arrows between elements *within* other elements) deep inside the generated code, and signal this with compiler directives. There isn't (or wasn't, anyway) a good way to show only the customized code, requiring you to wade through thousands of lines of boilerplate to find the line you need to change. And finally, you must adopt the GMF architecture whole-sale, and all its cognitive mismatches.

I suspect the non-GMF solution is much more amenable to extension and customization. In hindsight, although initially I was keen on the MDA approach, I think MDA is best suited to developing domain elements -- e.g., generating data objects with getters and setters. The complexity of [i* syntax ](http://www.cs.toronto.edu/km/istar/)is just to great to be accommodated.

Nowadays, my preferred approach is to leverage component-based software engineering. In this paradigm, which admittedly might also be amenable to model-driven code generation, the developer is just weaving components (libraries, services, what have you) together. Python is a great example of doing this. You leverage someone else's GUI code by providing an output format it understands, someone's data storage engine, someone's logic for calculating graph traversals, etc. I think GMF would have been much more useful if it was (architecturally) closer to OSGI than a true MDA approach.
