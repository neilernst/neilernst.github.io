---

date: 2007-08-22 02:32:23+00:00
layout: post
title: Geography, information, and the web
tags:
- geospatial_data
- gis
- open_source_technologies
---

There is plenty of activity on the open geospatial front. For example, there is a conference (in my hometown, no less) on [Free and Open Source Software for GIS](http://www.foss4g2007.org) in September. I worked for 2 1/2 years in GIS for a provincial government doing cartography, analysis, data cleaning, and so on. I loved the connection between the digital and the natural that GIS work provides (and it got me a sweet ride in a helicopter!).

I characterize the open geospatial movement with the following features (following the [agile manifesto](http://agilemanifesto.org/) style):



	
  * favouring simple, standards-based open-source technologies like [GRASS](http://grass.itc.it/) over large, proprietary tools such as [ArcGIS](http://en.wikipedia.org/wiki/ArcGIS);

	
  * driven by community and users instead of large-scale government or business interests;

	
  * leverages open data and 'routes around' the expensive and unreadable;

	
  * simple, clean outputs (maps, query answers) with a single focus instead of large, complex data products


What are some of the demands web users might have for geospatial data? When you work in a large GIS shop, in B.C. anyway, you are probably concerned with either public works data ([cadastral](http://srmwww.gov.bc.ca/sgb/IMF/index.html), such as city plans, roads), forestry (cut-blocks, tree cover), or the environment (pollution monitoring, wildlife habitats, parks use). The data sets are usually quite large both in area and information, and require quite elaborate data management and integration practices -- maybe not to the same degree as bioinformatics, but close.  These users need answers to very specific questions, and often need someone mediating between the data layers and themselves. For example, the GIS team builds a map of spotted owl habitats based on survey data, rather than the biologist making that map herself.

In the Web 2.0 world, though, our users may be people we've never anticipated. In order to foster a community of users, applications/sites should focus on supporting a simple, approachable set of functionality. For example, Facebook makes it dead simple to find long-lost friends and connect with them. So what might some simple tasks be for a geospatial web 2.0 site?

Many sites already provide digital mapping, e.g. Google Maps and [KML.](http://code.google.com/apis/kml/documentation/) Someone made the point that this is not the same as GIS, since very little analysis is being done. We're really just showing users custom maps. Is this all they want to see?

Government agencies already provide access to things like property assessments, road data, and so on via often-specialized portals. My feeling is that users will first off, want to control their own data that they upload; be able to access an API that allows them to 'mash-up' the site with others; and interact with other users to see what they are up to. I think one powerful function would be exposing some rudimentary processing functions, like data modeling and topological queries (contains, near, adjacent to, etc.). So I should be able to upload my GPS track file, the format being a common, standardized one, and then interact with other data repositories to perform queries. The site I use would just serve as an application server, with data being pulled in from a variety of other places. For example, I might be [paragliding](http://gravsports.com/Paragliding%20Pages/Paragliding%20Stories/Golden_June4_07.htm) over a nice lake and want to use my track file to identify all lakes greater than 100m wide.

I think providing a site that can do web-based topological modeling would be a big winner with some people. Clearly the user would have to be sophisticated enough to know they want to ask that question, but I can imagine some UI modeling would accommodate the most common questions pretty easily. Hmm, maybe there's a business idea in there.

Sites to keep an eye on can be found at ![](http://images.del.icio.us/static/img/delicious.small.gif) [http://del.icio.us/neilernst/foss4g](http://del.icio.us/neilernst/foss4g)
  *[GIS]: Geographic Information Systems
