---

date: 2012-04-26 19:31:37+00:00
layout: post
title: 'Using GitHub for 3rd Year Software Engineering  '
---

This past semester (Winter 2012), I was the instructor for UBC’s [CPSC 310: Introduction to Software Engineering](http://www.ugrad.cs.ubc.ca/~cs310/). As part of the course, students must complete a large-scale software project in teams of 4–5 in 2 months. This term, I allowed some teams to use GitHub to manage the project.





## Reasons


At UBC, we have for some time used IBM’s [Rational Team Concert](https://jazz.net/projects/rational-team-concert/) tool, which is free for academic use, as our software collaboration environment. This was the default tool for this term, as well, save for the three groups who applied to use GitHub. The University of Victoria has been using [RTC for a similar purpose](http://adrian-schroeter.com/2011/11/30/resources-for-using-jazz-in-a-student-course/).

RTC is, I’m sure, an excellent product for its intended audience, namely, professional software development teams. It is easy to install and maintain for the technical support staff here, has sufficient documentation, and clients for Mac, Linux and Windows. It is also free for us to use as part of the IBM Academic program. However, in course evaluations, it has been the single most complained-about part of the course. It is cumbersome to install for students, and most importantly, always seems to be out-of-date with other software. In our case, RTC 3 is built using Eclipse 3.4, which is “somewhat” incompatible with the libraries and plugins I was looking to use, chiefly the Google Plugin for Eclipse. A significant amount of course time (TA and instructor office hours) was spent getting RTC to work with the other software for the course. And I am just seeing that IBM is now working on [RTC 4](https://jazz.net/blog/index.php/2012/03/07/announcing-the-clm-2012-beta/), which implies more trouble in the future.

Now, this is partly because students have not had much experience installing commercial development tools on their machines, and that is certainly a learning objective for this course (I am confident it is a pain point for nearly all software developers, new or otherwise). It is also because students run a bewildering array of operating systems and language profiles on their laptops and desktop computers, which makes support a headache.

That being said, my sense was that RTC was simply too much tool for what the students needed. As Greg Wilson’s [DrProject experiment](https://stanley.cdf.toronto.edu/drproject/drproject) showed, students simply do not have time, nor inclination, to leverage the more powerful collaboration aspects. Filling out work items, creating documentation, even committing code is something they just do not see the need for. To get them to try it, we must assign marks to those activities. RTC’s terminology (streams, components, etc) is probably great for a developer with multiple projects: for these students (and me!) it is non-standard with most version control concepts and confusing to use.

Since [I’ve personally used](https://github.com/neilernst) GitHub for a while, and `git` seems to have a lot of developer mindshare, it seemed like a good fit for an experiment.


## Experiences




### Instructor


I emailed Github about the use of their web app for education and received a very prompt affirmative. Github will provide an organization account to the instructor, which includes private repositories for up to 200 people. At the end of the semester, they then require you to either delete the repositories (on Github, obviously not locally) or make them public (free accounts).

The Github UI is generally simple, but some of the navigation options are confusing from the team manager point of view (me!). Tracking student performance is pretty easy, since you have ready access to the excellent Github website, including issue tracking, change set tracking, pull requests, etc. Github has excellent graphs that allow the instructor team to check who is doing what. There doesn’t appear to be a good way to email all of the students in the various teams at the same time ([we are an “organization”](https://github.com/organizations/CPSC310W2012) made up of 4–5 person teams).

Git itself is the main reason to use Github. There are vastly superior tutorials on it, and I like the pure distributed model better than what RTC provides. Finally, and perhaps most important, as the instructor I’ve used Git a fair bit and RTC very little. The disadvantages are that there is no central repository for backup purposes, although being distributed this is presumably less important.


### Student


Students were generally positive. The alternative, in this course, was to use RTC. Git has the advantage of more widespread adoption (you’re unlikely to use RTC at Microsoft, but MSFT supports Git in various places). And of course, if Github goes down, then students can no longer manage issues. Git itself is complex to learn; I should have provided a short tutorial to those teams on the basics of Git.

They also found tools like [SourceTree](http://www.sourcetreeapp.com/) and [Tortoise](http://code.google.com/p/tortoisegit/) invaluable in understanding what was happening with branches and remotes. For a while, a few teams had multiple, non-merged and conflicting branches for each member, which they could resolve once they saw visually how the branches were happening. The concept of remote repositories and pull requests is a little alien at first.

Issue tracking in Github is primitive relative to RTC. This is a strength for this course, I feel, but when we go from user stories to tasks it means students had to roll their own classification scheme (e.g., define a product backlog item, then the tasks which compose it).

The teams which used Github were much stronger than most other teams in the course, so the results are no doubt skewed. That being said, I don’t think RTC was any simpler to use—in a number of teams, at least one team member never managed to commit code to the shared repository.


## Looking ahead


The obvious question is, “Would you use Github again”? The answer is _yes_, and perhaps even “I would like to make everyone use it.”

It was confusing to have two separate tools in the course. Partly, this is because marking is complicated by the fact student teams are in tutorial sections, so some teams in a given tutorial were using Github and some RTC. This meant TAs had to mark both tools (and learn both). Exam questions are more complicated, since you must account for some students never having used RTC, if you ask about issue tracking.

I like the fact that the project collaboration tool was separate from the IDE. I think RTC’s tight Eclipse integration makes it difficult to install the IDE necessary. Some students ran Eclipse 3.7 in conjunction with RTC (Eclipse 3.4) in order to get plugins working. Since `git` is so popular, it is much easier to find tool support for it than to munge RTC into your work flow. In future, tools like [Mylyn](https://github.com/blog/852-github-mylyn-connector-for-eclipse) would be useful to better integrate issue tracking into the IDE.

The big outstanding issue is privacy. In BC, the provincial government is considering laws that prohibit (or seem to, IANAL) student data being anywhere near a US server (despite students happily sending email about their marks from Hotmail or Gmail). While I respect that motivation, I feel there should be some way to give consent, particularly when so many excellent tools are US-based.
