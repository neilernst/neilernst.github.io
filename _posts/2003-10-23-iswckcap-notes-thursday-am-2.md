---

date: 2003-10-23 11:34:25+00:00
layout: post
title: ISWC/KCAP notes - Thursday a.m. 2
---

[Benchmarking DAML+OIL repositories](http://www.cse.lehigh.edu/%7Eheflin/research) - Guo and Heflin






	
  * different design options for SW

	
  * goal: develop a way of evaluating different repositories

	
  * similar to DB and DL benchmarks

	
  * compose some test queries on an ontology of (you guessed it) CS departments and research

	
  * key metrics: load time, repository size, query response (logical completeness vs. query time), query size (incomplete list)

	
  * showed some complex graphs for some databases (DLDB), seems guilty of ‘NASA syndrome’ with his PPT

	
  * wished he’d showed evaluations of more, different repositories

	
  * how much logical completeness is necessary




* * *


[Cooking the SW with OWL api](http://sourceforge.net/projects/owlapi) - Sean Bechhofer, Raphael Volz, Philip Lord



	
  * starts with conclusions

	
  * use higher level data model to insulate one from concrete syntax, make functionality salient

	
  * [contest  ](http://wonderweb.semanticweb.org/owl/WhatSpeciesAmI.rdf)

	
  * primarily targeted at OWL-DL/LITE

	
  * memory based

	
  * what is an OWL impl?  - modeling, parsing, serializing, manipulation, inference

	
  * not keen on RDF/XML, for example, round-tripping not great, containment messed up

	
  * OIL had a serialization that users liked

	
  * notes that as one of the key features is that ontologies entail certain information, but how can you *show* this new information? Just add it in, use a new interface?

	
  * particularly important when users are involved : what to do when a user tries to remove the information that was inferred. Separation also shows people what services are provided.

	
  * uses [Command design pattern](http://exciton.cs.oberlin.edu/JavaResources/DesignPatterns/command.htm) (metadata, notification, versioning) - seems applicable to EVF ideas.

	
  * imports a weaker part of language - need to capture where a thing was said (context)

	
  * does this exist outside the rdf model itself?  see rdf:isDefinedBy

	
  * it seems that increasingly, the base level of the SW is coming to an agreement, and now some bigger issues are arising: security, context, change, validation, meta-levels

	
  * another thought: see forums for a question on releasng SHriMP projects.






