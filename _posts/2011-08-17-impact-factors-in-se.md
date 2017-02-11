---

date: 2011-08-17 14:54:42+00:00
title: Impact factors in SE
---

I confess to not understanding the [impact factor](http://en.wikipedia.org/wiki/Impact_factor) in software research. The impact factor for a given year (as used by [ISI](http://apps.webofknowledge.com/)) measures the mean number of times articles in the preceding two years were cited that year. So an IF of 5 for 2010 means on average, each article in 2008 and 2009 was cited 5 times in 2010.

In SE many of the journals I consider the most prestigious have declined in the past three years [1][2]. Consider:
<table border="0" >
<tbody >
<tr >

<td >**Journal**
</td>

<td >**2010**
</td>

<td >**2009**
</td>

<td >**2008**
</td>
</tr>
<tr >

<td >[ToSE](http://www.computer.org/portal/web/tse/)
</td>

<td >2.22
</td>

<td >3.75
</td>

<td >3.57
</td>
</tr>
<tr >

<td >[CACM](http://cacm.acm.org/)
</td>

<td >2.35
</td>

<td >2.35
</td>

<td >2.65
</td>
</tr>
<tr >

<td >[REJ](http://www.springer.com/computer/swe/journal/766)
</td>

<td >0.86
</td>

<td >0.93
</td>

<td >1.63
</td>
</tr>
<tr >

<td >[ToSEM](http://tosem.acm.org/)
</td>

<td >1.69
</td>

<td >2.03
</td>

<td >3.96
</td>
</tr>
<tr >

<td >[IEEE SW](http://www.computer.org/portal/web/software/home)
</td>

<td >1.51
</td>

<td >2.04
</td>

<td >2.10
</td>
</tr>
</tbody>
</table>


What exactly do I conclude from this decline? Let's keep in mind that IF is taking the mean of a non-normal distribution, and that the first destination for new research results is almost certainly not one of these journals. Rather, most of the journals tend to publish longer versions of conference papers, invited issues on special topics, and so on. Here are some stats from [my last publication](http://fink08.files.wordpress.com/2005/03/ernst-re2011.pdf):

Number of citations overall: **31**
Number of conference papers cited: **13**
Number of journal papers cited: **15**
Number of workshop papers cited: **0** (other: 1 thesis, 1 book, 1 ArXiv paper)
Ratio of venues for recent work [3]: 4/5 = **0.8**

A decline in IF means that the published papers are seeing fewer people refer to them. Then the question becomes, is that because fewer people are doing SE research, or that fewer people are citing journal papers? I think there are a few observations:



	
  * It is difficult to consider impact in a three year span. That assumes that your journal paper influenced people in the next two years. I'm not sure how many of these journals are read by people immediately. For my work, journal papers tend to be those which have shown to hold up over time, i.e. > 5 years. If I want to keep track of current research I cite papers from conferences. This is particularly true if I look at papers only in this area (since other fields tend to favour journals). My 0.8 figure means that of the citations for that paper, I cited 5 conference papers from 2008-2011 vs. four journal papers (all of which were in other areas than RE). Consider [this paper](http://www.springerlink.com/openurl.asp?genre=article&id=doi:10.1007/s00766-011-0129-9) by my colleague [Sotirios](http://www.yorku.ca/liaskos/). It was originally published in September 2010 as a conference paper. It has just now come out (September 2011) in a special issue of REJ. But I doubt I will update my citation strategy to cite his journal paper rather than the conference paper.

	
  * Survey journals (e.g. [ACM Computing Surveys](http://www.worldcat.org/title/acm-computing-surveys/oclc/40522608)) and musings on the future of the field should be excluded. By definition these are broad overview papers, which mean they tend to pop up in plenty of paper introductory sections. But they do not represent 'research' as such.

	
  * The other factor is diffusion. It may be that the frustratingly long review times and perceived low impact of these journals has contributed to a negative-feedback cycle. It is natural in an emerging science like software research for the community to seek out other venues and create new journals and conferences. Consider requirements engineering. This is a very diverse field which touches on economics, artificial intelligence, human-computer interaction, sociology and many others. It seems silly to think that a single venue could appeal to all researchers. Many of the papers in CACM, for example, are of very little interest to me - probably less interesting than the papers published in Nature. They are simply too technical and too different than my chosen community. I do not know the numbers, but I suspect that smaller venues like [MSR](http://www.msrconf.org/) and [CHASE](http://ieeexplore.ieee.org/xpl/mostRecentIssue.jsp?punumber=5061471), which I perceive as having garnered a lot of momentum, have seen increases in impact.

	
  * And the _elephant in the room_? The fact that none of these venues makes it easy for people to a) find the papers and b) actually read them. For example, for the longest time just getting a list of recent papers was impossible with any IEEE journals. I subscribed to a RSS feed that always had an error when you tried to link through to the paper. It just isn't acceptable that publicly-funded research is this difficult to access. Impact factor in the large should be about more than just influence on other researchers. We should consider blog posts, software tools, and especially data repositories.


[1] [http://www.cse.chalmers.se/~feldt/advice/isi_listed_se_journals.html](http://www.cse.chalmers.se/~feldt/advice/isi_listed_se_journals.html)
[2] [Diomidis Spinellis's blog post on IF
](http://www.spinellis.gr/blog/20110731/index.html)[3] Number of citations in the past 3 years from journals over the number from conferences.
