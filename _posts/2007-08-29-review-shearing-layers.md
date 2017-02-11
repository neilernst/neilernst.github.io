---

date: 2007-08-29 04:59:37+00:00
title: 'Review: shearing layers'
tags:
- CWA
- goals
- i*
- kaizen
- shearing-layers
---

`@techreport{simmonds_shearing_2000,
title = {A Shearing Layers Approach to Information Systems Development },
url = {http://systemicbusiness.org/pubs/2000\_IBM\_RC21694\_Simmonds\_Ing\_Shearing\_Layers\_Info\_Sys\_Dev.html},
author = {Ian Simmonds and David Ing},
number = {RC21694},
year = {2000}
}`

In "[How Buildings Learn](http://www.amazon.com/How-Buildings-Learn-Happens-Theyre/dp/0140139966/ref=pd_bbs_sr_1/102-5738510-6468952?ie=UTF8&s=books&qid=1176055422&sr=8-1)", author Stewart Brand discusses how buildings change and adapt over time. One of his major themes is that the process can be modeled with a '[shearing layers](http://en.wikipedia.org/wiki/Shearing_layers)' model, reflecting increasing frequency of changes -- Site, Structure, Skin, Services, Space Plan, Stuff. The idea is that there are different timescales between the layers, and also that each layer determines the course of the one that follows it. For example, the site of a building will determine to a great extent the properties of the structure (e.g., air conditioning, steep roof, wood frame, etc.).

In this paper, Simmonds and Ing apply this same model to system development. The focus is oriented more to computer-supported work activities, specifically the design of information systems. I found the paper oriented to the sociological.

In theories of requirements and goal models, "the approach starts from system-level and organisational objectives from which ... lower-level descriptions are
progressively derived[[DvLF](http://www.bibsonomy.org/bibtex/2b29a6a271fc1d4f991acb0092c770350/neilernst)]." (see also [Anton](http://www.bibsonomy.org/bibtex/225d015f01a84a1719c74f0a180f30e08/neilernst), [Mylopoulos](http://www.bibsonomy.org/bibtex/2c00058f9ed68f2501f1f040ced28a9d9/neilernst)). Put another way, if we can construct our goal model from the top down, refining sub-goals as necessary, we are implicitly suggesting that these lower-level goals are changing more than the top-level ones do. We use the top-level goals to define what objectives the lower-level goals need to satisfy.

I suggest that goals are not sufficient. In [CWA](http://www.mie.utoronto.ca/labs/cel/research/frameworks/cwa.htm), goals represent the top layer of the abstraction-decomposition space, but the system design as a whole is also constrained by things like site and structure, which Brand was describing. For example, our top-level goals have to be constrained by physical laws and properties. We can't schedule meetings simultaneously for the same participant, since she is physically incapable of being in two places at once. Shearing layers act as constraints on our goals.  We need a formalism that handles this.

Simmonds and Ing emphasize the need for designs to be adaptive -- ""how can engineers optimize for change rather than stability yet do that efficiently, effectively and safely?" To adapt, one must be constantly gauging the state of the external world, and the concomitant implications for one's system. They provide a clear division between change -- system-initiated responses to external forces -- and evolution -- which I characterize as user-initiated responses. Autonomic systems can change, for example, by following [alternative goal decompositions](http://www.bibsonomy.org/bibtex/2828365e255d8ef8a076d827bfc60a6d4/neilernst), but can't evolve, since that requires human intervention (to, for example, change elements in the goal model, to redefine high-level goals, or to add resources (new code, new components)).


<blockquote>Here we build on rigorous definitions from systems science (Ackoff and Emery, _On Purposeful Systems_, 1972). An organization may be purposefully adaptive because its parts — people and smaller organizations — are purposeful. A system is purposeful if it is ideal-seeking. Software, which is a mechanism, is at best goal-seeking (and so purposive), since it cannot itself change the ends that it pursues. Thus software is at best adaptable and if it is this is a property of the way that it is constructed rather than the way that it functions [p. 9].</blockquote>


An excellent definition of issues I've been struggling with as well. Particularly in the context of autonomic systems, there is a real question as to what extent a system can evolve. Clearly, per this definition, true adaptation can only be implemented by a purposeful agent. Ackoff and Emery seem to be suggesting that only intelligent agents can show purposeful behaviour. I wonder whether Ackoff and Emery would reconsider in light of the increasingly blurry lines between software, intention, and agency.

Does adaptive imply agile?  While Simmonds and Ing focus on 'user-centered design', I think what their approach really requires is a [_kaizen_](http://en.wikipedia.org/wiki/Kaizen)-like constant reinvention of the system. A shearing layers model can identify where those changes will occur most frequently, and where maintenance and evolution efforts ought to be targeted.


### Towards a new syntax for i* modeling with CWA


Ideally, we would "embrace and extend" i* to give it the ability to create models that can be a) optative b) structural and c) constraint-based (shearing layers). I think the best way to accomplish this will be by combining i* with the CWA "Abstraction-Decomposition Hierarchy". The AH forces a structural and constraint approach that ignores mood in favour of describing the various elements, both of what is and what will be. This is tolerable because all of the elements being described are in the problem domain. Solutions take the form of processes that identify how the various structural means-ends relationships are achieved.



	
  * Actors are not present. Goals are assigned to the 'system'. Actor intentions become more relevant when we discuss strategies for achieving the system goals. At this point, we must consider the actor motivations and internal constraints. This is perhaps the most controversial aspect of a constraint-based approach, as most researchers in cognitive engineering give the actors complete primacy (as a reaction to the many design processes that place humans as the least valuable part of the system).

	
  * Tasks are not modeled at this stage. They are used in the next phase, once the structural constraints and physical properties are identified.

	
  * Resources are modeled in much greater detail than i* typically considers. Resources represent structural aspects of the domain.

	
  * Goals are elaborated from a system point of view. There is no specific attachment to an actor. This approach is closer to the NFR or KAOS modeling methodologies.  Non-functional goals (softgoals) are present.

	
  * Modeling elements are associated with metadata. This metadata might describe the risk of not fulfilling a goal; the evidence to support the placement of a means-ends link; the importance of a goal and its associated means. The metadata is used in the second phase of modeling, where tasks are elaborated and more traditional i* analysis completed - e.g., label propagation. In the third phase, the analysis results are used to enumerate a list of strategies that can be used to fulfill the goals.

	
  * Phase 4 assigns these strategies to actors. It is in this phase that we start thinking about actor intentions and motivations.

	
  * Phase 5 might be necessary for systems that rely on operator skill. Here we consider the formative design by using frameworks such as Rasmussen's "[Skills, Rules and Knowledge](http://www.bibsonomy.org/bibtex/23e0fc7b962143a2b724bf7243fc4050a/neilernst)" framework.


