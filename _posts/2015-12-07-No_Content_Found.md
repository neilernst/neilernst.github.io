---

date: 2015-12-07 14:58:12+00:00
layout: post
published: false
title: Requirements, Agile, and Finding Errors
---

It’s a long held view in the requirements engineering (RE) community that “if only we could do RE better, software development would be cheaper”. Here ‘doing RE better’ means that your requirements document adheres to some quality standard such as [IEEE 830](http://www.math.uaa.alaska.edu/~afkjm/cs401/IEEE830.pdf). For example, none of the requirements are ambiguous.

One justification is that, based on (very few) studies in the late 80s, requirements errors cost a lot more to fix in test/production than when they are incurred. For instance, if I tell a subcontractor she has a 100 kilobyte message size limit, and I really meant 100 kilobits, fixing that problem after she has delivered the subcomponent will be expensive. This seems obvious. But two problems emerge. 1) Why does she have to wait so long to integrate the subcomponent? 2) how many of these problems are there? Granted it is cheaper to fix _that particular error_ in the requirements/system engineering phase, how much money should we spend to find these errors at that point? [[1]](1)

An interesting early experiment on this is described in Davis, 1989, [“Identification of errors in software requirements through use of automated requirements tools”](http://dx.doi.org/10.1016/0950-5849(89)90145-6), Information and Software Technology 31(9) p472–476. In an example of an experiment we see very rarely these days, his team were given sufficient funds to have three automated requirements quality tools applied to a large software requirements specification for the US Army (200,000 pages!). The tools were able to find several hundred errors in the spec, including errors of inconsistency. Yay, the tools worked! But….

The program had decided to go ahead and build their (Cobol) system before the automated analysis. The developers on the program didn’t care much about the findings. 80 of the 220 modules were not detectable in the final system (meaning, presumably, they were either merged or omitted altogether). Davis did some post-delivery follow-up, showing that the modules with greater numbers of requirements problems had a significantly greater number of post-release defects. But whether the two are causally related is hard to say (those modules may simply be more complex in general, so both requirements and code are harder to get right).

What I conclude from this is that finding errors of the sort they did, e.g.,



<blockquote>PROBLEM: the referenced table directs that PART_NO be moved from the WORK_ORDER_FILE to the WORK_TASK_FILE. Available fields in the WORK_TASK_FILE include PART_NO_FiELD_PART and PART_NO_FIELD_TASK.

CHOICE: We assume that PART NO FIELD_TASK is the proper destination.</blockquote>



are ultimately of zero value to document. As a result, finding problems with them, automated or otherwise, is also of no value. Of course we know all this from the past 20 years of the agile movement, but it is interesting to see it in action. I think that (in 1989 certainly) this was excusable, as the program managers had no good sense of what made software special. The level of detail the design describes, down to field names and dependencies, is better suited to the Apollo program, where they prescribe how tightly to turn bolts, label each individual bolt, etc. Which makes sense in a safety critical dynamic environment, but not a lot of sense in an office logistics tool.



# Going Forward



A term I loathe but seems better than “Future Work”. I’ve worked a lot on automated requirements tools like PSL/PSA or SREM, so where should we head with automated tooling for requirements?

There is a lot of empirical evidence that simple, easily integrated process patterns such as requirements goals and scenarios lead to higher quality requirements. Intel, for example, are strong believers in training staff in [writing good requirements](http://selab.fbk.eu/re11_download/industry/proceedings-short-papers/RE2011SIP003.pdf) (although notice their domain is also hardware-oriented and mistakes are costly). Even in agile settings I believe there are big improvements to be gained in writing better user stories (e.g., how to create the “Magic Backlog” described in [Rebecca Wirfs-Brock](https://twitter.com/rebeccawb/status/673301475162918912)’s EuroPLoP 2015 paper).

Furthermore, we are seeing more and more use of machine learning to flag requirements problems. For example, at Daimler they have [simple detectors for checking requirements](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=7320451). And at Rolls-Royce, based on simple training exercises, they [label requirements based on potential risk](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=6051622), combining uncertainty, change impact and cost into an index. All of these types of tools integrate will into a developer analytics approach, able to populate dashboards and flag things unobtrusively (compared with the cost of writing requirements formally).

Like with any analytics techniques, which ones to apply is situation-specific. [Small companies doing the same things in well-understood domains](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=4384165) won’t need much, if any requirements analysis. I think there is a lot of room for intelligent augmentation of what makes a good requirement, that facilities conversations and discovery of uncertainty, that automates the repeated and boring tasks (if you cannot possibly avoid creating a 2000 page document …). And in specialized domains, we are moving to a world where more and more of the analysis can be done in models, to verify timing requirements, guarantee that software partitions hold, and so on. Here the line between ‘re quirement’ and ‘design solution’ is blurry: if I apply my



# Finding Defect Leakage



A major goal for large programs is to reduce defect leakage, the number of bugs that make it to production (to put it more precisely, reduce the number of _critical_ bugs that make it to production). It seems to me there are at least three approaches to this issue:




    
  * We could do this manually, and insist on writing good requirements using checklists and training, inspection, ets.

    
  * We could do it automatically, and run machine learning tools on past artifacts and try to leverage experience to predict problems. Not every requirement is equally important (obvious but not always followed).

    
  * We could design a process that accepted the inevitability of change and made it not only possible, but desirable to change design and requirements in response to new knowledge.



For the automated tools, I have this quick list of principles. Much like software analytics in general:


    
  1. **Don’t make life worse.** Developers should not dread having to do this. That said, an ounce of pain is worth a pound of pleasure.

    
  2. **Work with existing tools like Doors, Jira and Excel**. Your Eclipse plugin does not count.

    
  3. **Don’t mandate new or complex languages or tools for requirements**. We can barely get engineers to write requirements in natural language as it is.

    
  4. **Prefer lightweight, high value checks over complex, theoretically appealing ones**. Socialize people to the value of checking _anything_ before insisting on the complex stuff.

    
  5. **Integrate with existing dashboards like Shipshape or SonarQube.** These tools have good plugin frameworks and already integrate with many build and CI servers.

    
  6. **Facilitate conversations and early delivery of results**. Remember that requirements engineering is the start of a conversation that gets us to a valuable solution. It is never an end in itself. In very few domains does assuming requirements won’t change get you anywhere.









* * *






    
  1. And [Basili and Weiss’s 1981 study](http://portal.acm.org/citation.cfm?id=800078.802544) on the A7 program’s change requests and requirements suggest a power-law distribution to the most costly (e.g., > 1 person-month of effort) changes. [ ↩](1)



