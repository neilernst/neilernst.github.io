---

date: 2009-03-19 02:40:45+00:00
layout: post
title: 'MSR: Case study variability'
tags:
- gnome
- msr
---

_This is part of the [MSR Challenge](http://www.neilernst.net/archives/tag/msr/) series._

To keep the scope of my proposed project in check, I've decided to go with a subset of Gnome projects to test my NFR tool on. However, I want to make sure they're a good cross-section of projects so that  I can make some theories about the observations I may make. For example, I should have a mix of project lifespans, and a mix of project sizes (LOC, number of developers, etc.), among other variables. Although the project is restricted to the Gnome forge (a forge being a community of developers, like Sourceforge, MSDN, KDE, etc.), I would ultimately like to take it to other forges to see whether there is a difference there as well.

I selected eight projects, mainly based on my experiences with them, and my first order of selection was software purpose. One of the big absences in the software engineering literature is some taxonomy of software ecologies. I wanted projects that touched on a number of different ecologies, including operating systems, media, utilities, internet, and so on.

In the end, I ended up using mainly the longest-lived projects. They provided the richness needed for a proper longitudinal study. I didn't see much variation between the two (Nautilus and Evolution). The main change was that in Nautilus, software quality was discussed three times as often, relative to event volume, as Evolution. More work is needed to tease out the causes for this result.
