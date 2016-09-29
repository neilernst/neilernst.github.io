---

date: 2005-09-11 04:34:24+00:00
layout: post
title: Trac and me
---

Greg invited me to participate more actively in the Trac/Argon project he's running.  The project is building project management tools for undergrad programmers.  I think while traditionally CS courses have been programming oriented, this is going to have to change as fewer jobs are available for these students.  For example, today I viewed the film Ryan, which featured work from UT students, and Seneca College.  This combination of CS skills and creativity is the future, in my mind.

So the Trac project should support students learning higher-order software skills, such as modeling, requirements change management, stakeholder interviews, version control, architecture, etc.  Although I have my doubts about how useful even these skills will be: let's not make the mistake of thinking that Indian or Chinese programmers are only mindless cobots (code robots).  They too are interested in higher-level projects.

Greg's question to me: what interesting research questions can be addressed if you have access to 200 students using this particular software tool?  I suggested some interesting CSCW questions might emerge: for example, as Greg mentions, most students are now more comfortable on cell phones and IM than email or land lines.  How will this affect programming?

Greg also discussed XP and its lack of higher-order thinking.  Design docs are bad, they say: but at some point, someone must have an idea of what is being discussed. Right?  I should investigate how this higher-order thinking emerges, or is used, in XP projects. Are there big agile projects that would require this?  Ambler's Agile Modeling essay seems on target for small systems, but how does it scale to complex, sociotechnical systems involving hardware and software?  E.g. nuclear plant design.  Where is the cut-off?  What tools are useful at that level?

Another thing agile development suggests is feature-complete iterations.  That is, each iteration of a project focuses on a set of features to build, and the cycle is complete when those features work.  My question is, can you always separate things this neatly?  Like an order-entry system.  So in cycle 1, you just get the entry, and not the order filling?  That seems slightly useless, especially as agile advocates claim that because each cycle is complete, killing a project at stage D will still leave features A-C.  Sure.  But maybe it's a plane that now has no landing gear.  Clearly this suggests looking over the feature/user story list and making sure that the appropriate ones are being attacked first.  But that adds docs and clutter, and that's bad.  Hmm.

Piotr is working on Reef which looks to integrate UML and code, with no programmer interference.  Should look at that (so that people get used to manipulating the model).  Here's a question for him: if his UML is tied 100% to the source code, and people can use it to understand the system, then how is it different than MDA?  Perhaps because he doesn't suggest the next leg in the 'roundtrip' cycle: that is, the code must be changed before the model can be.  But this seems like a syntactic difference to me.
