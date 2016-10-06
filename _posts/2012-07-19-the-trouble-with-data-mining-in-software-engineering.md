---

date: 2012-07-19 17:38:17+00:00
title: 'The Trouble with Data Mining in Software Engineering  '
tags:
- data mining
- machine learning
- requirements
---

A lot of work has gone into applying statistical tools to software engineering artifacts, like code, tests, and social networks. The premiere venue for this is the International Working Conference on [Mining Software Repositories (MSR)](http://2012.msrconf.org/history.php).

As an example, myself and other researchers have been trying to automatically extract requirements from project artifacts, including emails, issue trackers, and code commit messages. You can read more about my work [here](http://www.springerlink.com/content/237368m41615742m), and it was recently extended [by Abram Hindle here](http://softwareprocess.es/static/RelatingRequirements.html). Another interesting tack was taken by [Radu Vlas at Georgia State University](http://www3.cis.gsu.edu/rvlas/index-3.html), using ontologies and part of speech tagging.

The trouble is all of the techniques we’ve used to date only give us a precision/recall of at best 60/60 [[1]](1), meaning we miss 40% of the actual requirements and only 60% of the results are in fact requirements. This isn’t very satisfactory, because it means you miss out on possibly important requirements, and still have to wade through a lot of noise. We’d like to get this to 100/100, of course, but anything would be an improvement. The benefits would be immense: requirements traceability would be simplified, allowing us to talk about whether a requirement was implemented, what requirements interact, describe the current requirements a project satisfies, and many others.

Unfortunately, I wonder if we haven’t hit on the fundamental limit to the natural language parsing/machine learning toolkits (in this domain). I say this because the most obvious successes of machine learning, such as [spell-checking](http://lifehacker.com/5895252/googles-new-spell-check-is-crazy-awesome) or [flu tracking](http://www.google.org/flutrends/ca/#CA), are due at least as much to the vast amount of data involved as to the novelty of the techniques themselves. The problem is that in software projects, the amount of information is measured in the _tens of thousands_ of data points, when it really should be _millions_ or _tens of millions_ to be really successful.

For example, one of the longest-lived open projects, Mozilla, only has about 800,000 issues in its issue-tracker. Which is not bad, but we need to remove duplicates and bug-reports to find the ‘new features’ or ‘requirements’ - making it more like a few thousand. And it seems unlikely that commercial sources would have orders of magnitude more to offer. This is like training a spell-checker using a corpus of ten thousand English sentences—it will perform terribly. For example, on the Google Flu Trends link above, you can see that for the Canadian provinces/territories of PEI, NWT and Nunavut, there is not enough data (due to small populations) to make any predictions.

Getting more data isn’t obvious, either. We might aggregate the projects together, but each individual project tends to be very different in how they use language, so essentially it is like configuring ten different languages for your spell-checker each with ten thousand sentences. Impossible!

So assuming automating requirements extraction from project data is useful, how might we do this? I think there are two approaches. One, we downgrade our definition of ‘automation’ to allow for human judgement. This might mean asking developers to define a common project lexicon, or to be more diligent about annotating requirements automatically (many projects already separate these). However, asking developers to do things other than their core activities (writing code!) is usually doomed to failure unless it is _very_ painless.

I think the other approach is to move past the bag of words model. In most statistical learners, you throw documents or sentences into a huge corpus. This works great for standard information retrieval examples like the [Reuters corpus](http://about.reuters.com/researchandstandards/corpus/). But in software projects, it feels like by doing this we are losing a lot of the metadata, like dates or people, that might be relevant. Perhaps if we somehow annotate the training data with this information, and feed that into a learner, we would have more success.






* * *






	
  1. I may be ball-parking these numbers! [ ↩](1)



