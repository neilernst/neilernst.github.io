---

date: 2009-03-20 19:21:01+00:00
title: There is no such thing as a non-functional requirement
tags:
- nfr
- quality
- software
---

Non-functional requirements, or NFRs, have long been a subject of confusion for me. Typically, NFRs have been used to refer to properties of software that are not directly related to specific task-fulfilling criteria. For example, 'calculates GST' is a functional property of a system. 'Do it quickly' has historically been considered non-functional, in the sense (and here's my problem) that it is not directly affecting the ability of the system to do the task. Of course this is hogwash. If I deliver a system to a client that calculates GST owing in seconds, the client will reject it. I think similar arguments can be made for usability, security, reliability, etc.

My advisor, John Mylopoulos, wrote what is considered one of [the seminal works](http://www.bibsonomy.org/bibtex/25bfa7202a6bada96079712d57f4f2313/neilernst) on non-functional requirements. In it, he and his co-authors describe NFRs as 'global requirements on [the system's] development or operational cost, performance, reliability, maintainability, portability, robustness, and the like'. This is essentially an extensional definition (listing the members of the set, rather than the attributes any member must have). Indeed, in the paper they note there is no formal definition of non-functional (citing instead work on software quality).

Martin Glinz, an RE luminary, wrote [a tortured summary](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.94.9254&rep=rep1&type=pdf) of the research thinking on NFRs, proposing (of course!) a new framework for NFRs. I think the issue is simpler than that. Dispense entirely with the notion of 'functional' vs. 'non-functional' -- anything the client wants the software to do is functional. Rather, we focus on whether we can quantify a requirement or not -- e.g., does the system calculate GST -- and divide our requirements into goals and softgoals, where softgoals must be broken into quality spaces (response time, for example) to understand them. I think talking about software quality is a much more fruitful pursuit.
