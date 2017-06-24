---

date: 2003-11-04 23:46:16+00:00
title: Notes on implementing EVF in Shrimp
---



  * idea is that eventually the FINALs in ShrimpView and ShrimpProject (like layout names) would be defined in the ontology and then used from there, rather than buried in the classes.  


  * I've renamed my classes (instances) to reflect the naming scheme used in the Finals


  * the context/popup menu is causing headaches, there are a lot of options that are multiply defined even though they represent the same action (e.g. performing an alphabetic arrangement on selected nodes.)  We should remove the context aspect and just apply the layout to those nodes.  Somehow I need to separate the menu items in Shrimp from the actions they perform.  Currently menu location is defined as part of the name of the tool.  So I if say remove all grid layouts, I have to say this is several different places.


  * what about the toolbar at the bottom of the screen?  this needs to be handled somehow?  I think for the purposes of the user study I can just make a 'good-enough' implementation, the temptation is to really start ripping out the guts and redo everything.  Must resist this!  The application is already excellent, and my ideas can be demonstrated using what I've proposed. 


  * I've modified the ontology to reflect the UI elements of buttons, and am adding those in and mapping them to the appropriate actions using the relation has_action.  I should probably also do this for menus and the popup as well.
