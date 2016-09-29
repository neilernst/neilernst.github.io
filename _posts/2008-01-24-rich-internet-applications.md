---

date: 2008-01-24 21:03:38+00:00
layout: post
title: Rich Internet Applications
tags:
- ajax
- flash
- flex
- rails
- ria
---

I'm working on a project with my brother. The idea is to be able to visualize results from [microarray](http://en.wikipedia.org/wiki/DNA_microarray) experiments he has done in [the lab](http://www.douglasrecherche.qc.ca/suicide/). I'm taking an image of brain regions and loading the microarray data. The expression levels for the various regions and genes can then be seen as you a)mouse over a region and b) select a gene. There are also sliders that allow one to refine the results (and there are a lot of them).

To develop the application, I'm using Flash. I tried Flex, the web application version of Flash, but the main need I had was designing a rich GUI (a labeled brain).

In Flex, you can create applications much like Flash, with the absence of heavy-duty focus on timelines, stages, etc. The main advantage seems to be an extensive and speedy library of rich components, with extension mechanisms. Flex can also talk to other tiers, middleware, database, etc. via Flex Data Services (all this is freeware, btw, unless you have a heavy need for data services, where it gets pricey).

However, Flex seems in many ways to duplicate the functionality of HTML forms. I don't see the point of a set of UI components that are comboboxes, lists, and text-entry fields, since these are also present in HTML. What is useful is the ability to draw and diagram a non-standard component like my brain chart.  I'm still awaiting an application that can provide the rich graphical editing tools of Flash with the lack of timelines and scenes that Flex provides. There _is_ a way to integrate a Flash component in Flex, but this seemed cumbersome.

For data access, I used Rails to serve up XML over the wire. It isn't really REST style, but simpler than other approaches. I didn't need to use Rails to do this -- probably a direct SQL call would have been simple enough -- but I wanted to try it out.

Why not AJAX? In some sense this is a false comparison. AJAX is a methodology, which Flex partly adheres to -- asynchronous and XML, just not via Javascript. The main difference seems to be that one doesn't need to muck around in Javascript and CSS/DHTML for the UI. Frankly CSS and HTML scare me with their complexities.  The resulting Flash movie is accessible to most browsers out there (although the broken context menu is annoying).

What is a RIA anyway? Many of these concepts seem to be drawn directly from good ole Applets, which to my mind are very much like Flash movies from an end-user POV (clearly less nimble, but still...). I suspect that for most applications, the simple suite of UI components that HTML defines are probably sufficient. It will only be for graphical charts and displays that Flash-like tools will be necessary.
