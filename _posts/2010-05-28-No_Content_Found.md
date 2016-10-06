---

date: 2010-05-28 10:50:09+00:00
published: false
title: Using GridWorks
tags:
- freebase
- gridworks
- lod
---

Gridworks, [described here](http://code.google.com/p/freebase-gridworks/wiki/UserGuide), is a data cleaning and browsing tool. I think. It can do more, I'm sure. Herewith a few questions that arose in playing around:

I'm trying it in conjunction with the [Apps4Climate Action initiative](http://apps4climateaction.gov.bc.ca/) to see how it works. My first step was to download the data from the [Ministry of Forests Climate Data section](ftp://ftp.for.gov.bc.ca/HRE/external/!publish/Climate/).


### Data cleaning


I then played with Gridworks's ability to do data cleaning. I had several cells with uppercase mixed with lowercase, the lowercase reflecting a 'sub-zone'. I used the _Transform Column _feature of Gridworks to leverage the Gridworks Expression Language (GEL) to do some neat regular expression style manipulations of the data. At its heart this is "merely" a find and replace function, but that description does not do justice to the user-interface work the engineers behind the tool have done. 

At any rate, by the end I managed to turn "ABBA unc 1" into three separate columns. A small cleanup but for working with the data, pretty fundamental.


### Loading data into Freebase


Now cleansed, I wanted to shove this data into my Freebase 'base' to share with others. For example, Freebase defines a query language and HTML API for turning these topics into web pages. [See my previous post](http://neilernst.net/2010/05/21/using-freebase/): the crux of it is that you will need to create a _base_ on the main site first. And then, since the Gridworks loader (currently) only loads to Sandbox, you need to wait until the Sandbox site (sandbox-freebase.com) gets its weekly refresh from the main site. 

The next hurdle was connecting the spreadsheet to the data model I defined in this post. I needed to map each cell in my dataset to some feature in my schema. To do this, you use the schema alignment skeleton.

Schema alignment is, like data modeling, a bit of a black art. Fortunately, the Gridworks engineers have built some nice functionality into the tool that makes this simpler. The challenge is to take each column (Types) and map those into data triples, where the left-hand-side is the Type, followed by the property, followed by its subject.

The figure below shows my initial 'alignment skeleton':

[caption id="attachment_1142" align="aligncenter" width="700" caption="Gridworks schema alignment skeleton"][![Schema alignment skeleton](http://fink08.files.wordpress.com/2010/05/screen-shot-2010-05-28-at-11-14-00.png)](http://fink08.files.wordpress.com/2010/05/screen-shot-2010-05-28-at-11-14-00.png)[/caption]

As you can see, I've mapped each column to the corresponding type in my base (/base/bcbiogeoclimaticzones/<type>) and also defined some other properties, like the Zone description, as plain text 'types'.

This defines a mapping that Gridworks can use to load into Freebase (using the "TripleLoader" view above).  It's key to make sure it maps to your types, otherwise it disappears into the ether. Screenshots from developer [David Huynh](http://twitter.com/dfhuynh) [here](http://imagebin.ca/img/GIEPHWq.png) and [here](http://imagebin.ca/img/GWU-LiHw.png) show the sequence to do this in.

Once you have a skeleton, you can load the data. This calls up the Freebase loading framework, which you can [see in action with Peacock.](http://peacock.freebaseapps.com/stats/data.labs/gridworks/)

I had a few problems with the data loading. The key is whether Freebase knows what to make of your personal types.


### Discussion and Related Reading


**Data modeling**: There is an excellent overview of the complexities of designing a data model/ontology [over here.](http://www.epimorphics.com/web/category/category/developers/organization-ontology) It makes one wonder whether the promise of OWL's open world assumption and linking data will ever pan out. Is it possible to make an ontology of other people's ontology concepts? How can we link ontologies? Do we even need to?

**Data formats**: Excel? First off, the file was in Excel, which means you need Office for it to work (well, maybe just the viewer). Secondly, it turns out (helpfully enough) that the file has been built with macros to make data exploration easier. But in the open data context, you really don't want that type of helpfulness -- it just puts another layer between you and the data. Fortunately the raw data is in another worksheet.

**Persistence**: how reliable is the URL the data is stored at? If I go to add the data to e.g. Freebase, can I reliably reference the URL for the metadata?

**Metadata**: it isn't enough to have machine readable data. We also need to have machine-readable experimental descriptions. There is a great discussion of this issue between [Jon Udell and Randall Julian](http://blog.jonudell.net/2009/12/15/talking-with-randy-julian-about-bioinformatics/) on how this works in biology and pharmacology.
