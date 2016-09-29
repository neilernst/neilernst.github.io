---

date: 2005-06-03 18:34:07+00:00
layout: post
title: 'RSR: implementing Really Simple Requirements'
---

We can start with the [M. Jackson framework](http://www.citeulike.org/user/neilernst/article/121868) for requirements engineering.  It has omissions (e.g., where is the system boundary, and who is drawing it?  What about change over time?  How do we guarantee an indicative assumption Ε will actually hold when the system is built?) but is a useful start for thinking about requirements.

We want to define, in our project, the set of things we are going to create.  These are the wishes, or desires, that we have identified as being necessary.  They are specific to the environment context, not to a particular machine.  E.g., "I would like a report every 2 weeks listing employees and their billable hours".  We discover these through elicitation.  Each of these is a requirement, and may be decomposed into more specific requirements - "A two page report in black and white".

Software engineering then takes these requirements, R, and using some assumptions about the indicated state of things in the environment, both now and after the machine is constructed, Ε, derives a set of specifications, S, of how the machine should be constructed.  I consider the derivation of a specification to be the first step in design.

A specification links causal chains in the environment to components of the machine (not labelled by Jackson, but are lines of code), and thence back to the environment.  E,S ⊢ R.

So in increasing order of detail, we have R, optative conditions, then S, specifications that together with E, satisfy R.   I argue the next step is to decompose S into specific test cases, T, that satisfy S.  This is a form of test-driven development.  The tests are a form of pre/post conditions that delineate how such specifications work, e.g., 'given a table of employees, and a table of billing' - do something - 'produce join of employees and billing'.  The tests ensure adherence to specification (which in turn adheres to R).  Once tests are written which satisfy all elements in S, we have a complete system, and can begin writing code that satisfies T.  Code writing is the last step.

Test cases should be written in a syntax that is testing framework independent, and yet maps onto common tools, such as JUnit or PyUnit.  For example, universities may define common testing classes (e.g., AbstractPreconditionTestClass) which can be extended to test specific classes and methods in a system.  This way the tests reside in the code, and requirements are traceable via these tests.

Thus, the RSR solution proposed here works from two aspects: one, alter development practices (tests are written first), and two, make the lineage of a particular feature readily apparent through a requirements-test-tree, such as [Bin Liang proposes](http://www.third-bit.com/~bliang/reqtrace/draft.html).  The key is to ensure thorough adoption by making the user aware of the benefits of the methodology.

This methodology is agile-oriented.  Rather than specific requirements and detailed specs, which is a 'fragile' way of developing, I suggest retaining flexibility by proposing user stories rather than specific requirements.  These stories can then be broken into components, specifications, and tests written to fulfill the stories.  To stand in for the customer role, the professor in courses can specify the stories in detail, and be prepared to answer, on a public list, questions posed by the developers.  This is necessary since requirements gathering and modeling is often highly iterative: development of a particular requirement might spur rethinking on other requirements.



#### Reference


[This paper](http://www.citeulike.org/user/neilernst/article/212915) discusses how test-driven development might lead to better code.
Scott Ambler has a [good essay detailing the role of requirements](http://www.agilemodeling.com/essays/agileRequirements.htm) in agile development, with good examples of developing requirements iteratively
