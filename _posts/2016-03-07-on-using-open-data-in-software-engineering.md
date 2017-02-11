---

date: 2016-03-07 20:56:41+00:00
title: On Using Open Data in Software Engineering
---

I recently reviewed [data showcase papers](http://2016.msrconf.org/#/data) for the Mining Software Repositories Conference, and I’m co-chair of [the Engineering track](http://www.ieee-scam.org/2016/#engcall) (subsumes datasets, tools, approaches) for the SCAM conference[^1]. I’ve worked with a number of different datasets (both openly available and closed) for my research efforts. This caused me to do some reflection on the nature of empirical data in SE.

We’ve had a nice increase in the amount of data available for researchers to explore, and most recently, the amount of well-constructed, easily understandable and accessible datasets – like the [GHTorrent tool](http://ghtorrent.org) – is impressive (traditionally it has been difficult to get any credit for creating these resources). I think it is a hugely beneficial effort for our efforts to create a well-grounded, empirical basis for software engineering (as opposed to [pie in the sky theorizing](http://semat.org)).

I have two concerns that threaten this idyll.

### Concern 1: long term availability and replication

Other fields, primarily psychology and economics, have begun [painful self-examinations](http://www.slate.com/articles/health_and_science/cover_story/2016/03/ego_depletion_an_influential_theory_in_psychology_may_have_just_been_debunked.html) of well-cherished, supposedly well-grounded results. In many cases replication of these findings is very difficult. What worries me most is that in empirical SE, we aren’t even in a position to attempt to replicate key findings, because (among other concerns) the original datasets aren’t accessible. This is most often because studying companies is usually caveated with “but you can’t tell anyone it was us”; other problems include datasets that are ‘live’ and self-modifying (for example, publishing a study on foul language in commit histories might mean those histories are modified), or just out of date entirely.

I propose two solutions. The first is to use long-term archiving approaches. This means no personal university website, no special database formats, no ‘email me for access’. The open access/open research communities have been tackling this problem for several years, and good solutions exist (like identifiers from [DataCite](https://www.datacite.org/about-datacite/what-do-we-do) or hosting like with [Felienne](http://felienne.com) Hermans’s [Figshare](https://figshare.com/authors/Felienne_Hermans/98650)). We have software specific repositories as well, of which [the Promise repo](http://openscience.us/repo/) is the one I know best. [The 2016 CHASE workshop](http://www.chaseresearch.org/workshops/chase2016) encouraged authors to stick papers on ArXiv, but the data should be similarly archived. One problem here is how to store data that institutional review boards might insist be destroyed.

The second is how we cite the data when we publish it in a journal or conference paper. I’ve seen URLs in the body of the paper, standard reference lists at the end of the paper, footnotes, and comments in the author’s notes. We need to standardize this so readers can quickly and easily find the URL to the dataset. My suggestion is to add a separate heading, like the useless ACM keywords, referencing any new datasets used/available, immediately after the abstract.

### Concern 2: new ethical questions
My second concern is one I only recently realized (somewhat shamefully), and this is the ethics of publishing data. This was prompted by [the GHtorrent debate](https://github.com/ghtorrent/ghtorrent.org/issues/32#issuecomment-189552452). There the central objection from (some) developers was that their email address was accessible, perhaps more easily accessible than on Github. Email is an obvious one, but beyond that I think we need to acknowledge that the mental model of a developer pushing code to Github (or wherever) is not one of public visibility. The silly comments they write (“huge HACK!”) could be career-limiting, and pushing that dataset out into the world is a question we have to tackle. My view would be to explicitly include terms of use in data you make available, and [Georgios](http://www.gousios.gr) is obscuring identities (e.g. with a SHA1 hash) when asked.

More broadly, the world of SE analytics opens up the chance that the data could be used for purposes we might not understand. For instance, one might show that a particular Chromium developer has an unusually high number of bugs. As researchers we might understand the nuances and limitations of how the data was collected[^2]. Managers might not understand the limitations, however. Furthermore, any data one collects is subject to subpoena and other legal requests, so in many cases immediate destruction is the best course (see the debate on sociology notes).

The big risk from NOT considering this is losing the goodwill of a community that only tangentially understands what software engineering research is. I’m not advocating for doing whatever developers tell you to[^3]; I am saying that not considering these issues risks antagonizing the people we are trying to help.


[^1]: Submit early, submit often!

[^2]: [Jorge Aranda’s](http://cuevano.ca) [‘secret life of bugs’](http://www.cs.toronto.edu/~jaranda/pubs/secret.pdf) paper sheds light on this.
    
[^3]: You put your freaking email on Github! What did you expect!? (sigh)


