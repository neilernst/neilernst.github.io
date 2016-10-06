---

date: 2013-03-12 16:47:55+00:00
title: The fuzzy notion of "business value"
---

Software development is rife with references to business value, particularly in agile approaches: the [Agile Manifesto declares](http://agilemanifesto.org/principles.html) that "Our highest priority is to satisfy the customer
through early and continuous delivery of valuable software."

The trouble is that it isn't clear what 'valuable' means. I'm sure that the point of this phrase, as with most of the Manifesto, is to start a discussion rather than to behave as a prescriptive methodology. I believe "value" is inherently context-dependent, so in that sense it is reasonable to leave it vague.

On the other hand, many people refer to business value as the Holy Grail of software development: this is what you are supposedly optimizing in Scrum. Other methodologies help focus on "impact". Lean approaches have one remove 'waste' from the value stream. And yet no one has ever pinned value down, as Racheva et al. have shown [1] (in the software domain, anyway - many attempts have been made in economics).

Business value does have the nice property of communicability, though. It gives developers that one number to sell the project to the business, and allows for a conversation about scope, cost of delay, and prioritization that is difficult to do with purely qualitative methods. And for the mathematically inclined, it lends itself to algorithms like linear programming for optimization.

One paper **does** try to break business value into more reasonable components, which I quite liked. It is by Heidenberg et al. [2]. They break business value into five dimensions, each of which is ranked on an ordinal scale with four possible categories:






	
  1. Monetary Value - this is the number calculated by, say, a business analyst.

	
  2. Market Enabler - does delivering this feature create new market opportunity?

	
  3. Technical Enabler - does this feature help prepare the company for other features?

	
  4. Competence Growth - measures how much the work will improve the team's skill.

	
  5. Employee Satisfaction - do the developers like working on this feature?

	
  6. Customer Satisfaction - how much will customers appreciate this work?


One of the big problems with agile planning is that making categories 2, 3, 4, 5 visible is often hard. It is comparatively easy to sell a customer a feature that ranks highly in monetary value or customer satisfaction - these are the slick and cool UI widgets, the mission-critical Word reporting function, and so on. But making architectural work (category 3) visible is very challenging. If we had this six-factor model, prioritizing important architectural work would be easier.




[1] Z. Racheva, M. Daneva, and K. Sikkel, “[Value Creation by Agile Projects: Methodology or Mystery?](http://www.springerlink.com/index/10.1007/978-3-642-02152-7_12),” presented at Product-Focused Software Process Improvement, 2009, vol. 32, no. 12, pp. 141–155.

[2] J. Heidenberg, M. Weijola, K. Mikkonen, and I. Porres, “[A Model for Business Value in Large-Scale Agile and Lean Software Development](http://www.springerlink.com/index/10.1007/978-3-642-31199-4_5),” presented at EUROSpi: Systems, Software and Services Process Improvement, 2012, pp. 49–60.
