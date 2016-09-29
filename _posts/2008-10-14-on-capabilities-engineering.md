---

date: 2008-10-14 18:38:33+00:00
layout: post
title: On "Capabilities Engineering"
tags:
- empirical
- evolution
- paper
- reading
- requirements
---

"[Improving change tolerance through Capabilities-based design: an empirical analysis](http://www.bibsonomy.org/bibtex/281c4da7098a2c999798454a2f2c620db/neilernst)", by Ramya Ravichandar, James D. Arthur, Shawn A. Bohner and David P. Tegarden. J. Softw. Maint. Evol.: Res. Pract. 2008; 20:135–170

The scope of this paper is building software systems that are change tolerant, where "the term ‘change tolerance’ connotes the ability of software to evolve within the bounds that it was designed". It's important to keep in mind the phrase "within the bounds" -- this limits this technique to _de novo_ design, rather than adaptive design (i.e., design that admits new components after the initial implementation). Any design that is designed to be change tolerant necessarily requires identification of potential changes up-front. And the authors acknowledge this with a small dig at agile techniques as being 'unconventional' (not anymore) and unproven (unlike the enormous body of evidence supporting waterfall processes :).

It would seem the focus of the paper is on complex, emergent systems: "requirements and technology often evolve during the extended development periods of complex emergent systems, and thereby, inhibit a comprehensive up-front solution specification" (agreed); yet the empirical assessment is of a course evaluation system. They measure how many classes are impacted by each change to assess how CE reduces change impact.

There are several problems with their empirical assessment. First, they compare "RE-based design" with their technique. They obtain the RE-design by reverse engineering an existing system, but they have not validated it as a 'good' design (we need to compare apples and apples, right -- both designs should have been created using the same amount of effort and skill). Second, the selection of change events is questionable; that the authors chose the change events implies bias in choosing those the CE-design is suited for. Finally, this system seems excessively trivial for a complex emergent system, as I mentioned before. Of course, it isn't easy to evaluate truly complex systems.

Capability engineering is a combination of abstraction, reduced coupling, and high cohesion design (which really tells us nothing -- who out there is designing systems that have high coupling and low cohesion? Possibly a few embedded systems, but not much else, I would wager). The key to the whole thing seems to be the **functional decomposition**, which is independent of system architecture/specification, and derived from user requirements. This commits the process fairly heavily to up-front requirements elicitiation, which is odd, since they claim to be concerned with complex, emergent systems, where (to my mind) requirements are never completely known from the beginning.

Complaints:



	
  * no reference is made to feature modeling, which seems nearly identical;

	
  * a bad case of EMS (Excessive Math Syndrome): too much detail about cohesion metrics, or algorithms for system design, when the real issue is coming up with the source numbers (anyone remember GIGO?);

	
  * conclusion marred by the confounding factor that the RE-system might just be poorly designed;

	
  * no reference to work on autonomic monitoring and correction (see [Yiqiao](http://www.cs.toronto.edu/~yw/)'s work).


Full marks:

	
  * acknowledging the issue of change in software systems (although I'm biased)

	
  * actually proposing a theory and testing it!

	
  * discussing threats to validity


What I liked the most about this paper was its fairly scientific setup. I don't agree that capability engineering is the panacea, but at least I can make concrete objections thanks to their well-structured paper.
