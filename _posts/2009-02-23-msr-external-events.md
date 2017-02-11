---

date: 2009-02-23 17:40:52+00:00
title: 'MSR: external events'
tags:
- evolution
- msr
---

_This is part of the [MSR Challenge](http://www.neilernst.net/archives/tag/msr/) series._

Having generated the lion's share of the data I want to mine, I've turned my attention to getting interesting things out. Following a presentation to my research group, I got a few great tips on what they would like to see. One thing that came up was the notion of tying the data points (e.g., 2 mentions of 'usability' in 2004-March) to some external events. The idea is that there is a reason behind an increase in mentions/occurrences of the word/concept, beyond my (naïve) initial idea of "heightened interest" in a quality as the project goes on.

So the question becomes, how to extract external events that might be causing these spikes? We can readily imagine many such events: change in developer team, release cycle, source audits, and even more random things. Clearly, it would be impossible to determine all of these. But like a good historian, we must try to account for all the variability using some model of the system: like a biological organism, my contention is that the software reacts to the external events by modifying its phenotypic characteristics.

My first task is to determine what plausible external sources might be and account for these. After that, I am going to audit the frequency plots by looking at how much of the variability is accounted for by these 'plausible' sources. Anything remaining is an outlier that I will endeavour to explain (for a subset of the data).

The most obvious external forcing is release date. Particularly in Gnome, which has for a while [since when?] followed a coördinated release cycle, these fixed release dates are sure to prompt people to begin questioning software quality.

I tried to extract this information, at first, from subversion tags in the repository itself. Typically a release changeset gets tagged with the release id for future reference. However, the dataset is quite muddy (imports, inconsistencies, etc). I turned to the #gnome irc channel, and was pointed to the gnome-announce mailing list. There, each release is announced, even relatively minor ones. I should probably determine when this policy was not followed, but it seems reasonably safe to say that it is the rule, rather than the exception (and thus acceptable error). I wrote a little bash script to download (yay wget!) the mail archives (10 years worth), unzip them, and turn them into Apple mail folders. Now I can search by subject title for the project ('evolution') I want. I think I may also add these to my corpora (although they might work nicely as a control set).
