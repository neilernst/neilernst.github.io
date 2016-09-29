---

date: 2014-06-13 13:34:46+00:00
layout: post
title: Software research shouldn't be about the tools
tags:
- complexity
- IT
- semantic web
---

It comes down to [essential vs. accidental complexity](http://en.wikipedia.org/wiki/Accidental_complexity), as outlined by Fred Brooks. What we research is new ways to 'nibble' at the accidental complexity: new languages ([GO](http://golang.org/), [Swift](https://developer.apple.com/swift/)), new abstractions ([Actors vs. functional programming](http://pchiusano.blogspot.com/2010/01/actors-are-not-good-concurrency-model.html) in distributed systems), new methodologies (random test case generation). It's what nearly every story on Hacker News is about.

But ultimately, I think most problems come down to two factors: the problem complexity itself, and the team tackling it. To me, many of the problems highlighted as software/IT failures, like the [FBI registry](http://www.washingtonpost.com/wp-dyn/content/article/2006/08/17/AR2006081701485.html), have nothing to do with a lack of good tools or techniques. These are ultimately management failures: scope creep, poor leadership, insufficient budget, too much budget, negative work environments, etc. It is ['executing'](http://www.nationalpost.com/news/story.html?id=2624855) that is the problem, not the technology. How many errors have been caused by the US reliance on imperial units?

Look at this [quote by a senior VP at Oracle](http://feedproxy.google.com/~r/zdnet/projectfailures/~3/QamQZg86wi0/) on failures in implementing CRM projects:



<blockquote>[M]y comments apply to ALL CRM vendors, not just Oracle. As I perused the list, I couldn’t find any failures related to technology. They all seemed related to people or process. Now, this isn’t about finger pointing, or impugning customers. I love customers! And when they fail, WE fail.</blockquote>



I'd be willing to say that software engineers have all the tools they need. We need some form of continuous integration and deployment, abstraction mechanisms to simplify the problem, tests to verify our solution, version control to maintain a history of changes, and some form of requirements (whiteboard, paper, spreadsheet, what have you) to keep track of what needs to be built. I don't even think it particularly matters how you use those tools. If you have a mature organization and process then you can all into the following matrix (James Montier via [Jonathan Chevreau](http://opinion.financialpost.com/2010/03/11/how-investors-can-avoid-being-their-own-worst-enemy/)):

<table >
<tbody >
<tr >

<td >
</td>

<td >**Good Outcome**
</td>

<td >**Bad Outcome**
</td>
</tr>
<tr >

<td >**Good Process**
</td>

<td >Deserved Success
</td>

<td >Bad Break
</td>
</tr>
<tr >

<td >**Bad Process**
</td>

<td >Dumb Luck
</td>

<td >Poetic Justice
</td>
</tr>
</tbody>
</table>

But just having the right tools, the good people, and a mature process is not enough to guarantee success, of course. You could be tackling a '[wicked problem](http://en.wikipedia.org/wiki/Wicked_problem)'. You could have a team of misfits and losers. You could have a manager who refuses to accept responsibility or make decisions. Most software research does not address those issues. I'm not convinced there is any research that addresses those issues: leadership, management, sociology... nothing can help when your team lead is having a marital crisis and can't devote any time to product development.
