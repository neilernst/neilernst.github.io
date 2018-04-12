---

date: 2007-12-19 17:21:41+00:00
title: Preserving knowledge in design projects
tags:
- chi
- design rationale
- paper
- requirements
- scenarios
---

James D. Herbsleb and Eiji Kuwana. [Preserving knowledge in design projects: what designers need to know.   ](http://bibsonomy.org/bibtex/22fb0378edddebb0c737393f4808e9ab9/neilernst)CHI '93: Conference on Human factors in computing systems,  7--14 , Amsterdam, April 1993.

I hadn't read this paper until it was recommended to me by an advisor, but it is now one of my favourites. It describes an experiment the authors ran on three industrial software projects. They had access to the requirements and design phase meetings from these companies ([NTT](http://www.ntt.co.jp/index_e.html), [Andersen](http://www.accenture.com/home/default.htm), and [MCC](http://en.wikipedia.org/wiki/Microelectronics_and_Computer_Technology_Corporation)), and coded the discussions based on three variables: the target of the question (subject of the question, categorized as _evolve, task assignment_,_ interface, realization_, and _identity_), the attribute of the question (_who, what, how, why, when_), and lifecycle stage (_req, design, impl, maintenance_).

The results were somewhat surprising. While most questions referred mainly to requirements or design stages (not surprising, since these were planning meetings), few questions sought the intentions behind a decision. Many more questions were oriented to 'what' was being changed/affected (~60%), and 'how' that was to happen/happening (30%).

Practitioners might not find this surprising; after all, pragmatically those two questions are most relevant to "getting 'er done". However, at the time (1993) there was a lot of work on design-rationale tools, which specifically targeted the 'why' questions. This is also a central argument behind early-requirements analysis: that understanding intentionality will improve how well a tool performs for the users. Now, I think an important distinction is between answering 'why' a particular implementation is necessary, or why the change was made, versus a better understanding of user goals. User goals describe 'what' the tool should satisfy, while design-rationale is answering 'why' a certain change is being made.

The authors present four possibilities for 'why' questions having such low representation:



	
  1. the information is perceived to be unimportant or avoided by people conscious they are not domain experts;

	
  2. these questions _are_ important, but these meetings are not the venue for addressing them, or the context is clear to the participants;

	
  3.  'what' and 'how' questions provide enough information to elicit or understand the 'why' questions;

	
  4. it is hard to answer these questions with current tools;

	
  5. (least likely) while low in frequency, these questions are greater in importance: this suggestion seems unsupported by the data; e.g., the minutes didn't reflect that such questions are more important.


Another critique that can be made, in a similar vein, is regarding the outcomes of these projects-to-be. I would imagine that studying the design meetings of ultimately failed projects doesn't tell us much about what ought to be done in these meetings. Perhaps they focused to such a great extent on the implementation details that they omitted other important considerations.  However, the fact the paper has used three fairly distinct datasets strengthens the results considerably.

The paper concludes with an observation that usage scenarios are very important according to the data; this supports the agile focus on use cases and user stories.

All in all an excellent paper, grounded in empirical and externalizable data. The one regret I have is that (to my knowledge) the data is not publicly available. It seems like a rich source of data for a wide variety of questions. While I understand the privacy and IP problems involved, one would think that there is either a way to anonymize it, or that 10 years later, it would be of very little relevance.
