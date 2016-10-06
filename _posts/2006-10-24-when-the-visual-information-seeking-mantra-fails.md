---

date: 2006-10-24 18:15:46+00:00
title: When the visual information-seeking mantra fails
---

Ben Shneiderman proposed, a while ago, a visual information-seeking mantra:


<blockquote>Overview first, then zoom and filter, and finally, details on demand.</blockquote>


This mantra works really well for focusing effort on most visualization applications. For example, when looking at a map, typically we need an overview of the area, then the ability to zoom in, possibly filtering out things like road numbers. Once we've narrowed in to an area of interest, we want the ability to see the details, for example, the house's selling price.

But I don't think this mantra holds up well in other categories of information visualization, or more generally, [cognitive support](http://computer.org/proceedings/iwpc/1883/18830185abs.htm). Many times a user of an application has a specific task or scenario in mind, and really doesn't need to see the overview -- in fact, the overview gets in the way, and can often slow down processing. Shneidermann himself seemed to agree with this notion in a recent talk at the University of Toronto. His recent work is focused on the [hierarchical clustering explorer (HCE)](http://www.cs.umd.edu/hcil/hce/), a tool which provides users with great detail about data statistics, e.g., what data sets are highly correlated. In this type of high-dimensionality space, an overview is at best useless. These users have a specific set of tasks in mind which they wish to accomplish.  They don't need an overview.

I talked about similar ideas in [my paper on ontology visualization](http://www.bibsonomy.org/bibtex/0c4b386a774f3178095395ce26a1851c4/neilernst). We came up with some requirements for tools that wanted to provide ontology visualization. It was pretty obvious from previous work in program comprehension that not all people do top-down (Shneidermann) comprehension. Many people like browsing, ad-hoc navigation, or task-based. Another possible mechanism might be problem-oriented browsing, e.g., have an error to find.

In summary, I think Sheiderman really intended for his mantra to capture commonalities among existing visualization tools. Many of these tools were/are dedicated to newcomers to a domain, for whom top-down exploration is the primary goal. However, I believe the main <strike>application</strike> difficulty of building cognitive support in applications is for frequent, expert users. They need solutions which understand their requirements and do the little things to make tasks easier to accomplish. Understanding the nature of these tasks is crucial and, to date, difficult.
