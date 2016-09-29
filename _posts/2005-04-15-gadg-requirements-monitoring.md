---

date: 2005-04-15 21:01:37+00:00
layout: post
title: 'GADG: Requirements monitoring'
---

This week we looked at requirements monitoring, specifically papers by [Fickas,](http://www.citeulike.org/user/neilernst/article/159259) and [Feather.](http://www.citeulike.org/user/neilernst/article/159263)  This is an interesting area, because it proposes that requirements should move from design side, to run-time.  In the Fickas paper, they use the generated logical model of the system (system image?) to verify concordance with run-time implementation (based on soft goal links that act as constraints).  If the constraint is routinely violated, then a set of simple rules is used to implement customizations of the current structure of the program.  The group agreed that this rule-based adjustment was a little fragile.  [Related work](http://www.cs.toronto.edu/~cebly/) is done in the AI planning space, particularly planning under uncertainty, and planning with partial information, using tools like [hidden Markov models](http://en.wikipedia.org/wiki/Hidden_Markov_Model) and [Bayesian probability networks](http://en.wikipedia.org/wiki/Bayesian_inference).  Notes:


  * Rick wondered if maybe the user should be given control, not just of the program, or the logical model (UML, in the MDA sense), but also the goal model, to tweak.  This might take the form of altering weights on certain softgoals (speed, for example), and having the code adapt.


  * Create new alternatives using a feedback mechanism, preference elicitation work


  * See also Michael Jackson, requirements types


  * Goal refinement is a set of assumptions with more variability (distance from user's actual goals) at lower levels


  * Big question: is the RE goal achievable?  I.e. can a sufficiently detailed analysis actually produce something perfectly in line with user expectations?  Almost certainly not.  This is why, I conjecture, CWA type analysis is needed, since it provides a domain model (as RIck is suggesting) that the user can use at the KBB level, to deal with unanticipated/unexpected events.  If no, perhaps just use a small goal model and define a tight system boundary.


  * Constrain identification (CWA) is similar to identifying goals which may not always be met (idealized).  Can either show user a constraint to meet, or an example (analogical reasoning) that fulfills the constraint.


  * Where is the limit between human and agent in all this?  Can SOCA be used to specify this?


  * Can see an AH as a frame-based KR system.  Perhaps could use Protege as a base for reasoning about AH?


  * A fundamental distinction is between who is responsible for dealing with software problems: the requirements engineer, the designer, the user, or the system? And where does the design put that onus?


  * Need to consider that, when applying CWA to RE, the goal model is similar to the AH in that they are both to be declarative, structural artifacts.  The execution model in RE is an operationalization, just as SA is an execution analysis of the CTA.  The SRK framework maps onto the levels of abstraction between goal and design (the tacit and the explicit).


