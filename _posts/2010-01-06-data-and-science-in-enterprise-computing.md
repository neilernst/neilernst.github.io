---

date: 2010-01-06 16:21:10+00:00
title: Data and science in enterprise computing
tags:
- IT
- science
- software crisis
- vincenti
---

Tim Bray had a [great post recently](http://www.tbray.org/ongoing/When/201x/2010/01/02/Doing-It-Wrong) on the 'software crisis'. That wasn't his phrase but it is his subject.

I challenged his conclusions on the basis of poor information. [I said](http://twitter.com/alex77/status/7415451476):


<blockquote>@lemire too bad @timbray's post is completely lacking in empirical data (consultants  don't count).</blockquote>


To which Tim replied:


<blockquote>@alex77 Follow some of the links from my piece. Tons of data. Also, get any COO drunk & you'll hear.</blockquote>


And I finished with:


<blockquote>@timbray anecdote is not the same as peer-reviewed data, sadly. Software field is light-years from even being able to have a "ClimateGate"</blockquote>


So what did I mean? And what did he mean?


### Hacker science


There are a lot of Tims in the industry (and this is a good thing!). For example, his [Wide Finder project](http://www.tbray.org/ongoing/When/200x/2008/05/01/Wide-Finder-2) is a classic example of 'tinkering' leading to innovation. I think the best way to characterize his work is _engineering science_. He starts with an itch, and tries to figure out the best way to scratch it. Along the way, we get new understanding of the problems (e.g., how can non-experts use Clojure effectively) and some data on what works and what doesn't (in the 'real world'). This is very similar to the development of the airfoil, and this stream of science is well described by Vincenti in ["What Engineers Know and How They Know It"](http://www.amazon.ca/What-Engineers-Know-How-They/dp/0801845882).

But this isn't enough. Vincenti makes clear that further airfoil improvements come from a good understanding of the physics underlying lift and computer modeling, not iterative tinkering (although there are clear parallels). Similarly, while the Wide Finder project is a great way to start understanding the theories and constructs involved in concurrent programming in large-scale problems, I'm not convinced this is sufficient. What we would need is studies of many programmers working on many different problems. For example, how would the C solution work with non-expert C programmers? Do the concepts of Agents in Erlang make intuitive sense to most people?


### Standard of evidence


These questions cannot be answered by individual tinkering. They require larger scale studies and more thorough investigation. But unfortunately, there is a trend in the software blogosphere to use one or two data points as solid evidence that "C sucks" or "Perl is unreadable".

But why would we accept this standard of evidence for programming, but not for, say,  climate change? In the same way, can we really base conclusions about the state of IT on the musings of some influential bloggers, industry whitepapers, and [self-serving consultant reports](http://catenary.wordpress.com/2008/09/24/standish-the-chaos-report-and-science/)? Let's imagine the same situation prevailed in climate science. Then we would have a few people commenting on the basis of anecdotal encounters ("boy, it sure is cold in Toronto this winter!"), Shell Oil writing reports on the oilsands ("only 100 hectares are polluted!") and a climate mitigation consultant encouraging mitigation strategies. In none of these cases do you have enough information for rational action (not that this is always the goal!).

Maybe you would say these are apples and oranges, that climate science is a much bigger issue, etc. etc. I'm not sure. In both cases we are talking about billions of dollars of costs. The only real difference is that policy action will be taken by collective action (climate change) or corporate action (IT).


### Improve the Data


So am I saying that Tim Bray is wrong, that corporate IT is fine, that the lessons of Twitter don't apply? Not really. What I am saying is that you should base these sorts of conclusions on empirical data that is collected in the best traditions of open science. It would be data that is from a survey whose questions we can see. It would be data from peer-reviewed research journals.

Let's stop making conclusions using data from Gartner, Standish, et al. These firms are in the business of selling advice, and they are not interested in objective truth. A lot of the reports are based on closed source surveys, talks with "Thought Leaders", random observations, etc. If you are Standish, are you really interested in a report that says "Most IT projects successful"?

What is needed is a non-partisan study, much like the [IPCC](http://www.ipcc.ch/), that will examine the relevant scientific research on the issue. Before we can draw conclusions, especially black and white conclusions, we need to know what we don't know ("unknown unknowns"!). This means raw data, and this means more openness on how well these IT projects are really doing. It would mean allowing researchers access to IT development teams, to perform [proper case studies](http://en.wikipedia.org/wiki/Case_study), to see, for example, why the [FBI system failed](http://www.washingtonpost.com/wp-dyn/content/article/2006/08/17/AR2006081701485.html). Too often software researchers are in the position of begging companies to release data. And even in industries where publicly accessible studies are mandated, we find [many games being played](http://www.badscience.net/2009/12/by-me-in-the-bmj-the-dodginess-of-drug-company-trials/) to prevent negative outcomes being published.

So will there be improvements in empirical data on software? I have my doubts. But it's necessary if we really want to know what software can do, and what software cannot do.
