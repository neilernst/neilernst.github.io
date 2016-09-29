---

date: 2006-11-09 22:20:27+00:00
layout: post
title: Multi-Agent systems and service-oriented computing
---

I've been experimenting with the [JADE](http://jade.tilab.com/) agent platform, along with the [JADEX](http://vsis-www.informatik.uni-hamburg.de/projects/jadex/) [BDI](http://en.wikipedia.org/wiki/BDI_software_agent) extension. One of the [case studies I've come across](http://www.bibsonomy.org/bibtex/0ea9210d8bcc7112cc6974f2898c9a3c9/neilernst) has been to simulate LP for hospital scheduling.  In this example, patients are agents with beliefs such as criticality of their medical condition. The resources are OR availability, for example.

In general, I can think of several objections to the MAS approach:



	
  1. Communication doesn't scale well - it is n^2 in the worst case(?). Clearly this can be remedied with well-designed agent architecture. Perhaps Tropos should include some sort of complexity checking routine in the design phase?

	
  2. Behaviour is opaque - a derived solution may not be comprehensible due to the complexity of interaction effects (agent interaction is something of a black-box).

	
  3. Speed may be an issue.


In this example, it isn't clear to me that the MAS approach is a significant improvement on other constraint programming approaches, e.g. genetic algorithms, machine learning, what have you. Furthermore this may be a slower solution due to the large overhead the agent platform incurs. The article doesn't evaluate this problem.

My current thinking is that MAS simulations of 'standard' OR problems - linear programming problems -- seems like a fairly interesting proof-of-concept, but nothing terribly useful.

Where MAS could be useful, though, is in circumstances where there is imperfect information. In particular, this might involve web services, where the QOS demands are important (which are, in turn, informing the high-level NFRs of the system). We could model each web service as an agent, with dependencies, and then simulate for observed failure rates, and so on.

Alexei noted that it is difficult to compare a MAS to a 'standard' software system. This might make a theory that discusses such a system in the context of requirements evolution less generalizable. However, I feel that there is enough of a win from using a well-established methodology like TROPOS to make this problem less troublesome.
