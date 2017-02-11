---

date: 2012-07-06 17:23:36+00:00
title: 'RE-KOMBINE: Paraconsistent Reasoning for Requirements'
tags:
- requirements
- techne
---

Here I try to summarize the work and motivation for my dissertation, or parts thereof. One of the bigger components of [my thesis](http://fink08.files.wordpress.com/2005/03/ernst_neil_a_201206_phd_thesis.pdf) is RE-KOMBINE, which is a reasoning engine for requirements models. You can find the [code and examples here](http://github.com/neilernst/Techne-TMS).


A central problem in requirements engineering (RE) is to understand what to build next. Requirements models are representations of what your system needs to accomplish. They encompass both that which exists, the current payroll system, for example, and what needs to be created—the interface between the payroll system and the point-of-sale system, for example. Like any model, requirements models are imperfect copies of the real world, with the degree/extent of imperfection reflecting cognitive support characteristics. For example, some of the most popular requirements models are informal lists, kept on paper or in a spreadsheet.

My dissertation research was about better understanding what a good model of evolving requirements ought to do. And I’ve come to the conclusion (somewhat diametrically opposed to my beliefs at the start of my Ph.D.) that formality is not only NOT harmful, it is under-utilized.


## Formality considered essential


One’s representation of a problem is either informal or formal. I don’t understand people who say they are ‘semi-formal’. That’s like being a little pregnant. Formality means very specific things in this domain. Furthermore, if we want to do anything with a machine like a computer, we cannot give it inconsistent instructions. Most of the machines we’ve built do very badly with inconsistent information (although we are working on that). So even though you may claim to have a ‘semi-formal’ language, at some point it will assuredly be formal. It’s just that the process of translation may be found at a different point in the chain. E.g.

problem domain → req. elicitation → informal model → Rational requisite pro/Blueprint → knowledge/software engineer (makes many decisions that were ‘implicit’ → formal representation (code, typically)

VS.

problem domain → elicitation → formal model → translation engine (human/automated) → source code


### But what do we mean by ‘formal’?


Opponents of formalization often characterize it as unwieldy, non-scalable, confusing for end-users, etc. Is it difficult for humans to represent things in a formal system? Sure.
But as this book says, “the power of formalization is that, once formalized, an area of interest can be worked in without understanding” (Reeves, S., & Clarke, M. (2003). Logic for computer science. Addison Wesley. Retrieved from http://www.cs.waikato.ac.nz/~stever/LCS.html).

This makes formalization particularly important for sharing with others, or for using computer programs. Is reading a formalization challenging? Yes. There is much abuse of notation in many formal research papers, and even worse, the demand formality places on clarity of presentation necessitates an unwieldy presentation (you cannot just wave your hands and ‘claim’ something is true). But that is also the beauty of it - once you understand the formalization (for example, propositional logic), it becomes impossible (or rather, very difficult) to hide wooly thinking. Is formalization subject to scalability challenges? Sure. If a problem is inherently NP, formalization won’t remove that. But neither will being informal. I actually think titles like “formal methods” or “formalization” are not helpful. They have so much baggage that the terms have become pejorative. Also, if you are a researcher in software, and don’t understand propositional logic, lambda calculi, complexity theory, etc., shame on you. Even if you work on human-computer interaction, these topics will make you a better researcher.


## Techne (τέχνη)


We have been working on another requirements modeling language, Techne ([see this paper](http://jureta.net/papers/techne-RE10.pdf)). Why another language? We have plenty of requirements languages: KAOS, Problem Frames, i*, Tropos, UML (sort of) … In Techne we tried to write a language that was minimal and captured the essence of the requirements problem: given your requirements, find the implementation choices that will satisfy them (originally proposed [by Zave and Jackson](http://mcs.open.ac.uk/mj665/fourdc.pdf). We are working on ways in which Techne can be extended with concepts for more expressive models, using actors, numeric weights, and so on. But the initial language is merely requirements, tasks, and constraints (domain assumptions).

Requirements and tasks (nodes) are encoded as propositions, and the only formalization necessary is the relationships between propositions. These come in two flavours: implications, which capture the notion that (for instance) implementing task T will satisfy requirement R. We didn’t want to have propagation of ‘partial’ anything, like other languages, because it is unclear what partial satisfaction means. So Techne allows for conflict relationships to represent the situation where doing one thing means another cannot be done, which we write as D ∧ E → ⊥. (Read as satisfying requirements D and E will be inconsistent).

Why is this stuff useful? Techne makes two main contributions. One is to present a formal requirements modeling language with very well-understood proof theories and theorem provers (using Horn logic). It is decidable and polynomial to find inconsistencies (not the case in full SAT). The second contribution is the addition of the following notions: mandatory and optional states for nodes; preferences between minimal solutions in a set of requirements; and approximations of softgoals using quality constraints.


## Node labels


Typically in requirements models we want to associate with each element a label reflecting the satisfiability of that node (hence the use of SAT solvers). We might monkey around with this notion, for example by using four-valued logic to handle ‘partial satisfaction’ (e.g. [Sebastiani et al.](http://scholar.google.com/citations?view_op=view_citation&hl=en&citation_for_view=ulB0WtkAAAAJ:Tyk-4Ss8FVUC)).

Some nodes, certainly domain assumptions, and possibly tasks we have chosen, will start with labels (let’s call them T or F for now, although the mapping from these letters to the notions of Truth or Falsehood is not straightforward). The outcome of ‘evaluating’ a goal model (or other requirements model) is a labeled model, which tells the analyst which elements can be satisfied (hopefully the high level requirements!). We can also call this a ‘solution’ to the requirements problem – it tells us which elements will satisfy our optative properties.


## Types of reasoning


I’m primarily considering logical reasoning; there are other pseudo-logical algorithms available. I am trying to collect these[ algorithms on GitHub](https://github.com/neilernst/goal-reasoning). I’d love pull requests.

All requirements languages rely on consistent models. That is, if an inconsistency is found (that bottom, ⊥, can be derived), the entire model is trivialized; the inconsistency must be removed.

Two main approaches are forward and backward reasoning. In forward reasoning we start with a set of ‘facts’, and try to determine what ‘goals’ we can fulfill. Expert systems work like this, too. Considerations: can you support cyclic graphs? Does the algorithm terminate? Is the algorithm scalable?

Backward reasoning starts with a goal, or goals, and works to find the facts that make that rule true. This is how Prolog works: resolution proofs. I’m not aware of any requirements languages that support backward chaining; datalog might be an example though, and if we generalize requirements models as KR systems, there is a lot of work here.

A final way to reason about goal models is to try to ‘label’ the graphs consistently. I don’t hold this to be either backward or forward reasoning: instead, you are just brute-forcing the problem into a set of conjunctive normal form (CNF) formulas, and then trying to satisfy the resulting wff. This problem is NP-complete, but SAT solvers have advanced to the point where most requirements problems should be readily solvable. The nice thing about the CNF representation is that there are a variety of twists on the boolean satisfiability problem, such as WeightedSAT, MaxSat, MinCostSat, etc.


## RE-KOMBINE


To extend these approaches, we noted that it is often desirable to support _paraconsistency_, that is, tolerating inconsistency. There are at least four reasons for allowing inconsistent statements and working around them (after [Nuseibeh et al.](http://www.sciencedirect.com/science/article/B6V0N-43RHW98-9/2/c3ddc41fdcf7e06032699f48ba18ad70)):



	
  * to facilitate distributed collaborative working,

	
  * to prevent premature commitment to design decisions,

	
  * to ensure all stakeholder views are taken into account,

	
  * to focus attention on problem areas [of the specification].


RE-KOMBINE is the name of [the tool I wrote](http://github.com/neilernst/Techne-TMS) to support paraconsistent reasoning over Techne models. You can view [a presentation which summarizes it](http://www.slideshare.net/NeilErnst/supporting-agile-requirements-evolution-via-paraconsistent-reasoining) on Slideshare, or [read the CAiSE 2012 paper](http://fink08.files.wordpress.com/2005/03/caise-incons.pdf) for more in-depth discussion.

If we continue with the Techne notion that we should have propositions which are either requirements, tasks, or domain assumptions, and then allow for refinements and conflict relations between them, then our paraconsistent approach simply says that we _credulously_ accept minimal solutions which entail the desired requirements. That is, we are merely looking for a subset of the tasks which satisfy our requirements.

This is nice, because it means that even if there is a possible conflict between two requirements, or between a domain assumption (like “Don’t Use WEP”) and a requirement (“Use WIFI for remote terminals”) we can ignore that conflict as long as there is a ‘workaround’ solution. We like this, because it means we can be more flexible (agile) by looking for the immediately implementable solution, and worry later about how we might actually make the conflict disappear.

The only constraints we impose is that our domain assumptions are internally consistent, and that the requirements we are seeking to satisfy are also consistent with each other (if this isn’t the case, then presumably the operator is confused).

We used RE-KOMBINE on the Payment Card Industry case study (PCI-DSS) as a proof-of-concept. Our next focus is to make this tool integrate with existing requirements management and work tracking tools, in order to seamlessly fit into existing workflows.

It’s possible this post was too long.
