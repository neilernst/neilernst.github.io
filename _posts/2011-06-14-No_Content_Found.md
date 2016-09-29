---

date: 2011-06-14 10:11:03+00:00
layout: post
published: false
title: On innovation in software development
---

One of the funny things about being an academic in an 'engineering' discipline [1] is that there is a sense that you are competing with non-academics to innovate in software development.

Some people have criticized academic software research as hopelessly irrelevant and doomed to unimportance. They ask, what has software research done for us?

Let's take that question to mean, what tangible tools and techniques have software researchers come up with that have dramatically improved how we build software. They might point to most of the trends in industry -- Agile, Rails, J2EE, REST, Twitter -- and show how these were all innovated by people in the trade, rather than via an academic publication. First of all, _should_ academia be trying to make these impacts? Take mobl, for example.

This paywall is the single biggest problem for academics concerned with relevance to practice (and not all academics are, for better or worse). It frustrates practioners, it cuts researchers off from feedback, and is gradually widening the gap between the two worlds. Instead, practitioners turn to alternative venues: the XP conference instead of ICSE, cutter IT journal. Gartner. Standish CHAOS reports. ACM paywall.

To be fair, there's also a much higher standard for evidence and novelty in the academic publications. For instance, the Cutter IT Journal is a consultant newsletter for IT practitioners. But [the articles ](http://www.cutter.com/content-and-analysis/journals-and-reports/cutter-it-journal/sample/itj0903b.html)are blog posts, essentially unsourced and amounting to the opinion and experiences of the particular writer. This model is fine, so long as we remember that the [plural of anecdote is not data](http://en.wikipedia.org/wiki/Anecdotal_evidence). Anecdote can be useful, particularly if it is recounted by someone with interesting experiences, as it can be used to assert the existence of some interesting phenomenon. For example, David Anderson applied Kanban to Corbis, and found this dramatically improved service. From that I conclude that something interesting was happening that merits further study, but it is a stretch to conclude that visual displays of workflow, or limiting work in progress, is the solution to software maintenance tasks.

To be even more fair, many academic studies are little more than anecdote either (unfortunately).

Let's look at what the most influential paper was at ICSE 2010. This award is given to a paper from the conference 10 years ago (selection bias in effect!) that the program committee feels had the most impact. What is influential about it for academics? For practitioners?

This year's award went to Audris Mockus, Roy T. Fielding, and James Herbsleb for "[A case study of open source software development: the Apache server](http://portal.acm.org/citation.cfm?doid=337180.337209)". It has garnered 368 citations according to Google Scholar, which is a good number, although not as high as the paper by Axel van Lamsweerde on requirements (491). There is often a power-law distribution for conferences - most papers are cited very rarely, while one or two make a major impact.

The importance of this work for academics is the way it introduced the study of open-source software, and particularly, the mining of software artifacts. For industry, the impact of the paper was the way it showed that Apache (although atypical OSS) was developed as rigorously as comparable industrial projects.

The difference between anecdotal blogs and academic research is rigor. Both start off with a thought -- "it would be better if we limited work-in-progress" or "what if we adopted Toyota's lean manufacturing to software". Academic work should go deeper into the topic. An academic paper, an academic contribution, is not something that can be written in a few days. It should summarize other approaches, delineate the way the result fits into the wider theory of software development, and give some formal underpinning for the result. There is no doubt in my mind that each of the studies David Anderson describes in his Kanban book could be easily published in ICSE, the premier venue for software research. The techniques are novel and they are validated in industrial settings.

1. ... by which I mean a field that focuses on tangible artifacts rather than theories, as you might see in e.g. Astrophysics.
