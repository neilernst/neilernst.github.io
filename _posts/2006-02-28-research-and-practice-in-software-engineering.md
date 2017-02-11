---

date: 2006-02-28 23:22:33+00:00
title: Research and practice in software engineering
---

I just read the book ["Facts and Fallacies of Software Engineering"](http://www.citeulike.org/user/neilernst/article/385770) by Robert Glass.  First off, let me state the book is excellent and should be required reading for all software researchers. I am left with many thoughts, but primarily, the book has caused me to ponder the proper role of research in software engineering.

Glass is quite critical of researchers in the field, saying -- I believe accurately -- that there has been way too little evaluative research. His chief complaint seems to be the FUD spread by tool vendors; specifically, that researchers aren't evaluating claims and methods spread by these agencies. However, I doubt many researchers are that interested in validating claims like these.  Firstly, it is unlikely, without a regulatory scheme that insists on validation (e.g., medicine, pharmaceuticals, lasers), that companies would allow fair tests to be conducted. Secondly, such studies are very hard to conduct in software engineering.  Think of the difficulties of assessing how well the Rational Unified Process works, for example.  To eliminate external factors, the test would ideally be of identical problems, simultaneously, with one group using RUP and the other some other method. After both were completed, the data could be collected and analyzed based on some performance criteria (the definition of which is equally problematic).

This seems extremely unlikely to happen. The nature of software projects, as Glass mentions in his book, are time-constrained and highly stressful.  Adding researchers in would be difficult.  I think researchers understand this, and this is a key reason why little evaluative research is done.

More importantly, I think people like myself, junior researchers, don't see their role as one which supports the software industry. Is it my job to evaluate _current_ technologies for value?  Or is it my job to look farther afield for new technologies and strategies to improve the process?  In this context, practice in the field is less important.  It is a popular belief that researchers in software engineering don't understand the issues in the field, that they have their heads in the clouds. Like all stereotypes, there is a grain of truth to this, but the opposite is true as well. Software development isn't really a mystery. Most academics have read the books, used the tools, and keep abreast of the latest developments in practice. We understand the ad-hoc and shifting nature of software engineering. I think the same argument could be levelled at someone like my brother, who works on neuropsychology, specifically the chemical basis of depression.  Has he ever lived with it? Not to my knowledge. Is he a practicing psychologist? No. But that doesn't mean the basic truths of the discipline are therefore hidden to him. So I believe it is in software.

Specific notes on the book:

- p 13 refers to importance of people in software success.  This is a truism that underlies the difficulty in empirical studies.  Why should a researcher investigate a particular methodology when almost 90% of the success of a project is due to people factors (management and talent)?  These are externalities that are hard to control for.

- p 37 discusses the problems with managing to estimated schedules/milestones (which are the least well-known characteristics). Glass discusses managing to product outcome, issues/bugs, risk, business objectives, or quality.

- p 47 covers reuse-in-the-large vs in-the-small.  This seems like a hot topic nowadays with discussions about SOA and web services. Glass is skeptical, thinking that true component generalizability is nearly intractable.

- p 37 suggests that more research is needed on how programmers apply and make use of patterns, which are most useful, etc.

- p. 59 suggests that for every 25% increase in problem complexity, there is a 100% increase in solution complexity. Glass posits that complexity is the main reason software is designed and built in mostly ad-hoc ways.  He also acknowledges the role of complexity in the scarcity of evaluation in the field.

- p. 61 discusses the distinction between intellectual software design tasks and clerical tasks (creating a diagram). Glass gives evidence for an 80/20 split -- which suggests why tool improvements might not be that much help, given only 20% of the time is spent where a tool might help.  I suspect there might be room for tools to help the intellectual aspect as well, however -- for example, by helping to explore a solution space, e.g. with known design patterns. [Mylar ](http://www.eclipse.org/mylar/)fits in here.
- p. 92 discusses the various types of testing -- requirements-driven, structure-driven, statistics-driven (random), risk-driven.  I think the DrProject requirements/tests tool only covered the first aspect.

- p. 118 discusses maintenance types and costs. Maintenance in total is 60% (on average) of a project's total cost. Of this only 17% is fixing bugs. 60% is adding new features (hence the 60/60 rule). 18% is adaptive maintenance. 5% is refactoring. Sources for these numbers are Boehm, 1975 _The High Cost of Software_; Lientz, Swanson, and Tompkins, 1978, _Characteristics of Application Software Maintenance_, CACM; Landsbaum and Glass, 1992, _Measuring and motivating maintenance programmers_.

- p. 121 The maintenance life cycle according to Fjelsted and Hamlen 1979: Defining and understanding the change (15%), reviewing the documentation (5%), tracing logic (25%), implementing the change (20%), testing/debugging (30%), and updating docs (5%).

- p. 125 mentions that better software engineering means more maintenance, that is, better built systems are easier to update.

- p. 129 Glass gives seven attributes that define software quality: portability, reliability, efficiency, usability, testability, understandability, and modifiability. He discusses the notion that different projects prioritize these differently. Source for these is Boehm, 1978, Characteristics of Software Quality.

- p. 136 suggests that there may be a power-law distribution for software errors, e.g. that some modules have greatly disproportionate numbers of errors.

- p. 178 Glass argues that basing future predictions of maintenance on past experience is foolish. He argues this is mainly because existing work focuses on repair rather than enhancement, which we have seen is much less important.

I think the last point helps to illustrate my conundrum about this book. While I think it is important to keep these facts in mind, I don't think that this last fallacy means research in maintenance needs to ignore things like Bayesian prediction. More work is required, and I don't think researchers need to be overly concerned with solving practical problems of the here and now.
