---

date: 2003-10-23 09:19:49+00:00
layout: post
title: More thoughts on evaluation
---

First, thanks to all the group members who attended my design co on Monday.  I received lots of feedback which was excellent.

Clearly, though, I have a lot of thinking to do.  My [initial approach](node/view/203) was overly simplistic, but it did get me thinking about what to do.  Here's what I gleaned from the discussion we had.

What would make me _happy _is somewhat complex, but I think the question is really, "How can you show scientific validation for what you did?"  This is challenging.  I think what a lot of software engineering theses tend to do is say, 

<blockquote>Here's my idea for improving system X.  I looked at its problems and identified some challenges for people using the system.  So I improved that system with the following techniques.  Next, I tested some people who have only a cursory interest in the tool to see whether my improvements were improvements, based on a selected list of tasks _I chose to show that they were improvements_.  So my improvements improved the tool!</blockquote>

I don't think this evaluation mechanism is inherently evil-minded, but nor is it meaningful - it seems somewhat circuitous.  Most of the time, it arises because the student ran out of time to do more conclusive, complete user studies.  So, for example, I have a certain set of tasks in mind where I think Jambalaya can really beat Protege.  So I have an unfair _a priori_ knowledge of what needs support, and evaluation of the tool using that criteria will only really show that I identified problem areas correctly.



What I think needs to be done is much more difficult, and more akin to what I think we've done with Jambalaya.  Namely, some longer-term, longitudinal study which examines all aspects of the tool with real-world problems (like the NCI).  If we evaluated the wines ontology, it would be unrealistic to a degree, because the tool is really snappy at that size, which is unrealistic. 



The approach I've taken is based on tool adoption.  That is, my criteria for success (in the sense 'we address real-world problems with our tool well') is to show that the tool as developed was used more than previously.  Clearly, another measure would be some sort of qualitative survey of people using the tool to see whether this happened and whether they were happy with it.  The big problem here is that adoption is a very tricky thing to measure.  How much of the fact that company X uses Jambalaya can be attributed to our improvements (say, in customizing the tool) and how much is based on other factors, such as those Rogers talks about (management dictate, lack of alternatives, use of Protege).



What to do?  Clearly, I cannot roll out improvements to Jamblaya and get testers to evaluate how well those changes worked (i.e. are they faster/more accurate/happier than if they'd used either old Jambalaya or Protege) because that process suffers from selection bias.
( Although that isn't necessarily true if the tasks are selected independent of the tool, but how to prove that)



The other issue is that my area of study, the NCI, does not use Protege in day-to-day activity, which makes the issue of adoption a purely hypothetical one.  If Gilberto likes it, does that mean that the NCI will use it?  I see more chance of this happening in an organization which already uses Protege.  But for a smaller subset of functionality, say like that in PromptViz, I can definitely see that being easier to show that people liked.  It would be a matter of saying to Frank, here is the tool, here is how you get your data into it, and it's bombproof and works well with large datasets.  I don't think I'll be able to say that.  I'm concerned that assuming I had a good user population to conduct some kind of survey on, the improvements I make to Jambalaya will be too obtuse or confusing to people _unless_ they had a compelling reason to try it, such as widespread corporate use of Protege.



These issues make me think, at least for now, that the best way to analyze the ideas I have -- that allowing people to customize a complex cognitive support tool with some (hopefully) simple mechanisms -- is impossible to do with end-users (modelers).  My feeling at the moment is that this is evaluation is best treated as validation, by asking Gurus like Polly, Samson, and Gilberto whether the improvements make Jambalaya easier to use and more likely to be adopted by end-users.  Thus the analysis becomes a purely qualitative one, perhaps even making use of some of my own expertise in an introspective case study like Polly performed.  It's disappointing, though, after a lot of work, to not be able to conclude defintively whether or not your work has merit.





* * *


Walenstein's work has application here, for sure, and it is probably a good idea to contact him.  He talks about some of these issues in validation of his cognitive support framework.  I'm a little concerned still about the close ties between an analysis of cogntive support requirements (e.g., BU-HASTI) and the tool he's looking at (RIGI).  Which came first?  For example, he poses some key cognitive requirements for bottom-up program comprehension, such as offloading memory, and then mentions that RIGI can do this.  Yes but why?  Is it possible to categorize program comprehension support tools using any kind of independent analysis?  I'm afraid I'm leaning towards a negative answer here. As he writes (page 288): Rigi's authors seem to have been quite aware of most or all of the essential insights all along.  Walenstein seems to identify the same issues I'm running up against: 

<blockquote>This chapter demonstrates that latent psychological claims existing in research tools can be articulated. This means that they can be explicitly tested for, both for evaluating existing ideas, and when designing new tools and variations of them. Right now, little else is known about how to systematically evaluate such tools. Currently we pit tools against one another and pick through the secondary evidence of performance data. Being able to articulate psychological claims about tools makes it possible to test the claims more directly. For instance, do perceptual judgments in Rigi substitute for knowledge-based reasoning? This is (at least in principle) a directly testable hypothesis. The deeper implication is that tool building expertise within the field can be made more credibly founded by exposing such claims and encoding them in independently validated theories. Thus, if domain wisdom is the raw materials for tools knowledge, then applied theories appear to be the most likely catalyst for scientific reform; credible claims about tools are the precipitate.</blockquote>

Thus, perhaps one of the ways to analyze my improvements might be to use Walenstein's distributed cognition framework to show that a) Jambalaya does NOT address all the issues and b) the improved version does address more (similar in theme to the IJHCS paper).  Thus adoption is bypassed as a merely 'last-mile' challenge, and when I call for more cognitive support in KE tools, what I'm really looking for is more disciplined analysis of the tools we design for this area.  That is, using topics Walenstein mentions on page 290, I can show (perhaps) how using such an analysis would show that KE tools really could have been a lot better a lot earlier.  Evaluation is confined to demonstrating that the new version supports more cognitive tasks than the old version (we take as a core assumption that Jambalaya IS a KE tool).





* * *

### Updates

Talked with John Domingue of KMI today about the evaluative aspects of my thesis.  He mentioned Paul Mulholland was someone who had evaluated progam visualizations of Prolog tools which might be applicable. His thinking was that the idea that there is a 'better' and 'worse' zero-sum game in evaluating these kind of tools is irrelevant.  What is more important is for the tool and the thesis to act as an exploration of the problem space, identifying the tasks and challenges therein.  Then that thesis can be expanded upon by others (advancing the body of knowledge).  A better evaluation is to get the tool used by real users and then get them to report on their experiences/problems, what tasks the tool helped them with, what challenges it presented etc.
