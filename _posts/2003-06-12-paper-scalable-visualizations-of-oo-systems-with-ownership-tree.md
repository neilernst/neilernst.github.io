---

date: 2003-06-12 14:01:16+00:00
layout: post
title: 'Paper: Scalable Visualizations of OO Systems with Ownership Tree'
---

See [Shrimpbib](http://shrimpbib.chisel.cs.uvic.ca:8081/drupal_viewrefs.jsp?frameId=journalarticle_15) for more details.
Uses the concept of ownership trees to visualize software.  An ownership tree represents parents and children as classes that have a 'calls/called by' relationship.
Seems equivalent to non-structural relationship (where the structure is given by the is-a arcs).  In Shrimp I think this distinction is less clear (as everything could be structural).
Important idea: abstract the specific links (such as MouseMotionListener) to the generic type (Listens, Adapts, Implements) according to some design pattern ontology.  This would simplify the links required to visualize the ownership graph.
Understanding the structure of a program's object graph, then, is a crucial prerequisite to understanding the program itself, and thus to debugging, maintaining, or extending the program, or even simply learning how it works.Key principles for their visualization (compare to our requirements?): 

  1. one display showing most objects;
  2. an automatic layout;
  3. layout provides info about the semantic structure of the objects.

The visualization itself seems to suffer yet again from a complete lack of testing.  It seems very confusing and cluttered, and the information presented is sparse and unhelpful.
