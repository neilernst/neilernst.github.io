---

date: 2011-05-27 10:30:07+00:00
layout: post
published: false
title: Why research shouldn't worry about industry
---

One can find essays and surveys on industrial applicability throughout the software research field's (short) history. Perhaps the beginning of all software engineering can be said to be concerned with industry, arising as it did from the NATO conference (if by industry we mean very expensive defence projects). I think the underlying question is, Why didn't academics invent Rails, or Scrum, or GO, etc. I think the answer is obvious: they already have. But there's a huge difference between conceptualizing object-relational mappers and turning it into something so simple as Rails. Consider the code behind understanding the statement Person manages employees computationally. There is a lot of meaningless, research-irrelevant work behind the scenes to determine the proper mapping from "employees" to the Employee table.

Does that mean all research is worthwhile? Of course not. But the hair-pulling over research impact is largely a storm in a tea cup in my view. Here are a few reasons why we either cannot do anything about it, or should not be too worried:**
**



	
  1. **What is industry?** There is a big difference between software development in Microsoft, the 4 person web design firm down the road, and the software created for the US department of defence. Different needs and different expectations.

	
  2. **Adoption is always a challenge.** There is an entire research industry devoted to this topic. The very idea of marketing is about creating a need for your product. Look at the [Mobl research project](http://www.mobl-lang.org/). One of the reasons for its success (mindshare) is that the developer spent hours of his time fixing small bugs. I hate to admit it, but my software projects are full of bugs and exist solely to prove the points I make in my papers. If you want to use it for actual projects, there is a lot of work ahead. For example, I use code from a 1996 textbook. Its purpose is pedagogical, and so there are no improvements or speedups incorporated. Marian Petre [makes the same point here](http://catenary.wordpress.com/2011/05/19/how-do-practitioners-perceive-software-engineering-research/#comment-6782).

	
  3. **Research results are poorly disseminated.** IEEE and ACM do a horrendous job of being relevant to industry. Useful academic results are all hidden behind a paywall, guaranteeing no one will bother to access it. The irony is that most of the research is funded by government, so why the taxpaying public can't be assured easy access is beyond me.  Conferences like REFSQ and RE try to include industrial partners, but I have never seen any serious representation from IBM Rational or Blueprint at the conferences. (I should point out that Joy Beatty from SEILevel is the exception who proves the rule). SImilarly, when I've attended industrial conferences like BAWorld, I have found them full of vendor-driven hyperbole and glitzy advertorials. It's hard to see the relevance they have to research.

	
  4. **Industry isn't convinced by facts.** Look at every sale of Oracle databases. I'd wager very few of these sales are because the customer carefully evaluated Oracle against MySql, did some testing, wrote down an exhaustive list of requirements, and so on. I bet the sale was made by the IT manager, who doesn't know Oracle from a hole in the ground, but really liked the strip club the sales guy took him to. Consider Kanban, an innovative software process improvement technique. The research behind its use in software development is spotty at best: the original book consists of three not very rigorous case studies, all in very similar domains. The man behind the initiative stands to benefit financially from its success, and travels the world exhaustingly to promote the technique. Now, this isn't to say there isn't value; I think there very much is. But this isn't something software researchers can take on. And like all good engineering disciplines, research shouldn't be targeted because someone has an innovative idea in the field. Our role is to provide the underpinnings and theoretical understanding that shows problems and possible improvements. The entire Agile movement wouldn't exist without the research that showed the problems with waterfall development, by people like Barry Boehm and David Parnas.

	
  5. **Industrial problems are often not interesting**. Most problems in industry boil down to scale. Tools in academia may manage 100 requirements; industry needs them to handle 100,000. For a lot of researchers, this isn't an interesting challenge, because the work that must be done is in algorithmic optimization, tool improvements.

	
  6. **Useful failures are important.** In industry, you go bankrupt or get fired (unless you are in banking) if you lose money or fail. In research, failures are important. They point out what avenues are not worth exploring.

	
  7. **Software success is often about people.** I don't think Paul Graham succeeded because he used Lisp: in fact, one might argue he succeeded in spite of it. A key reason for his success was timing, and hard work. The best software process in the world will not survive a manager who is a buffoon.


Conclusion: As long as researchers are rewarded for publishing papers, there is little reason to focus on measurable results. And as long as companies can profit from bad RE practice, there is little reason to look for R&D improvements.
