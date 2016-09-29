---

date: 2007-08-17 16:53:15+00:00
layout: post
title: 'Requirements Evolution using Views: a review'
tags:
- lormans
- MOOSE
- reading
- requirements-evolution
- RES
---

`@inproceedings{marco_lormans_monitoring_2007,
address = {Amsterdam},
title = {Monitoring Requirements Evolution using Views},
booktitle = {European Conference on Software Maintenance and Reengineering (CSMR'07)},
author = {Marco Lormans},
month = mar,
year = {2007},
pages = {349--352}
}`

This is a paper that is quite closely related to my research, in fact, probably the closest I have yet found. Both Lormans and myself are interested in the topic of requirements management. Requirements management generally refers to keeping track of changing requirements, storing and updating existing requirements, and tracing from requirements to code/tests/implementation. Traceability is by far the most active research domain in requirements management. Traceability seems to have the most to offer practitioners, but I think one thing traceability fails to address is change in requirements themselves. I am working on a theory for why requirements change, and how that change manifests. Traceability is a technique for updating the Machine (software) when a requirement is changed.

My claim is that system maintenance is easier when maintainers can work in the domain language, rather than the Machine language. Consider a system that evolves as follows: a [dialysis](http://en.wikipedia.org/wiki/Dialysis) system needs to handle a new scenario where patients can take the unit home. It will be simpler for a systems analyst to describe the scenario in the domain or problem language (Patient, unit, blood, kidney, home) than the machine's language (Class Patient, Class Monitor, Package org.test, etc.). Of course, object-oriented modeling is intended to remove some of that [cognitive dissonance](http://en.wikipedia.org/wiki/Cognitive_dissonance), but there will always be things the Machine needs to know that don't exist in the domain. Thus, being able to describe one's changes in the language of the domain is very important.

Lohrmans describes his system for doing this, the **R**equirements **E**ngineering **S**ystem (there has to be a more descriptive name!). I found the proposal (it was presented at a doctoral symposium) weighted towards generating traceability links and automatic generation of changes from work products like requirements analyses. Like my work, Lormans's also focuses on post-implementation changes and system maintenance. He emphasizes requirements views for structuring concerns, including views such as coverage or lifecycle. I found the description of the work skimmed over the issue of maintaining various versions of requirements models. It isn't apparent how RES will store requirements models that it generates, or how it can show changes to stakeholders. My opinion is that this problem will require some careful thinking on visualizations for change.

The work on requirements traceability with information retrieval techniques like [Latent Semantic Indexing](http://en.wikipedia.org/wiki/Latent_semantic_indexing) is interesting and valuable, particularly in large products, but given all IR techniques have incomplete recall, I have to wonder whether important non-functional requirements might be omitted. If we structure our requirements in a tree, such as goal models do, the roots of the tree are the more important goals -- the high-level requirements. If one of these is missed, then isn't the entire model very indeterminate? Furthermore, if the IR technique is relying on statistics like co-occurrence, I would imagine it is possible that certain high-level goals could be so _obvious_ to system stakeholders that they are not that frequent in work products like requirements documents. For this reason I'm more fond of semi-automated techniques.

A big plus in Lormans's work is its integration with several multi-year EU research projects. This has provided a lot of empirical data for him to leverage, and is something I need to achieve as well. The [MOOSE project](http://virtual.vtt.fi/moose/publications.htm) is one such project.

[![](http://fink08.files.wordpress.com/2009/12/res.png)](http://fink08.files.wordpress.com/2009/12/res.png)
