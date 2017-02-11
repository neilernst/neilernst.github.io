---

date: 2010-01-11 17:00:27+00:00
title: A better scientific notebook
tags:
- msr
- r
- science 2.0
- workflow
---

[Cameron Neylon](http://friendfeed.com/cameronneylon) is an [advocate of open science](http://blog.openwetware.org/scienceintheopen/) (along with others like [Michael Nielsen](http://friendfeed.com/michaelnielsen)). Among other things, open science or Science 2.0 means keeping track of your mundane day-to-day activities (I like to call it "sciencing") using some publicly accessible repository. This way other researchers (your competition?) can see what you are doing and comment/question/improve your work.  This also has benefits for the researcher herself, of course, in keeping track of what steps were followed. Nothing is worse than getting a good result and not being able to replicate it ("I swear it was there! I saw it!" "Yes of course you did, here, just take this pill.."). Actually there is something worse and that is losing data and not having a backup. Like me.




Recently I was working on an project - [MSR/data mining of open source software](http://neilernst.net/tag/msr/) - and saw one aspect of this that could be improved. I'm working with [R, the open-source statistics toolkit](http://www.r-project.org/) to do data analysis. I've never used it before, so there's a fair bit of reading the manual, copying/pasting of examples, and experimentation involved. This can be dangerous: am I selecting a result from my analysis just because it "looks right", or because I really understand what the analysis is saying? I am also going to want to repeat what got the particular graph I end up with (e.g., change my numeric yearweek dates to R date objects).




Helpfully R has a command line history you can store in a '[workspace](http://www2.warwick.ac.uk/fac/sci/moac/degrees/modules/ch923/r_introduction/workspace_scripts/)'. But one thing I would like to be able to do with this, and any command line environment, is to somehow identify the _key_ commands. For instance, I modify an online example to [plot a regression line](http://www.cyclismo.org/tutorial/R/linearLeastSquares.html) for my data. I would like to somehow send that command to a "repeatable steps" repository to preserve a sense of  useful workflow (not just history). The vanilla history typically has a lot of missteps, and going back through it can be a challenge. To make this tool even better, it should somehow parse out the dataset-specific pathnames and variable names. Then I would be left with something like:



[sourcecode language="matlab"]
> <data.frame.variable> <-  read.csv(file="<csv file name>",head=TRUE, sep=",")
>summary(data.frame.variable)
>data.frame.variable$<index column> <- sequence(nrow(data.frame.variable))
> <dates.variable> <- strptime(as.integer(data.frame.variable$dateweek.variable), "%Y%U")
> plot(dates.variable,data.frame.variable$<values.variable>[/sourcecode]

Which would allow me to insert my own variable definitions (a meta-language, I guess) and have that run automatically as a script in R.
