---

date: 2003-10-17 14:49:12+00:00
layout: post
title: Some thoughts on non-functional requirements
---

While I don't consider myself a software development process researcher (less well-defined 'intelligent' apps have always been of more interest), I'm coming to appreciate the usefulness of conceiving of systems (either knowledge or software focused) via an [aspect-oriented](http://www.aosd.net) or non-functional requirements perspective.  Finally, [Piotr's paper](http://ideanest.com/braque/ICSE2001%20Position%20Paper.pdf) on multi-dimensional separation of concerns is making sense! :)

I'm writing a paper on how knowledge engineering tools provide cognitive support, and the final section is focused on non-functional requirements.  The paper starts off describing some tasks in knowledge engineering which require cognitive support, then details how some common tools in the [Protege ](http://protege.stanford.edu)application address (or don't address) these tasks.  Finally, in order to tie the paper together, I look at how the need to support the tasks we identified can be addressed using non-functional requirements.  I read a little on this (more links are welcome) and I'm agreeing with the interpretation offered by Eric Yu, Lawrence Chung, and John Mylopoulos at U. Toronto - that NFRs are best seen as goals that need consideration during the design process ([a process-oriented approach](http://citeseer.nj.nec.com/mylopoulos92representing.html)).  These goals often can, and will, conflict. For example, if a company is interested in scalability and speed, bad design will develop something that directly addresses this goal. A better design would accept that there are other concerns, such as usability and security, that need to be addressed as well, and attempt to reify the trade-offs between them.
