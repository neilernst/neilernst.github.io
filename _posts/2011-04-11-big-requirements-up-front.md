---

date: 2011-04-11 16:01:28+00:00
title: Big Requirements Up Front?
tags:
- agile
- bruf
- large-scale systems
---

Big Requirements Up Front are certainly not in favour with the industry thought leaders in software development. But I think the idea of specifying your requirements ahead of time, as Parnas says in "A Rational Design Process and How To Fake It" is worthwhile.

Consider the case of climate models. Or smaller open-source projects. Here the developers 'scratch their own itch' and the requirements are almost always implicit. What to develop next is driven by an internal process, where the Customer (in the XP sense) is always present by definition, since the developer and the Customer are always the same.

And yet these projects often run into trouble because the requirements are not explicitly modeled, where by 'modeled' I mean somehow written down and discussed, prioritized, etc. _(ed.: Justify this claim!)_. Backwards compatibility with previous instances is not maintained, reliability is awful, effort is duplicated, and so on. I think only in projects that are being done the same as last time - cf. Aranda et al, 2007 -- is there a hope of totally ignoring requirements explicitly.

Why did we start with the BRUF paradigm in the first place? I think it was because like everything in software development, (and computing itself for that matter) things started with the US Defence Department. And their needs are so different than those of a small software development company like 37 Signals that it's a totally different animal. You have multiple competing vendors, huge safety considerations, multi-year and multi-billion dollar developments. It would be foolish not to do some up-front design. That's not to say that iterative, frequent release models can't work in the Army - I think they could. But a little up front planning could save a lot of time designing things you won't need.

Because the army gives so many dollars in grants, the prevailing academic attitudes are concerned with defence sized issues. The problem is that these concerns are not shared by other sectors. And so small "a" agile started as a reaction to this top-down design.

I'm not defending the IEEE requirements template, or the amount of documentation for CMMI certification. But I very much believe that some form of explicit requirements modeling is important for projects. Look at Scrum -- most people are doing user stories with story points. These are requirements models! Simple, but still explicit, prioritized, costed requirements. And people like Scott Ambler argue that to scale Agile, you need a little more - you need ways to organize the stories, to assign responsibility, to manage the stories.

The reality is that when systems get more complex, for most of us it is impossible to keep track of the scope and scale of the system (unless you are Linus Torvalds, perhaps). In that case, to communicate with the rest of the team you will need something to share — and requirements neatly capture what needs doing. I think the word 'requirements' itself has come to mean BRUF requirements, when it properly means the set of new properties of the environment your new machine will bring about [(Jacksonian requirements](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.99.1593&rep=rep1&type=pdf) (pdf)). Under this definition requirements becomes a much broader term.

One of the big problems is that we understand things in this industry using anecdote. And so many horrible anecdotes have come from "big requirements up front" projects. But in those cases, any methodology would likely fail if the organization lacked maturity. And conversely, any mature organization could use any methodology it chose and succeed. Those organizations know how to motivate people to get excellent work and know not to change scope midway, not to alter budgets, and so on. I think these factors are ultimately much more important than the particular development methodology one chooses.
