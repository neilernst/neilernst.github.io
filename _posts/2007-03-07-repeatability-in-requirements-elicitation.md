---

date: 2007-03-07 04:40:05+00:00
layout: post
title: Repeatability in requirements elicitation
---

Is it possible to design a requirements elicitation technique that is actually a function mapping Environment phenomena to Machine implementations (to paraphrase the [language of Jackson](http://mcs.open.ac.uk/mj665/topics.html#ReqSpecs))?  That is, can we design a process that always produces the same output for the same input?

If not, then the requirements elicitation phase is non-deterministic. We can never conclusively state what the outcome will be or should be, regardless of technique. An i* model, for the *exact* same circumstances and initial factors (assume we can 'rewind' time) will not be produced the same way twice. Some studies suggest this: getting students of approximately similar capabilities to create a model leads to many, quite different models.

Of course, there is difference and dissimilarity. That is, two models may be different -- element A is named B in the other version, the relationship is modeled as association instead of aggregation, etc. The models may not be that dissimilar though: they may converge on an approximate answer. [If we were in class](http://www.bibsonomy.org/bibtex/28847a3292cad24c0f0c2cebcd08b4e48/neilernst), we could say some models (of the same problem) get As, some Bs, and some fail (these people usually don't even try). This suggests there is some statistical distribution model we could apply that would capture how models varied from one another -- perhaps even a power-law model. There would be an exponentially larger number of good models than bad models, assuming all modelers are equally motivated and competent (no safe assumption, probably). If this is true I could apply for some social networking money, since anything with a power law is also a social network (I'm being slightly facetious here).

If you cannot be guaranteed determinism in requirements modeling, is requirements gathering/elicitation/modeling a science? Is it engineering? Engineering to me suggests repeatability: for the same initial factors, there is one best way to create the solution. There may be multiple varieties of solution: arched bridges, suspended bridges, bridges with black paint, etc.  But there is only one set of criteria for each that will satisfy the design requirements.  The laws of physics, materials, etc. dictate this. I think there is an element of this to RE: you have some notion of what the final Machine needs to look like from the customer. There are then a variety of solutions, with some 'more better' than others, for some definition of 'better', which may be completely capricious.

But these basic constraints on creating requirements models are less clear. Each time we go to create a requirements model, we are working within a framework of entropy and human dynamics that can never be repeated. The organizational context changes almost constantly. The wider business context for the software changes almost as often.

Many of the frameworks created for RE seem to imply that this non-determinism is manageable. For example, if you apply the NFR framework, there is one _good_ solution that will account for all the relevant variables and produce a demonstrably correct design.  Has anyone ever done this? Instead, I think the conclusion that is most clear is that the NFR technique is most useful in the process of conducting the analysis, **not** the end result.

For my research, the implications of this discussion go something like this: **If** the NFR and i* techniques are more useful for what is produced during the _process_, rather than the _artifact _itself, **then** there are no reasons to save the model artifacts. The value is transitory and encoded directly in the software.  And indeed, this seems to be the practice in industry, to wit, traceability is lost, design rationale is abandoned, and the code becomes paramount.  Mind you, there are very pragmatic reasons for this, having largely to do with business-pressures and a culture of short-term fixes that [many](http://codecraft.info/index.php/archives/70/) [other](http://www.codinghorror.com/blog/archives/000801.html) observers have noted (and embrace?).

So why worry about requirements evolution in this scenario? Few people care about the requirements artifacts, particularly the high-level business and domain models, after project completion. Nonetheless, I think we can agree that the software doesn't live in an unchanging context, desirable as that might be. It is constantly subjected to change pressure, as [Lehman](http://www.bibsonomy.org/bibtex/2e934d1b5f72ebaba1ad140d89fc35a40/neilernst) and others have pointed out. My conjecture is that understanding the mechanisms of this dynamic at the requirements level, particularly business and domain modeling, is important to managing the Machine/Environment relationship.

My work is focusing on first enumerating these mechanisms of requirements change, and providing a tool for accomodating changing requirements models, as current tool support is inadequate.  From there, I am using the changes we note in the requirements models, particularly the Environment models, to drive automatic acceptance test generation. This will allow stakeholders to have on hand a current set of tests that can be used to validate the software-as-is and software-to-be.