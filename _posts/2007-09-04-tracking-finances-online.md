---

date: 2007-09-04 03:08:59+00:00
layout: post
title: Tracking finances online
tags:
- bank_statements
- budget
- finance
- money
- public_api
- wesabe
---

I used to slavishly enter bank transactions (credit card purchases, online payments, etc.) into [Microsoft Money](http://www.microsoft.com/money/default.mspx) (and before that, Quicken). But the product isn't that impressive. It feels like being on the Money team at Microsoft is where careers go to die - there haven't been any substantial updates in years, the Internet is sort of tacked on, and the basics are cumbersome to manage.

Recently, I discovered [Wesabe](http://www.wesabe.com), a site that duplicates the register functions of Money. In other words, you can upload bank statements you download from the bank site, and Wesabe does a pretty damn good job of reconciling the various entries. I used to spend a lot of time worrying about getting the various accounts to balance to zero, but Wesabe's approach is liberal in what it accepts - all it concentrates on is getting the outstanding amount correct, which is really what's important. If I forget to include a 20$ grocery bill here or there, it isn't that crucial. You can tag transactions (rather than Money/Quicken's categories), and then generate spending/income reports for the various tags. Very slick, much better than the PC applications.

One thing I miss is a simple way to mark transfers between accounts. For example, if I pay my Visa bill from my checking account, I'd like that to show up as a transfer of money rather than income/expense. However, it's possible to exclude tags from reports, so this isn't a major issue.

The other feature I feel is really necessary is the ability to create a budget, and see how spending is tracking that budget. So far there aren't any good tools in Wesabe for that, although there are on other sites. What I'd like is the ability to set target amounts for tags per month, and then compare that with my monthly average. Wesabe does give you monthly averages, which is great, particularly when you have plenty of data for it to average. Since there is a public API, I can see tools being built to offer these services. For example, scan a user's data and identify anomalous spending, untagged spending, spending over 500$, etc. These reports, which Money does offer, aren't very prevalent. Yet.

Finally, Wesabe has an extensive community that offers tips and goal-sharing ('buy a house'). I haven't found the tips all that useful, but that's mainly because they are predominantly American, so the tips mention things like mortgage deductibility or strange American banks that aren't relevant in the 51st state. It's a pretty cool idea, nonetheless.

Another component of Money that I wanted to replace was the investing aspect.  Money had a kludgy way of managing investments using accounts and ledgers, and again seemed overkill for my simple needs. My main requirement is the ability to track all my investments in one place. For the longest time, it was easy to view stock prices online, particularly American stocks, but not Canadian markets or indices, mutual funds, [ETFs](http://en.wikipedia.org/wiki/Exchange-traded_fund), bonds, and so on. I'm still not satisfied completely, but [Google Finance](http://finance.google.ca) has recently added support for Canadian mutual funds and Canadian ETFs, which is great. Now I can see my portfolio performances pretty quickly ([which may not be a good thing](http://faculty.haas.berkeley.edu/odean/papers/returns/returns.html)).

There are still quirks. For example, there seems to be some issues converting from American to Canadian currency. Also, distributions aren't included, so the rate of return is net of distributions, which is very misleading for income funds or bond ETFs. I'm still not clear why this information -- how much money did my investments make for me last year -- is so difficult to obtain. To my mind, part of the work a broker ought to do is provide a simple quarterly report stating average rates of return, including distributions, tax implications, long-term performance, and so on. This has to be incredibly simple to provide, but my bank -- TD Waterhouse -- doesn't.  My assumption is that this is because they only provide this to investors who aren't cheapskates and go for a full-service broker. My experience is that most brokers are in business to make commissions selling product, and actually helping clients is a secondary consideration.
