---

date: 2009-12-31 14:52:46+00:00
title: Stories vs. models
tags:
- agile
- models
- user story
---

One of the central concepts in various agile software development techniques is the user story. Why go with a 'user story' instead of a rigorous requirements  elicitation, culminating in a model of varying complexity? Is a story enough?

What is a 'user story'?  These statements are (originally) from [Agile Model Driven Development with UML2](http://www.ambysoft.com/books/theObjectPrimer.html). Caution: as far as I can tell none of these statements is  empirically tested (or possibly even derived).



	
  * "a user story must be able to be                          implemented by two people in a single iteration/cycle"

	
  * "the                          user story card includes an indication of the priority"

	
  * "You often create a stack of user                          stories during cycle 0 to identify the scope of your                          system"

	
  * "Stories make it easier to divide the work into tasks than use cases"  p 321

	
  * "user stories are malleable and change during cycles"

	
  * "because they’re small that they are                          very easy to work with and to evolve"

	
  * "user stories contain so                          little information you will need to flesh them out a bit                          when you first work with them"

	
  * "User stories are merely the starting                          point" for figuring out how to implement these stories.


Here's an example, from the same source: "Parking passes can be paid via credit cards".

So this user story takes two people pair programming about a week (for an average project). Really? Anyone who has worked on task-decomposition, whether in personal life or for work, would probably agree that the tough part isn't determining goals, but figuring out how to achieve them. In other words, _what concrete set of steps do I take to get this achieved? _Presumably going from the story to the implementation is something a competent developer can handle, but it seems to me that a lot of design is hidden within that story: what does payment mean? What types of credit cards? Do we need to handle monthly and daily parking passes? And so on.

I would like to see a distinction drawn in talking about software development: We can talk about the process used to develop software: e.g., plan-driven, design up front, vs. work-in-progress limited lean development. But we can also talk about the artifacts used to drive the development. We could use stories and an onsite Customer. We could also use more formal requirements models, issue trackers, bug repositories, etc. I think these two are to some extent orthogonal. Nothing says the model must be set in stone before implementation.
