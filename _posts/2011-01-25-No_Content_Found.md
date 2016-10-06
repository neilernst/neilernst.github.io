---

date: 2011-01-25 12:35:32+00:00
published: false
title: '10x Productivity: DeMarco and Lister'
---

There has been an interesting back-and-forth about one of the essays published in the book ["Making Software"](http://oreilly.com/catalog/9780596808303). The focus of the book is verifying claims for practices which improve software development, and in the essay "10x Software Development", author Steve McConnell puts forth his position (an expanded version of [this essay](http://blogs.construx.com/blogs/stevemcc/archive/2008/03/27/productivity-variations-among-software-developers-and-teams-the-origin-of-quot-10x-quot.aspx)) that there is an order-of-magnitude difference between the best and worst programmers in productivity (for some definition of productivity).

Laurent Bossavits critiqued this essay, [translated version here](http://morendil.github.com/folklore.html), McConnell responded [here](http://forums.construx.com/blogs/stevemcc/archive/2011/01/09/origins-of-10x-how-valid-is-the-underlying-research.aspx), and Jorge Aranda put [his view forth here](http://catenary.wordpress.com/2011/01/12/the-thorny-and-the-obvious/).

Since one of the key issues is the nature of the evidence for this position, I thought I'd use my academic subscription to these articles and check out the claims made. I'll start with the paper by DeMarco and Lister that McConnell cites.


### What constitutes evidence?


This is a key epistemological question for us, and I'm not sure the book has provided a clear answer. Greg Wilson, the book's editor, states


<blockquote>[I've learned over time] there are many other
ways to discover things. They may not be statistical, but they
are just as rigorous, and just as revealing.</blockquote>


in reference to whether only positivist inquiry is a valid source of evidence. I agree, but we should be clear what these "other ways" are. For me, they are not anecdotal reports, surveys that don't release methodologies, or examples claiming to be case studies. In my experience "discovering things" is time consuming and difficult if you want to make a general claim.

When we look at the paper I think there are three things to keep in mind. One, DeMarco and Lister definitely seemed to have a bias. They were convinced that poor treatment of people led to lower productivity (which is the focus of the study). Two, it was conducted an eternity ago for software development. Does that mean things have changed? Hard to say. Finally, it is very easy to find holes in papers and ignore the wider connotations.


### The paper


It's a good paper. The motivation is to study workplace environment and productivity. They secured 160 programmers from various software companies. They got them to pair up, and then complete a programming task. The fastest were 5.6 times faster than the slowest. Some didn't complete the task. Being fast didn't seem to be indicative of generating more errors, according to passing acceptance tests.


### Problems:





	
  * how were these programmers selected? what was the makeup of them in terms of gender, IQ, education, experience, etc? Were we comparing Microsoft programmers against BoringBankITDept? Were we comparing CMU grads against self-taught programmers (just to be clear, I'm not sure what difference that should make!)

	
  * why divide into pairs?

	
  * why were the tasks divided into two milestones?

	
  * the acceptance criteria were quite limited.

	
  * there are no calculations of statistical significance. It isn't clear why, when, how outliers should/could be excluded. Recall that in an experiment we generalize to a population. I would like to see more data showing that these claims are meaningful with respect to the population. Maybe in this particular study you encountered some random occurrence: that someone ran into problems with the submission, for example, or that someone else took a lunch break during the test. So simply saying that submission A was done is 100 minutes, and submission B done in 800 minutes, ergo 8x difference, is not valid. Let's be clear: lack of statistical significance doesn't mean, "there is an effect, but not a big one". It means quite simply that any effect is just as likely to be due to random chance as to a definite effect.

	
  * Not completing the tests does not mean they couldn't finish it. It might be that there was an extraneous confound, like the boss said they had to get back to 'real' work.

	
  * It is important to note that the paper does not make any claims for causality. They don't give reasons or even guesses as to why A is better than B (e.g., workplace, education, language, etc.)

	
  * The study was done in 1985, and the main language used was COBOL.


The paper is fascinating - the authors clearly put a lot of effort into the study. However, it wouldn't be acceptable as a paper in empirical software engineering today. There is no discussion of limitations, no obvious way to replicate it.

Summary

Is this paper an acceptable source of evidence for the claim that there is an order of magnitude difference in productivity? Since it is an experimental study, we must judge it on experimental terms. Since there is no statistical significance analysis, it is hard to accept the conclusions. However, it would seem that there is a small effect happening, should we be able to analyse the data. Nonetheless, the fact that the authors weren't clear about how they chose their sample population makes it impossible to conclude anything from this study.

It would be as if I gave you a sample of 50 young men and 50 old men, and told you that the young men were all over 6 feet, and the old men were under 6 feet, therefore humans are getting taller. But I didn't mention that the young men were people I encountered in the Netherlands, and the old men were all born during the Second World War. Dutch people are taller than average; lack of nutrition during early childhood stunts your growth. It might that all the DeMarco study shows is that people educated at CMU are more productive, or that programmers using IBM computers are better than PDP-11 programmers, or the balding programmers were faster than their hirsute companions. We simply can't separate confounding from causative in this study.

Again, this is the standard of evidence we must judge such a study by. If DeMarco and Lister had done case study research at several different companies, we might be able to conclude using a different standard that there is an effect.

Ironically, McConnell makes a similar point in his more recent essay on programmer compensation. Since the job of 'programmer' invariable involves more than just writing code to a spec, it isn't clear that the slowest coder isn't also the best tester, or the strongly connected component in the corporate social network, facilitating communication.

So is there a difference in productivity?

The clearest indication I'm personally aware of for software productivity is group work at the course level. Some groups produce A-quality work, while others are barely able to complete the basic requirements, and get a D. It's not clear why this is. Certainly in some cases certain students are more committed, more intelligent, and more capable. But in others we must blame group dynamics, intrinsic motivation, personal problems, and so on (even the teacher!).

Craftsmanship in coding is extremely important, but to me it is analogous to becoming an expert carpenter: the craftsman can frame the house in half the time an apprentice can, can eyeball instead of liquid level, etc., but both must work from some wider set of plans.
