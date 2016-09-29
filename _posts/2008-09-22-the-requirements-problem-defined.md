---

date: 2008-09-22 20:17:39+00:00
layout: post
title: The requirements problem defined
tags:
- requirements
---

Here's a useful way of thinking about how requirements, implementation, and preferences interact:

[caption id="attachment_932" align="aligncenter" width="195" caption="    the core problem, defined"][![](http://fink08.files.wordpress.com/2009/12/jureta-def.png)](http://fink08.files.wordpress.com/2009/12/jureta-def.png)[/caption]

Below are the ways these things are defined. Essentially, we are seeking a set of plans, P, that will satisfy the functional requirements, G, the qualities, Q, according to stakeholder attitudes, A, without violating the domain assumptions, K.






	
  * **Definition 1.** Believed content, i.e., \phi in B\phi, communicated by way of _assertive, declarative, or representative declarative speech acts_ is a domain assumption, denoted generically k.

	
  * **Definition 2.** Desired content, i.e., \phi  in D\phi, communicated by way of a _directive speech act_ is a quality constraint, denoted q, if and only if \phi describes qualities and constrains quality values. Described qualities must have quality space with a well-defined and shared structure.

	
  * **Definition 3.** Desired content, i.e., \phi  in D\phi, communicated by way of a _directive speech act_ is a goal, denoted g, if and only if \phi neither describes qualities nor constrains quality values.

	
  * **Definition 4.** Desired content, i.e., \phi  in D\phi, communicated by way of a _directive speech act_ is a softgoal, denoted ˆq, if and only if \phi describes qualities or constrains quality values, whereby the described qualities must have a quality space with a **subjective and/or ill-defined structure**.

	
  * **Definition 5.** There is a justified approximation, denoted jApprox(ˆq; q) if and only if there is a justification for the claim “q approximates ˆq” and there is sufficient correlation between values in the quality space of q and the quality space of ˆq.

	
  * **Definition 6.** Intended content, i.e., \phi in I\phi, communicated by way of a _commissive speech act_ is a plan, denoted p.

	
  * **Definition 7.** Attitudinal content communicated by way of an _expressive speech act_, i.e., \phi in A\phi, is an attitude, denoted a, if and only if it evaluates in terms of favor or disfavor one or more elements constituting K, P, G, Q, or ˆQ.


This is from Jureta, Mylopoulos and Faulkner, 2008, ['Revisiting the Core Ontology and Problem in Requirements Engineering](http://www.bibsonomy.org/bibtex/2971c9eea4bab0cff18d5f00d3e6510a8/neilernst)".


