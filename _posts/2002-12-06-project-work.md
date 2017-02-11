---

date: 2002-12-06 16:15:00+00:00
title: Project Work
---

Tearing some hair out today. I have been trying to set up the different aspects of the system. Broken down, this is

    * the web server (GUI), which must be Java-enabled (e.g. Tomcat);
    * the parsing and query engine, probably Jena
    * the data instance store - see note 1 below;
    * the actual ontology schema - see note 2;
    * the data, which are the web pages and the email repositories (MBOXs).

Note 1: the data instance store can be run as a full-fledged database, using something like Sesame
Note 2: the ontology schema are what defines the classes used in the instances (the raw RDF files are defined by the RDFS files, in other words). I have had some difficulty wrapping my head around how this works. Furthermore, there seems to be poor tool support for either option. If we conflate the ontologies (like FOAF and DC), we simplify the naming but lose the power of separate maintenance. If we separate them, a tool like Protege has a difficult time maintaining all the namespaces. There is a need for a tool which can be used just for instance creation with separate namespaces for different ontologies; or at least, I have identified no tools filling such a need.
