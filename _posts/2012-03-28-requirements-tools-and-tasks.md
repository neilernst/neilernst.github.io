---

date: 2012-03-28 20:52:44+00:00
title: Requirements tools and tasks
---

Just read a nice paper by Dan Berry et al. [1] on tools for requirements engineers. It was a position paper that looked at the progress to date in using natural language processing (NLP) for requirements analysis, modeling, and comprehension. In it, they argue that we should partition RE tasks into the clerical part (tools can do this with 100% precision) and a thinking part, where tools can't come close to enough precision. The key part is this paragraph:


<blockquote>Finding this partition for any task will require research to think of a different way to decompose the task. It will require a thorough understanding of the task and of what is algorithmically possible. It will likely require ingenuity in finding perhaps multiple, orthogonal lexical proxies for the semantics of the task, whose combined capture of false positives is significantly reduced from that of any one lexical proxy. For any task, the partitioning will take into account – the burden to the human analyst of the imprecision of the clerical part and – the difficulty to the human analyst of the thinking-required part.

Obtaining this information will require research like that done by Dekhtyar et al.[ [14]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6051649&tag=1) for tracing tools to determine what is really difficult for humans and how well hu- mans perform parts of the task with and without automation. Addressing the issue of how to separate the clerical and thinking-required parts of a task is of course one of many research questions that challenge the developers of NLP-based tools for RE. The challenge of ensuring industrial adoption of the tools remains.</blockquote>


This is a great motivation for my immediate research direction. My tool, RE-KOMBINE [2], can automate the process of discovering possible solutions a given set of requirements. It can provide information to the analyst about the optimal set of user stories (or use cases, requirements, what have you) to prioritize for development. But it should not, according to Berry et al., try to automatically generate solution, nor should it concern itself with how the requirements are entered into the knowledge base (indeed, our support of natural language propositional statements seems as much formality as one can demand). Finally, it seems the most important research challenge is "determining what is really difficult for humans" in RE.

For more on RE-KOMBINE you can check out our CAISE 12 paper [2].

[1] Daniel Berry, Ricardo Gacitua, Pete Sawyer and Sri Fatimah Tjong, "[The Case for Dumb Requirements Engineering Tools](http://www.springerlink.com/content/v65xk36k04411271/)", _REFSQ_, Essen, March 2012.

[2] Neil Ernst, Alexander Borgida, John Mylopoulos, Ivan Jureta, "[Agile Requirements Evolution via Paraconsistent Reasoning](http://fink08.files.wordpress.com/2012/03/caise-incons.pdf)," _CAISE_, Gdansk, June 2012.
