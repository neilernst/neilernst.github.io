---

date: 2013-11-20 19:11:45+00:00
title: Evidence in Software Engineering
---

This post is spurred by a line in a paper of Walker Royce, son of Winston Royce, he of the "waterfall model" (misunderstood model). He says



<blockquote>
  without quantified backup data, our software estimates, proposals and plans look like long-shot propositions with no **compelling evidence** that we can deliver predictably or improve the status quo.
</blockquote>



Bold text is mine, to emphasize this notion of evidence. The question then becomes what evidence is acceptable. And here I think we get into some hoary philosophical questions concerning truth in science (epistemology, really).

I think one of the fundamental impedance mismatches in software engineering for large-scale systems, or software engineering in a systems engineering environment (e.g., airplanes, military software, ultra-large-scale software, safety-critical software) is that a number of people on those teams have a positivist view of evidence. They subscribe to the notion that sufficient "data" can show whether something will work or not. So if you design a missile system's rocket engines, those engines either deliver the necessary thrust, navigability, etc. or they do not (actually, I think this is probably not the case in those so-called hard sciences either, but the point is that people from those domains _think_ it is the case).

Agile software delivery works much more from the falsificationist or even outright constructionist approach. I would estimate that the majority of agile practitioners believe in the test and refine approach, where you deliver an increment, test it to determine how well the ['theory' of that software](http://catenary.wordpress.com/2011/04/19/naurs-programming-as-theory-building/) matches reality, and then iterate. The key difference with the positivists being, of course, that there is no _a priori_ evidence you can use to show things will work. It is hard to do simulations in Simulink or Matlab as to how well software will perform. This is why [Alistair Cockburn calls software development a cooperative game](http://alistair.cockburn.us/Software+development+as+a+cooperative+game). And some people, I would say, would go even further and treat software development as a post-modernist exercise in building the reality you want to see and dispensing with evidence altogether ("if it works, it is right"). Those people probably don't get a lot of government contracts, however.

Back to the quote: the issue remains, how easy is it to produce "compelling evidence" and what does it consist of? In Royce's view, evidence takes the form of historical context for productivity, function points, etc. In that case we are almost measuring the team's capability to deliver more than any particular artefact.

At some level, cynically one might say, there is a need to show the 'evidence' that will get the job or contract. People hire companies like Thoughtworks because they have a track record of getting the job done to people's satisfaction. We don't much care how long it took, or how many lines of code were written, if the software was valuable.

Which is fine, but as an engineering discipline one would like a bit more to chew on.

