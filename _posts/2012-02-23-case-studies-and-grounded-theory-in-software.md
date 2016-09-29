---

date: 2012-02-23 23:01:22+00:00
layout: post
title: Case studies and grounded theory in software engineering
---

# Case study vs. anecdote





In software development, many advances (by which I mean "better ways of developing software", where better is defined with respect to perhaps cost, time, value-delivery …) have come from industry and consultants proposing solutions to the problems they have come across1, of which some examples include _[Scrum](http://www.scrumalliance.org/learn_about_scrum)_, _[Kanban](http://www.amazon.com/Kanban-David-J-Anderson/dp/0984521402)_, _[Go](http://golang.org/)_, _[Continuous Delivery](http://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912)_, etc.  The argument could be made that one person's hundreds of consultations with troubled software projects provides him or her much more in the way of actionable observation than does a researcher's single site visit at a large organization, even if the latter is rigorously conducted. Several researchers have argued that the case study is not necessarily non-generalizable, and that it is probably the most useful empirical method for software engineering. However, I think this raises a bigger question: how does a well-conducted academic case study compare with the plethora of anecdotal evidence from software consultants?





Consider this [blog post](http://martinfowler.com/bliki/PrematureRampUp.html) by Martin Fowler. He is a well-respected member of the software engineering community, a thought-leader if you will, having written important books and posts on refactoring and agile software development. In this post, he talks about the notion of adding members to a software development team, the difficulties with which have long been recognized, starting with Fred Brooks and the IBM os/360 project. Fowler makes a few interesting points about this process, and as evidence for his beliefs, cites some of the many consulting experiences his team has encountered. The question for an academic, then, is how your efforts can be compared with his. Is his experience any less generalizable to theory? Is his data less valid for being encountered as part of a for-profit consulting gig? How can a researcher compete with the level of access Fowler has?





Ultimately what troubles me is this question: is the knowledge which Martin Fowler gains via these visits any less useful to us than that which is collected through a more "scientific" case study approach? While we would certainly reject a paper which did not explain the research questions, data collection approach, and discuss threats to validity, none of which are mentioned in his blogs (and why should they be!) I would argue that Fowler's experiences are in fact more useful: he is extremely experienced with software development, and the breadth of cases which he encounters makes the problem of research question moot. By at least one standard his knowledge has been directly applied: one can argue that the hugely influential "[Refactoring](http://books.google.com/books?hl=en&lr=&id=1MsETFPD3I0C&oi=fnd&pg=PR18&dq=refactoring&ots=pLN7t0WF9b&sig=jM7AP8hci1ApMI09eO2bFvkhaeQ)" book is a direct result of his anecdotal experiences2.





# Yin: analytical generalization to theory





The central argument against the complaint that case studies cannot be generalized (and therefore provide no general knowledge, just context-specific knowledge) is that of analytical generalization. This is a complex way of arguing that what you obtain from a case study is simply a singular datapoint about how phenomena are manifested. As the figure below, from Yin's book3, shows, the notion is that in any form of scientific inquiry we are interested in the theoretical implications (since we assume that the theory is how we make sense of the world). However, I've yet to encounter a similar notion to that of "[power](http://en.wikipedia.org/wiki/Statistical_power)" in experiment for case studies. It seems it ought to exist, because a case study which merely confirms what we've already suspected is less useful than one which, well-constructed, can give us good evidence against a particular phenomenon.





![Yin's diagram on making inferences(p32)](http://fink08.files.wordpress.com/2011/11/screen-shot-2011-11-11-at-13-27-42.png)





Flyvberg 4 makes a nice point about this: if you pick your case study subjects well, then you don't need to conduct a number of repeated experiments---one will be enough. This (to me) is what Kuhn and Popper have in common: the notion that intuitively, it ought to only take one good experiment to invalidate one's acceptance of a theory (where theory might mean as little as "intuition"). Flyvberg illustrates this by pointing out that what Galileo did in establishing a revised theory of gravity was simply a conceptual experiment about conjoined masses. Since he had chosen his case study subject well, he was able to confirm for himself that Aristotle could not possibly be correct. There was no need, in other words, to continue doing experiments with different materials, since by that point he had demonstrated a counter-example and invalidated the theory. He did not even need to concretely demonstrate this to himself, but only show it must be true - the black swan, in Flyvberg's words.





For me this illustrates the importance of case study selection. A poor selection will only be able to confirm what we already suspect, and in this must be supplemented with additional inquiry. But a well-chosen set of cases---for example, looking at bug fixing practices in a large industrial setting, in an open source setting, and in a safety-critical setting---could be sufficient to invalidate a number of existing assumptions. And for me this is also what distinguishes research from anecdote: research chooses cases so that they can serve this purpose. While the anecdotes of Martin Fowler _may_ do this, it is more likely that they are a series of confirmatory experiences, none of which illustrate much other than the fecklessness of management and the importance of concepts such as frequent delivery, customer interaction, and version control---none of which are remotely controversial5. However, should Fowler find a single case where agility hurt business value, then we might have an interesting experience to report (although I suspect those circumstances would be waved off as extraordinary and non-relevant).





It did not take practitioners long to formulate theories such as agile software development (prefigured in any case by the work of Brooks, Boehm, and even Royce's initial "waterfall" paper). Indeed, most of Extreme Programming was based on a single experience at the Chrysler Compensation system, hardly the stuff of rigour. I conclude, therefore, that as academics, one ought not to be fearful of the extensive industrial experiences of consultants, but instead apply strategic sampling in order to identify truly meaningful cases. I conclude this section with a nice passage from Flyvberg:





<blockquote>
  
> 
> Knowledge at the beginner’s level consists precisely in the reduced formulas that characterize theories, whereas true expertise is based on intimate experience with thousands of individual cases and on the ability to discriminate between situations, with all their nuances of difference, without distilling them into formulas or standard cases.
> 
> 
</blockquote>





In this light, then, perhaps we can cast Fowler's anecdotes: that it is innately difficult for him to distill the true nature of these experiences into simple narrative for the beginner.





# What distinguishes case study from anecdote?





There are fairly clear methodological guidelines for conducting formal case studies. To begin with, more (even _most_) problematically, Fowler does not make data available. Either because of time or NDA, there is no way to confirm any of the claims he makes based on the data6. This means we cannot in good conscience reject rival hypotheses, since there is no formal proof. A case study is one way of deriving scientific knowledge (parallel techniques include experimentation and ethnographic studies). Since the case study is well-suited to investigating problems in context, it has been argued this technique is most suitable for software engineering, given the well-documented challenges research in this area has with reproducibility and isolating confounding factors.





The most important aspects of a case study is to begin with a clear research question (either exploratory or confirmatory), correctly identify meaningful units of analysis (e.g., development teams, specific bugs, software components), and follow a clear methodology for data gathering (using purposive sampling to gather as much variability as possible). The academic would argue, I suppose, that without a clear research question, and an underlying theoretical perspective (e.g., there is a rich, tacit knowledge in development teams, and bug databases do not capture this information), one cannot generalize to a theory.





This is perhaps the most important distinction to keep in mind, particularly since case studies are usually dismissed as anecdotal or trivial by doubters (who desperately want software to be math or physics). In experiments, we select a (hopefully random) sample of a population, and test a specific research hypothesis on them, attempting to isolate the factors we believe truly contribute to the effect. For example, we may ask a set of students to model a problem with either UML or ER diagrams, and try to measure which technique is "faster", "richer", "more understandable". Assuming our study has sufficient power (large enough sample to be considered representative), and we have correctly controlled for unknown variables (unlikely, in my opinion) we can use this data to generalize to the wider population: for example, with a 5% chance of being a random result, we see that UML is 20% faster at modelling a problem.





In case studies, by contrast, we are generalizing to a theory. Let us say that we believe that bug repositories do not capture all the information inherent in bug reports7. We conduct a study at a single company of 10 bugs, interviewing developers, and tracking the bugs throughout their lifecycle. We find that the information that developers know about that particular bug is not completely accessible using artifacts. This suggests that our theory about bug repositories is on to something: at least, it isn't rejectable, yet. Such studies are often criticized for focusing on a single domain or company, where the findings may be completely different at a second or third setting. But I think this criticism misses the point. We now know more: that this study should be repeated at other places and in other settings does not invalidate the findings, but merely shows their limits. Instead, the criticism should be directed at the entire field: why do we insist so often on "new" results, rather than "true" results?





# Challenges with "grounded theory" in exploratory case studies





I think this issue of anecdote vs. case study extends to grounded theory as a way of sense making and theory generation. At best, grounded theory is merely a systematic way of thinking inductively (from multiple "samples" to a cohesive theory). At worst, it is highly confirmatory: you find the data you would like to see. Tagging something with a grounded theory label is a way of justifying the conclusions you drew, of formalizing what scientists do anyway.





But again, without the detailed notes, I have no way of assessing whether the codes you identified are reasonable. There was a nice article I read that characterized (Andrew Gelman?) this type of work as "story-telling": we seem to be highly narrative as humans, and so cannot resist spinning a good yarn. This leads to reading into the data effects which are poorly supported. The reality is that in many cases, there is a very weak effect at best; however, we get promoted for significant results, not minor improvements. This leads us to draw conclusions from the data that are not warranted. I worry that the same is true of grounded theory.





# The real challenge: reproducibility





The real obstacle, of course, is repeating these studies. In isolation very few results mean anything. They must be replicated and reproduced in order to have more validity. This is true of positivist experiments as well as qualitative case studies. Unfortunately very little effort is spent confirming results. Consider the claim that there is a significant factor of difference between good and poor developers. The evidence for this claim is largely old and poorly reported. What we need to do is conduct more studies to test this theory! Yet in software engineering research, testing existing claims is poo-poohed as not innovative. We favour those who generate theories, even if they make little difference or have no good support behind them.





And here is where I believe we can link the academic and the consultant: verifying claims8. In the piece by Martin Fowler I linked to above, he makes the testable claim that "any increase in productivity is likely to be proportional to the square root of the increase in people, so doubling a team will get you roughly a 50% increase in productivity". Of course this is surrounded by caveats, and yet it is something testable. We ought to be doing this as researchers: in many ways, the consultants and talking heads have generated more than enough theories about software engineering for us academics to begin verifying those claims. Consider:





  * "Kanban is an evolutionary system for changing workplaces that often leads to revolution".


  * "Pair programming is more effective than programming as an individual".


  * Test-driven development makes for higher-quality code.


  * Continuous delivery is preferred to piecewise delivery.








* * *






  1. Many academics would point to earlier research which argued the same thing. For example, the notion of incremental and iterative development was not invented in the 1990s---see C. Larman and V. Basili, Iterative and Incremental Development : A Brief History, _IEEE Computer_, June, 2003. ↩




  2. 


And boasts some 4100 citations on Google Scholar, with the closest academic papers with that search term coming in around 500. ↩






  3. 


Yin, Robert K., "Case Study Research: Design and Methods". Sage, 2003. ↩






  4. 


Bent Flyvbjerg, "[Five Misunderstandings About Case-Study Research](http://qix.sagepub.com/content/12/2/219)", Qualitative Inquiry 2006 **12**: 219 ↩






  5. 


Although to be fair, that was not quite as clear earlier in our knowledge of software engineering. ↩






  6. 


But clearly, also no reason to doubt his motivations. ↩






  7. 


J. Aranda and G. Venolia, The secret life of bugs: Going past the errors and omissions in software repositories, in _International Conference on Software Engineering_, 2009, pp. 298-308. ↩






  8. 


I should evaluate how many software engineering research papers are testing existing theories versus creating new ones (if they talk about theory at all: all too many papers are about some new technique or tool validated with a trivial and highly context-dependent data set--- a practice of which I'm guilty as well!). ↩






