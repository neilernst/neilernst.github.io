---

date: 2009-12-22 15:19:38+00:00
title: Evolving models is more than model management
tags:
- evolution
- model-driven
- uml
---

When we consider the nature of software-based systems over time, software evolution, there is always a lot of talk about evolving that system. Most famously, perhaps, [a set of "Laws"](http://en.wikipedia.org/wiki/Lehman%27s_laws_of_software_evolution) were proposed regarding software evolution.* And to date, most work on software evolution tends to be very focused on technical issues:



	
  * backward compatibility

	
  * transformations

	
  * versioning

	
  * comparison


However, at heart this issue is not just one of technical challenges (low-hanging fruit, if you will). You are dealing with a change in domain fundamentals -- e.g., a Car no longer has a combustion engine -- and this forces a change in nearly all other layers of your technology. Whether you believe in Model-Driven Something in Upper Case or not, reality is that the domain model does drive your software-based systems: as soon as cars can now have battery engines, your existing software is no longer adequate.

Resolving the technical details, like updating your UML class models with new BatteryEngine boxes, is a simple enough idea, I think (obviously the devil is in the details). More of an issue is figuring out "what" the change means and "why" there was a change. This presents a challenge because we technology types would rather worry about the "how" since it is more amenable to immediate tinkering.

To answer the what-it-means and why-the-change questions (as well as impact analysis), I think there is only one answer: you must maintain the domain model in some explicit form for the duration of the software lifecycle. What form the model takes is context-dependent: I wouldn't bother with a complex modeling solution if I was building a web site for a client, for example. It might be a [DSL for a very specific](http://www.infoq.com/articles/dsl-evolution) set of business rules, or a massive set of finite state machines and a model checker. But you cannot answer questions about change without some explicit model artifact (unless you have some savant developer who maintains the domain model and implementation details in her/his brain over many years).

Ideally, this model will be able to answer the why and what questions for you automatically, or nearly automatically. It will explore scenarios, evaluate impacts, and allow you to choose the preferred evolution path (for some context-specific set of preferences). Even better, this model will evolve quickly, so that you can push changes to the software quickly and nearly transparently.

* The term "Laws" is more reflective of the modernist and logical positivist origins of software _engineering_, a paradigm that has long outlived its usefulness. The notion that nature can be controlled has been flung happily into the trash in most other disciplines.
