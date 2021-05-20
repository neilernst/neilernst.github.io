---
date: 2020-09-30 
title: Running a Mining Challenge Using Kaggle
---

For the [2nd edition of the Dynamic Software Documentation (DysDoc) workshop](https://dysdoc.github.io/docgen2/), the organizing team wanted to push the boundary on how to engage the community in tool supported demos. Previously, we had asked participants to come to the workshop (co-located with ICSME) with a tool to demo, live, to the other attendees. One of the goals was a tool that worked on unseen data. 

This year, at our organizing meeting, we wanted to try something that went beyond documentation generation, and looked at other issues with dynamic documentation fixes. [A study by Walid Maalej and Martin Robillard](https://cado.informatik.uni-hamburg.de/coding-guide/), which looked at types of API documentation, included an interesting issue with documentation - code comments - that were uninformative. 

```java
/** 
 *  Clears the log
 */
public void clearLog() {
  LogMessages.getInstance().clear();
}
```

This comment is clearly not adding information to the code, and in fact, might even be harmful, if it were to be outdated. Thus our "Declutter" Challenge: figure out a way to identify these type of comments and (eventually) target them for removal. I was co-organizer alongside [Nicole Novielli](http://collab.di.uniba.it/nicole/). 

We were inspired by the success of datasets and benchmarks such as Fei Fei Li's [ImageNet contests](http://image-net.org/challenges/LSVRC/2016/index), or the [SAT competition](http://www.satcompetition.org). Both of these have been influential in driving innovation in graphics and satisfiability solving. As it turned out, these distributed competitions were also ideally suited to the new remote work paradigm that was required during the COVID pandemic. 

To set up this competition, there was the option to have the competitors take the dataset, work on a solution, then submit their solution to the organizers for evaluation. Of course, this involved a lot of work on the part of the organizers, and being fairly lazy, I looked for an alternative approach. Immediately the Kaggle competition platform seemed the way to go: it has been hosting large-scale data science competitions since before there was data science. 

I therefore investigated how this could work. Normally, [hosting Kaggle competitions](https://www.kaggle.com/c/about/host/) require payment (commercial) or prizes (academic). Academic contests are also selected by Kaggle. Fortunately, Kaggle makes the platform available for classroom use, on [Kaggle InClass](https://www.kaggle.com/c/about/inclass). The difference, other than no support, is that competitors do not get Kaggle points for entering. Nicole and I thus decided to use Kaggle to host the Declutter challenge, which you [can find here](https://www.kaggle.com/c/declutter20v2/leaderboard).

# What Worked

Despite lacking support, getting the contest going on Kaggle was fairly simple. Nicole organized labeling with the rest of DysDoc's organizers, and hosted a gold [set on Github](https://github.com/dysdoc/declutter). I then used the gold set to generate the inputs Kaggle wanted. This includes the gold set, split into training and test. Test data is further split into "public leaderboard" and "private leaderboard", since competitors can submit multiple entries, and see where they stand on the leaderboard. Only the organizers get to see the private leaderboard, which is what ultimately ranks the competitors. You can see that [in practice here.](https://www.kaggle.com/c/declutter20v2/leaderboard)

I also had to choose between Kaggle's available validation metrics, in this case choosing F1, and this can be a bit finicky, as you have to map between the columns in the solution CSV file and whatever Kaggle's automation expects. Clearly at paid support levels they would make this simpler, or just do it for you.

Despite not having a lot of labeled data, we managed to get a good set of data, and Kaggle's infrastructure worked - as far as I know, anyway! - with no problems. Competitors download the data, run their model, and then upload a solution file with their predicted labels. 

We managed to get 2 principal competitors, one of whom submitted several distinct entries. Both entrants published their submissions at our workshop, which can be found at the ICSME proceedings site. 

# Improvements and Questions

I was quite happy with how simple Kaggle made the process of evaluating entries. It also scales flawlessly (unlike me), and in theory, could help us dramatically expand our contest. In the COVID era, of course, it also made it pretty easy to host a remote contest, unlike our previous approach, which used in-person demos.

It would be nice to have more support for notebooks, or perhaps a mandatory notebook submission, so that we can see how each group approaches the problem (after it finishes of course). 

As far as I am aware, this is one of the first challenges to be hosted on Kaggle. To me it seems like an obvious choice for running and hosting automated benchmarks, such as the various effort estimation and defect prediction datasets out there. If we could disambiguate entries, that would help with understanding *who* is entering.

Kaggle makes it possible to host an ongoing, never-ending contest, which is also appealing. The obvious bottleneck, unsurprisingly, is data annotation, and at this point I would say that is the main obstacle to running more such contests. However, we have tentative plans to continue the approach in future workshops.  