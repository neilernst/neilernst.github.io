---

date: 2016-04-22 16:00:45+00:00
layout: post
title: On SCAM's new "Engineering Track"
---

This year SCAM, the [Working Conference on Source Code Analysis and Manipulation](http://www.ieee-scam.org/2016/) (located in Raleigh, NC, Oct 2–3 2016) includes an engineering track, [as described here](http://davidshepherd.weebly.com/blog/scam-16-in-the-land-of-bbq-beer-bluegrass). The CFP is [available here](http://www.ieee-scam.org/2016/). This track will be co-chaired by myself and [Jurgen Vinju](http://homepages.cwi.nl/~jurgenv/). In this post I want to briefly explain what an engineering track is and why you should submit to it! [^1]

### Purpose

Software is an engineering discipline, for most definitions of ‘engineering’. My definition, for what it’s worth, includes the notion that it involves working on real systems that do things, and to that end research in software engineering can be seen as a design science, where the chief task is to “design and investigate artifacts in context”.[^2] This implies that for the most part researchers in this space need to concern themselves with pragmatics: how will this work at scale? How do people do this now? What data can we use that has practical relevance?

However, traditional conference submissions (the dominant form of scholarly dissemination in Computer Science) tend to follow the 10page, aim/motivation/observations/conclusions framework, often full of Greek letters and references to obscure papers. Whether this is a good way to advance the engineering discipline is debatable, but in any event, such a submission tends to ignore two things: one, how people dealing with problems in practice can use the work; two, the artefacts related to the scientific endeavor (the ‘treatment’ in Wieringa’s design science parlance). While improving, too many research papers still do not include tool downloads, fail to show practical impact, or fail to provide for data download to replicate the findings.

Our engineering track is out to improve the practical, engineering-relevant side of source code analysis and manipulation.

### Submission types
This track has evolved from the tool track of previous SCAMs. As David mentions,

<blockquote>This is not to discourage tool paper submissions–they will now fall into the Engineering Track–but to broaden the scope of the tools track … for those of you that invest blood, sweat, and tears into tooling, infrastructure, or realistic field studies SCAM recognizes the value of this work, which is not always pure research, and we are designing this track to attract that type of work.</blockquote>

What artefacts qualify as “engineering track” material (from CFP)?

  * **tools**: software (or hardware!) programs that facilitate SCAMmy activities.
  * **libraries**: reusable API-enabled frameworks for the above.

    
  * **infrastructure**: while libraries are purely software, infrastructure can include projects that provide/facilitate access to data and analysis.

    
  * **data**: reusable datasets for other researchers to replicated and innovate with.

    
  * **real world studies** enabled by these advances. Here the focus is on how the {tool,infrastructure, etc} enabled the study, and not so much the study itself. Novelty of the research question is less important than the engineering challenges faced in the study.

Some of the criteria the PC will look at includes:

  * How well motivated are the use cases (and hence the existence) of the engineering work. Here we are asking whether this solves some realistic and ongoing challenge in practice. However, we are open to brilliant new ideas that scratch a previously unknown itch[^3].
  * Relate the engineering project to earlier work. All engineering is a product of lessons learned, so including some narrative about how this particular submission has evolved is useful (e.g., what paths turned out to be dead ends).

Optionally (and encouraged):

  * Any empirical results or user feedback is welcome.
  * Contain the URL of a website where the tool/library/data etcetera can be downloaded, together with example data and installation guidelines, preferably but not necessarily open source
  * Contain the URL to a video demonstrating the usage of the contribution.

Ideally one would submit and make public the artifacts and required steps to create it. However, realistically people may not be able to (given IP rules, NDAs, etc.).

### Program Committee
Building on SCAM general chair David Shepherd’s [excellent blog post](http://davidshepherd.weebly.com/blog/how-to-double-the-submissions-to-your-industry-track) on industry tracks, both Jurgen and I are committed to a program committee (PC) that has strong industry representation. That doesn’t mean only people who work in industry, but at least means people who have some sense of the engineering challenges of building real-world software. The purpose is to vet submissions against the standards industry holds: not necessarily will work right away at scale in mission critical systems, but that there is some promise of that.

Incidentally, if you are a former academic now practicing, or just a research-minded practitioner, I would love to [hear from you](mailto:neil@neilernst.net) for future PCs. We need more folks straddling the two cultures.

### “Related Work”
We are not the only place thinking of how to expand and include more non-traditional research papers. At MSR [Working Conference on Mining Software Repositories](http://2016.msrconf.org/#/home) there is a data track, a tools track, and a mining challenge.

One of my favorite venues, the [International Conference on Requirements Engineering](http://re16.org), has long had what I have found to be the strongest industry focus of any software conference. In part I think this is because RE is implicitly concerned with what business needs, but it also reflects a purposeful ambition to increase relevance of the research results. For example, there is a “Ready-Set-Transfer!” panel in which academics present tools to practitioners to review practical readiness.

Practitioner conferences are (almost by definition) industry focused[^4] and both the Agile series of conferences and the XP conference include mirror-world ‘research’ tracks.

* * *
[^1]: Incidentally, I agree with and support the ICSME co-chairs’ [statement on the anti-LGBT](http://icsme2016.github.io/response.html) legislation in North Carolina. 
[^2]: That definition is from Roel Wieringa’s excellent [design science book](http://dx.doi.org/10.1007/978-3-662-43839-8). 
[^3]: can itches be unknown? I may be mixing metaphors.
[^4]: Incidentally, I am not a big fan of the term “industry” or “industrial”. Maybe it is my location in Pittsburgh, but it conjures up steel mills and heavy machinery. The other problem is the term “industry” is used as a catch-all for a widely different set of folks, from a 2 person startup to a Fortune 500 company or DOD agency. I prefer research vs practice. Not a huge fan of “real-world” either, since we all live in the real world. Presumably.



