---

date: 2010-05-21 17:37:54+00:00
title: Using Freebase
tags:
- climate
- freebase
- gridworks
- lod
- open-data
---

I'm trying to learn how to import data into [Freebase](http://www.freebase.com/), a web site that is like a machine-readable Wikipedia, by way of learning how to use [Gridworks](http://blog.freebase.com/2010/05/10/announcing-the-release-of-freebase-gridworks-1-0/), a data-cleaning tool. However, there don't seem to be any tutorials on creating data schemas in Freebase.


### The data


I was browsing the BC Apps4ClimateAction site to play with Gridworks, and found the BC Forest Service's climate data for the [biogeoclimatic zones of BC](http://www.for.gov.bc.ca/HRE/becweb/system/how/index.html).  I think they are recording things like average annual rainfall for each zone. I thought the general concept of biogeoclimatic zones (BGC) was worth sticking on Freebase, as it forms a terminology that can be re-used in many different settings. A BGC (or BEC) is a geographical area that is defined by similar climatic conditions. E.g., the climatic zone defined by rolling hills of prairie grasses.

The data I'm working with consists of the zone names and subdivisions, along with some common names:

[caption id="attachment_1133" align="aligncenter" width="700" caption="Snapshot of the BGC data model"][![Snapshot of the BGC data model](http://fink08.files.wordpress.com/2010/05/bgc-data.png)](http://fink08.files.wordpress.com/2010/05/bgc-data.png)[/caption]

There are 229 rows like that.


### The model


Now, the important task is to represent this spreadsheet in a linked data schema. There seem to be some common properties: one is the partonomy -- well, geographic containment, really -- between Zone, Subzone, Variant and Phase. The other relations are descriptive: the long name for the zone, and the description of the particular subzones. Finally, we have a relationship between the zone and something called the NDT Code. I haven't figured out what that means, but it's probably worth sticking in.

How does Freebase expect data to be entered?

The meta-schema for Freebase is similar to RDF. There are _Types_ and _Properties_; each _Type_ belongs to a domain (namespace) consisting of similar _Types_. A _Base_ contains _Types_ and _Properties_ describing a semantic domain. _Topics_ are instances of (multiple) types and can be related via properties to other _Topics_.

The Types in this case are the column headings (except the index, of course). The Properties reflect the properties I discussed above. They relate Types together. Then the next question is how to map this model to the Freebase set of properties. Ideally, particularly for these high-level concepts, we would re-use existing relationships.

We also want to describe our Types using existing Freebase types and relations. E.g., we should probably reflect the fact that a `BGC Zone is-a Location`. The more annotations like this we can include, the more useful our data set should be for people who want to re-use it.

So I found the following mappings:



	
  * BGC Zone is type Location (http://schemas.freebaseapps.com/type?id=/location/location)

	
  * The same is true for the other subdivisions.

	
  * The divisions are related using the contains property: http://schemas.freebaseapps.com/property?id=/location/location/contains

	
  * The Phase and BGC Zone have alias properties http://schemas.freebaseapps.com/property?id=/common/topic/alias

	
  * An NDT_Code becomes a new property of a BGC Zone.


Each cell in the table is then linked into this model; e.g., the cell BAFA becomes a Zone topic, with certain instantiated properties (like `Contains SubZone 'un'`).


### Using Freebase's Schema Editor


Now I went to the Freebase Sandbox to actually create the schema. I created a new base, and in that base created my four types and added the Location super-type to each type. A Location naturally has the properties of containment, but I couldn't understand how to override that property to specialize it further. Eg., my Zone should only contain Subzones, not any Locations. I was therefore forced to create special properties for this base.

[caption id="attachment_1136" align="aligncenter" width="700" caption="A snapshot of the Schema Editor"][![A snapshot of the Schema Editor](http://fink08.files.wordpress.com/2010/05/freebase-schemaed.png)](http://fink08.files.wordpress.com/2010/05/freebase-schemaed.png)[/caption]

The neat thing about Freebase is that I can add others who can now edit this schema. For example, a forester might have some other properties that can be added to a Zone. Even better, the schema can be re-used in other schemas: for example, using the Type Zone in some species project.


### Accessing the new schema


You can check it out at http://bcbiogeoclimaticzones.sandbox-freebase.com/. The next step is loading the instance data into the base using Gridworks -- stay tuned.

Update: Apparently 'sandbox' means the server is overwritten weekly. Should have anticipated that. Anyway, I have recreated the base at the main site: h[ttp://bcbiogeoclimaticzones.freebase.com/](http://bcbiogeoclimaticzones.freebase.com/)


### Challenges





	
  * Evolving schemas: what happens if the Forest Service redefines the data model or renames a Zone? In a linked data context, external parties will rely on my model in order to build applications. That means a change in my naming conventions (e.g., "Zone" vs. "BGC Zone") will impact them. I'm not sure the Freebase folks have thought about versioning/backwards compatibility.

	
  * Consistency: how can we check that our model is consistent? Do we care about issues like normalization in the linked triples context? How can I constrain the model? There are some opportunities in the Schema Editor, but we might want cardinality restrictions, logical tests, and so on. 


