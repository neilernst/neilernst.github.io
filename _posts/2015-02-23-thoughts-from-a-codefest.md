---

date: 2015-02-23 13:23:40+00:00
layout: post
title: Thoughts from a CodeFest
---

This past weekend was the [Steel City Codefest](http://steelcitycodefest.org/). The idea is that community non-profits present some problem for which an "app" would help them, and coders spend 24 hours coming up with some solution. It was a lot of fun. You can see our team's solution at [http://citipark.herokuapp.com](http://citipark.herokuapp.com). Our challenge was to create an easier way for people to find the city of [Pittsburgh's GrubUp food program](http://pittsburghpa.gov/citiparks/summer-food-service), which offers free lunch and breakfast at 80+ sites around the city in the summer (sadly, a lot of Pittsburgh youth are food insecure).

[caption id="" align="aligncenter" width="402"]![](https://pbs.twimg.com/media/B-Z1ipnIIAAXvyo.jpg) Me and my teammate Monica starting off Saturday morning.[/caption]

We didn't win the challenge, but I learned a lot on the way.

We created tons of  **technical debt** : code clones, code comments, no testing, no design. It was code as fast as possible, get it working, fix the obvious user facing bugs. We shipped. But even during that 24h span the design hit us, as it became harder to change things since logic and UI were wrapped together. Even something as trivial as renaming a media folder became a massive headache. We had no tests, so any change had to be "tested" by running the app and running through a few scenarios. Error handling was likewise left for later work, so if faulty input was entered the whole thing crashed.

It took a long time simply to do **infrastructure setup:** what Github repository, what web host, what database, how do we communicate together. Part of it was this was only my 2nd time building a [node](http://nodejs.org/) application, so I was unfamiliar with its internal expectations and capabilities. Things like "don't send headers twice" caused problems for me that a more experienced developer would not have had. In a 24h period this stuff needs to be like riding a bike, so deciding on a framework that I had little experience in was costly. It's like going to a marathon without having trained at all.

We were three people: two coders and a designer/QA person. Three was the minimum, and it really wasn't enough. There were tasks like entering data into the database (the Citiparks staff provided excel spreadsheets) that took me a few hours but had zero payoff. In a codefest, data quality is not a factor in the judging (the judges don't come from the clients). In an enterprise situation, the data is probably as important as anything else, but here it was wasted effort, and sample data would have worked fine.

We had somewhat of an idea how things would work, but wireframing it beforehand, and being much clearer about what steps were necessary, would have been better (you could not write code before, but this sort of sketching was allowed). A **simple design plan** and backlog would have been easier to work off, and help to resist the temptation to simply start hacking away. A number of times I would push back from the table, and say to myself "do I even need to do this?"

Writing code this way is a great way to learn these lessons. I have a number of academic publications about finding requirements, for example, but it is only when you do it yourself that you realize how much is lost between the quick IM conversations you have with teammates and the actual issue tracker. I do wonder, however, if these 24h codefests promote 'code first' over the value of design. For example, my sense is that a lot of what we did simply wouldn't work in an enterprise environment: there are design guidelines, authentication, security, data integration, lifecycle maintenance concerns, none of which you have the luxury to spend much time with. The cool thing about the Steel City event, however, is that the organizers do make a series of $10k grants available, in order to take the app to a more integrated and polished version.

It was a great event - very well organized, with great food and volunteers. And the Citiparks staff were amazing, sending their director and deputy director to do user testing at 7pm Saturday, and bringing amazing treats for us twice during the event. It also focused on an underserved area, in my view: social justice and not-for-profits. Many have quite simple needs, that in many cases amount to adding data to a Google Map, but even that is beyond their budgets.
