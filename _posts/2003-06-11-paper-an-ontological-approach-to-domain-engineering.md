---

date: 2003-06-11 14:17:06+00:00
title: 'Paper: An Ontological Approach to Domain Engineering'
---

See [here](http://shrimpbib.chisel.cs.uvic.ca:8081/drupal_viewrefs.jsp?frameId=conferencepaper_14) for more information about this post.

Routine paper about using ontologies to do domain modelling (inexplicably called domain engineering, why must every area have engineering appended to it?).  The idea is that if you have to model a domain, for example, in requirements gathering, you can model it formally (with an ontology) and then try and translate this into software specification (say, from classes and method calls to concepts and relations in the ontology).   This will help with reusing the artifacts produced (since you now have a formal model that can be modified and altered).

- 2 phases: building ontologies, and deriving object frameworks from them.

- I had a problem with the idea of this paper as it seems to directly contradict some experiences in the field; namely, that what we need is less formal domain models, not more formal.  Requirements engineering is a loaded term that seems to insist on the use of complex, rigid models that fail to address the changing and dynamic nature of most software projects.  I can see this approach working in some situations, for example, safety-critical systems, but not in the majority of software projects.  For example, how would XP make use of an ontology?

good quote: "an ontology is not only a hierarchy of terms, but a fully axiomatized theory about the domain." (from Falbo, Menezes, Rocha 98)

should look into the categories of ontologies more:
- neutral authoring
- ontology as spec
- common info access
- ontolgy-based search
- ontology-based Info Vis (?)
from Jasper and Uschold (KAW 99) see [ uschold-onto-class.pdf](///c:/Documents%20and%20Settings/nernst/My%20Documents/papers/kr-onto/uschold-onto-class.pdf)

Paper proposes LINGO as a graphical language to model ontologies.  Problem they encountered is that this is too abstract a representation for most users.  Didn't use UML because: too much notation, no formal semantics.  Also, using UML might overload the meaning of certain constructs, but might help adoption.
