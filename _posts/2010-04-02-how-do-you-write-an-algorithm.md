---

date: 2010-04-02 17:25:11+00:00
title: How do you write an algorithm?
tags:
- fmri
- problem complexity
- rspec
- tabu
---

It would be interesting to see how different people went about implementing a solution to a particular well-defined yet complex problem.

For example, I'm trying to encode a version of [Tabu search](http://en.wikipedia.org/wiki/Tabu_search) for a particular domain. I have the generic Tabu idea – tabu list, random choices, periodic restarts – but now have to apply that to the specifics of the problem. As we know, these implementations can vary greatly depending on constraints such as the data structures that are already in the solution.

What I've done is start with the pseudocode from [various](http://www.ifi.uio.no/infheur/Bakgrunn/Intro_to_TS_Gendreau.htm) [publications](http://books.google.ca/books?id=mFYt0C5cqtAC&printsec=frontcover&dq=tabu&source=bl&ots=_8wkMbQPOd&sig=LeIrQqNAW_PBSKz_kOi6hnWsvEc&hl=en&ei=vyS2S8nsM4H88Aaa1pTYAw&sa=X&oi=book_result&ct=result&resnum=19&ved=0CFUQ6AEwEg#v=onepage&q=&f=false) on Tabu, and some of the [projects](http://github.com/riobard/tabusearch) I've looked at. Then I immediately set out to code it all at once, get something working that I could try. That failed, in that I only got halfway before realizing I'd made some design decisions poorly. Do you think experts would not get stymied at this point?

My next approach was to write it out in the language of my domain, as opposed to the implementation language, and to generate a small set of test cases that would simulate the larger problem without confusing the issue of the actual algorithm. As an aside, I really like the Ruby [RSpec](http://rspec.info/) concept, where you write, in fairly natural language, what you are trying to do. Then iteratively fail until the spec is satisfied.

I think the problem with trying to write directly in code is that for complex algorithms (whatever your definition of complex is), I'm not sure you can easily grasp all the ramifications of your design. Probably some people are able to hold multiple cases in their head at once, and 'see' the solution. I would love to see a study looking at this question.

How might we test this? [fMRI](http://en.wikipedia.org/wiki/Functional_magnetic_resonance_imaging) comes to mind, although it may be of [questionable](http://en.wikipedia.org/wiki/Functional_magnetic_resonance_imaging#Disadvantages_of_fMRI) [statistical](http://www.edvul.com/pdf/Vul_etal_2008inpress.pdf) value. Simple IQ test questions might reveal something, but I don't know if IQ tests capture this idea of problem complexity. Code competitions probably come closest, but a) they don't capture the thought process well (although there are fascinating [screencasts at TopCoder](http://www.topcoder.com/tc?module=Static&d1=education&d2=overview)); b) I get the sense that the problem statements are a little divorced from truly complex domains ("solve the fox and the chicken problem without using recursion") – although I see they have a ['software  conceptualization'](http://www.topcoder.com/wiki/display/tc/TopCoder+Conceptualization+Contests) component.

We really want to see if the person can account for multiple possibilities at once. Chess might be a good model, as there are so many branches (maybe too many). The problem is really to achieve a single goal while conceptualizing multiple requirements for getting there.

Frankly, however, as an employer you might be better off with someone who may not have the same raw mental talent, but at least knows when he or she is beaten. Better to work it out in detail first then hack together a possibly faulty solution. At least that's my view (as someone who is not a _mentalist_). Not to mention it is by no means clear that building software requires the same skillset as maintaining (testing/securing) it.
