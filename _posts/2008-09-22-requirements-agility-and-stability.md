---

date: 2008-09-22 20:22:17+00:00
layout: post
title: Requirements, agility, and stability
tags:
- agile
- requirements
- services
---

Having returned from the [Requirements Engineering](http://sites.upc.edu/~www-gessi/re08/) conference in Barcelona, I've been pondering where my own research fits with the talks I listened to. One of my concerns, perhaps needless, is the relevance of my research to practice (both current and potential). The RE conference has parallel streams of industrial reports and academic papers, to emphasize the purpose of research, I suppose (although other fields don't seem as concerned as we are with relevance).

Many of the tools I've worked on are fairly heavyweight, and assume a fairly large degree of co-operation from the user regarding his/her commitment to the modeling process. But is such a tool important for most users?

Siemens, for example, presents numerous reports each year at the conference arguing for heavy process around requirements engineering, but since it is the RE department presenting the research, it's hard to tell how much these tools and methodologies are appreciated internally.

Microsoft, apparently, uses documentation extensively in development (security analysis, i18n analysis, performance analysis, etc), but one might argue that this is hardly an endorsement. I'm not familiar with what Google tries, but my sense is that they are much more about the competitive environment for new ideas (and have many fewer challenges with respect to legacy systems support).

Cringely has a good post about organizational support for innovation. In it, he quotes the following: "You wouldn't need "change management" if you made continuous improvements at the functional level the responsibility of every individual and team cluster ([Janna Raye),](http://www.pbs.org/cringely/pulpit/2008/pulpit_20080917_005420.html)" So it would seem that in the industrial context, there is a big difference in how, and what, requirements practices are used.[
](http://www.pbs.org/cringely/pulpit/2008/pulpit_20080917_005420.html)

The questions that one must consider is clearly one of future directions. [Jorge Aranda](http://www.bibsonomy.org/bibtex/2b3756822eb487d407b99ffec63d3e3c7/neilernst)'s paper suggests that for many small and medium-sized companies, at least, the use of requirements models (and associated tooling) will be (is) negligible. The business analysts, who are probably also programmers, generally understand the environment very well, and tweak their product to accommodate new clients, rather than doing revolutionary design.

[Greg Wilson](http://www.cs.utoronto.ca/~gvwilson/) characterizes one dimension of software systems according to how agile or stable they are. An agile system to him is one that tries to duck the punches of unanticipated evolutionary changes; a stable system tries to build itself so solidly that these changes cannot affect it.

Martin Fowler, in turn, characterizes these as [evolving or planned](http://martinfowler.com/articles/designDead.html#id59037) designs. Clearly for planned designs tools and models become more important (though arguably still not necessary). Evolving designs focus more on working code, code as documentation, and testing as the way to verify the match between requirements and implementation.

A colleague of Fowler's at Thoughtworks proposes [Consumer-driven contracts](http://www.infoq.com/articles/consumer-driven-contracts), essentially user stories for web services: "To recognise the specific benefits and outcomes supported by a service, we need to understand that service in its collaborative context." How they help with change management: "consumer-driven contracts help contextualise compatibility issues based on extant obligations and relationships. A change to a mandatory element need not always be considered a breaking change; rather, changes that require some form of versioning can be identified with reference to the consumer contracts they break. If existing consumers aren't using a mandatory message element, then changing or removing that element need no longer be considered a breaking change."

This turns the burden of change management over to the client, requiring him/her to determine his/her needs, and then managing the change in that context. Previously, a new release from, for example, Oracle, required a fairly binary decision from the IT department: thumbs up or thumbs down on the new product update. In the service world, the promise is that such monolithic upgrades will be a thing of the past.

The [requirements problem](http://www.neilernst.net/archives/2008/the-requirements-problem-defined/) doesn't disappear, of course. Indeed, a consumer-driven contract is a form of customer requirement, which should be (largely) satisfied to build a successful project. What is changing is the form these requirements take: rather than large, static, possibly stale models, the requirements might take the form of acceptance tests, behavioural checks, or quality of service policies.

In terms of my research, which focuses on unanticipated changes to a system domain, the relevant questions surround a) understanding how this type of evolution might be best characterized (yes, yet another taxonomy) and b) what type of tool support might help manage these situations. My current thinking is that while change is **always** unanticipated in some form, we should attempt to support processes for deciding how to adapt to that change.
