---

date: 2003-10-27 18:55:35+00:00
title: KCAP workshop - Visualization in Knowledge Engineering
---

Here are some notes on the KCAP workshop "[Visualization in Knowledge Engineering](http://www.cs.uvic.ca/~nernst/vike)" I organized with Peggy Storey.  We had 21 people attend the workshop, exceeding my expectations, and all told it went very well. More notes from Peggy, should get those.
Some scattered and random notes:



	
  * Look at pattern detection

how many tools develop because they're free and java
	
  * must consider the #clicks measure

	
  * provide a gentle introduction to ontologies

	
  * path visualization

	
  * [walrus graph](http://www.caida.org/tools/visualization/walrus/) tool by Munzner shows a lot of nodes as context (and has a cool name to boot!)

	
  * Point was made (perhaps Peggy) that there is a lot of expertise in drawing large graphs in speedy fashion and in fact, this is not the limiting problem in the field of VIKE.  Rather, the limit is deciding what to do with these graphs.

	
  * Predictability is another good NFR/goal

	
  * More talk from Harith about a 'visual slot widget' to allow people to use the tool in Protege forms

	
  * Alan Rector mentioned he was used to thinking of his ontology as super-subclass structure plus lateral relations

	
  * Someone mentioned the paper comparing InXight vs. Treemaps but I can't find it.


Comments on my talk:

	
  * John D. mentioned that showing the execution model is important for verification, for e.g. even Ian Horrocks can't figure out all the implications of some complex OWL ontologies.  He also mentioned that you should think of ontologies as high quality reusable components, and as such, perhaps the designers should be incorporating these features at that point, rather than adding it in.  I mentioned I didn't think that was very likely (they often don't even document what they are adding anyway!)

	
  * Another person (whose name I didn't get) mentioned that graphic design features, such as graying out labels, what text size to use etc. could be important to consider.  I talked with him about this, it seems difficult to do this when the domain is not known (for example, when a cartographer creates a paper map he has a good idea of the requirements; making these techniques domain independent is much harder).


The third talk, by John Laird, talked about using diagrams to show experts how the knowledge they entered plays out in the real world.  Allows one to do specification and verification at the same time using examples.

	
  * At the break, I had a good talk with [Stuart Middleton](http://www.ecs.soton.ac.uk/~sem99r/index.html) from Southampton about recommender systems.  His talk earlier at KCAP (see previous postings) talked about the same kind of idea, using the combination of interests the users specified to make recommendations about what papers might be of interest.  He suggested extending the recommendations to suggest good _visualizations_, for example, based on the paths others have taken to that node.  This ties in to the discussion I had with Ken Wong at CASCON about how the UA team implemented a central history bean into SHriMP to track a complete list of actions a user has taken.  Stuart's suggestion would use this history path and record a series of navigations, and use that record to suggest the ones that were fruitful.  Then users would be able to specify whether that visualization was useful.  I really like this idea, it's a bit smarter than the bookmark, but not completely automated.


[Heiner ](http://www.cs.vu.nl/~heiner/)gave a talk after the break about [P2P sharing](http://km.aifb.uni-karlsruhe.de/projects/swap/public/public/index.htm).



	
  * Reminded the group that ontologies are intended to be distributed.  His system uses local queries and also forwards the query to peers to implement and store results for later.

	
  * Mentioned the DOPE browser for query forming and refinement.  Requirements were to be fast and snappy, intuitive, and learnable.  Problem is that no conceptual knowledge is shown and it was overwhelming.  Essentially the browser is a form of the Spectacle tool shown in the paper by van Harmelen.

	
  * Heiner also mentioned the EROS project (great acronyms!), emphasizing that the focus in RDF is really the relationships (well, perhaps this could be restated to suggest that 'concepts' are not the sole focus, and the relations have equal importance).  The problem area identified by this project is that no tools support looking at two different relationships at the same time.  Perhaps use [stylesheets ](http://www.w3.org/2001/11/IsaViz/gss/gssmanual.html)to do "personal views on external data" and be able to customize?  Requirements evolved from 2 groups (e.g. Elsevier people), via a mediating partner (informal req gathering sounds like).


[Rich Keller](http://ic.arc.nasa.gov/people/keller/) gave a good talk on the challenges they have organizing complex data for scientists at NASA, using three techniques.



	
  * Semantic organizer

	
  * nodes/links gives some idea of a metric for complexity.

	
  * Question: where do techniques such as filtering and organizing information fit into EVF?  Perhaps should be in another ontology for interacting with data?

	
  * Presented a categorization of 3 ways of looking at data:

	
    1. graph-theoretic

	
    2. information theoretic

	
    3. semantics-based (their approach)




	
  * Contextual filtering: user typically knows the context, so define a constraint which generates a meaningful subgraph in that context.  For example, for this domain of data gathering, all I want is the location, the data samples, and the time collected.  Allow users to define a set of nodes for a context e.g. FieldTrip = {samples, measurements, people, images}

	
  * Good idea, but how to collect that information?  Who specifies it?  Maybe use Stuart M.'s idea for recommendations here, and populate with some initial data?

	
  * Other approach: Semantic Structure Abstraction.  Figure out what substructure patterns there are, and use graphic design cliches such as trees for hierarchical data, matrices for tabular data, PERT charts for temporal data, etc.  Postulated that this could be done semi-automatically.

	
  * Finally, talked about Semantic Navigation, such as a 'Bull's Eye Navigator', using some kind of meta-ontology or upper ontology to suggest ways to navigate and deal with space-explosion problem.


There was a good discussion at the end as well.  [Alan Rector](http://www.cs.man.ac.uk/ai/Staff/alan.html) commented that [GALEN ](http://www.opengalen.org/)project typically has 6 parents, 20 children, and 6-7 links out for each concept, which would make a graph structure nearly impossible to navigate.  Called for a meta-level for big graphs.  Rich mentioned that this was a fuzzy thing, that there is no use-axis on which things are built.  John D. talked about how in some projects, such as [WebOnto](http://kmi.open.ac.uk/projects/webonto/), the UI was a focus, but generally this wasn't the case.  Alan then commented that there were large ontology projects with a user focus, such as [GO](http://www.geneontology.org/)'s [Dag-Edit ](http://www.geneontology.org/doc/dagedit_userguide/dagedit.html)and an Oxford project, using custom tools.  Alan also thought that perhaps some of the problems had to do with a lack of screen real estate, that maybe it was time to look at multiple monitors like in CAD apps or the [British National Formulary](http://www.bnf.org/).

All in all, a very productive and informative workshop.


[Listening to:  Liberation Front (Radio Paradise - eclectic intelligent rock - music info & listener community at radioparadise.com)  -  Thievery Corporation  -  (0:-1)]
