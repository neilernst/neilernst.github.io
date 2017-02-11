---

date: 2007-08-20 01:28:08+00:00
title: Grok, graph patterns and scenarios
tags:
- grok
- reading
- scenarios
- software
---

`@inproceedings{wu_using_2002,
address = {Paris, France},
title = {Using Graph Patterns to Extract Scenarios},
url = {http://swag.uwaterloo.ca/\~j25wu/papers/iwpc02-wu.pdf},
booktitle = {International Workshop on Program Comprehension},
author = {Jingwei Wu and Ahmed E. Hassan and Richard C. Holt},
month = jun,
year = {2002},
pages = {239-247}
}`

[Grok](http://swag.uwaterloo.ca/~nsynytskyy/grokdoc/grokintro.html) is a tool from [Waterloo](http://swag.uwaterloo.ca/) that can do algebraic manipulations of graph structures. In this paper, the graph structures are source code relationships like 'calls' or 'uses'. They first extract 'scenarios' from the software model, which seems similar to my desire to extract high-level goals from requirements specifications or documentation. Again, the challenge is a reconstruction one, and seems very similar to [software histories](http://www.neilernst.net/pubs/#workshop). Since we don't have access to the decisions and thought-processes at the time of design, we must reconstruct these (albeit imperfectly) from original documents. Although imperfect, it isn't much different than a historian analyzing Napoleon's decision to [attack Russia](http://en.wikipedia.org/wiki/Napoleon's_invasion_of_Russia) in 1812.

Source code extraction has better fidelity. After all, most version control systems allow you to checkout code from a specific date, preserving perfectly the state of the software at that point in time. However,  this can only ever reproduce the facts on the ground at that point in time (e.g., bugs, design, architecture) but not what is, in my opinion, the more interesting rationale insights (why this design?).  Similarly, we know Napoleon ended the invasion with massive casualties -- but have to settle for reasonable estimates as to why this disaster (or triumph) happened.

The target system here is Gnome's Nautilus. The authors first generate facts about the source code, then  manipulate this  'factbase' with Grok in order to produce something that can be used for architecture recovery. Using this knowledge, they then generate scenarios (e.g. interprocess communication via CORBA) and then validate with facts extracted. There seems to be a certain degree of 'find the facts which fit our scenario', and one has to wonder to what extent the extraction process was 'massaged' to produce the graph that supported the scenario. Perhaps a more reasonable approach would have been to use a portion of the code to generate the patterns, and then search the remainder for similar matches (supervised classification). I think this issue is a common one in software engineering science. The Grok pattern matching extension seems very similar to the RDF query language [SPARQL](http://en.wikipedia.org/wiki/SPARQL).


<blockquote>[One problem] was identifying a useful set of scenarios, because substantial knowledge about the important tasks of the system were required. Our experience showed that such knowledge could be accumulated during architecture extraction. In our analysis, the trial-and-error method was applied to extract useful scenarios. We carried out many iterations of defining patterns before we got useful matches. (p. 8/9)</blockquote>


The ability to query a factbase is very powerful, especially as a precursor to generate visualizations. In general, with large knowledge bases, it is silly to merely generate a large graph visualization without first manipulating the data to support user-defined queries. This paper confirms the utility of a graph-matching approach to pattern extraction, but highlights the difficulty that remains, namely, gaining sufficient understanding of the system to be able to pose lucid queries.
