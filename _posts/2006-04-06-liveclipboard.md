---

date: 2006-04-06 00:31:29+00:00
layout: post
title: LiveClipboard
---

Jon Udell has an interesting [screencast](http://weblog.infoworld.com/udell/gems/liveClipboard.html) about the Microsoft [Live Clipboard proposal](http://spaces.msn.com/editorial/rayozzie/demo/liveclip/liveclipsample/clipboardexample.html). He illustrates how it might work for events, then points out the problem with identifier clashes. Two event services (for which we might want to copy/paste an upcoming event) have different representations for the same venue (and Udell notes this could easily be the case for people or things as well). How do we map between an identifier on one site and an identifier on the other?

The top-down approach would seem to be a general taxonomy, with an agreement on what constitutes "Avon Gumby Theatre, England".  Then all the services would use the URI for that theatre, and happiness all around. Udell's proposal for tagging standards are along the same lines -- at some point there needs to be agreement on representation.  Danny Ayers [posts](http://dannyayers.com/2006/04/04/live-clipboard-and) about the structured approach to the problem. I like the idea that what identifies you is a collection of statements about you, such as your photo, your address, your web site, etc.  A reasoner can assume nothing until it is reasonably satisfied you are a certain individual.

The bottom-up approach would probably be some sort of data mining strategy, a la Google. If enough references are made to the event/person/thing, then it must be the canonical version thereof. Of course, this completely ignores the long tail - what if I have an event at the "Avon Gumby Theatre, England" only mine is a small community theatre in the Midlands, instead of the vast edifice in London?
