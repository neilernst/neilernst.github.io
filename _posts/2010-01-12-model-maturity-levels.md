---

date: 2010-01-12 15:22:42+00:00
title: Model maturity levels
tags:
- nato
- ocl
- science
- uml
---

Part of my research used the [Object Constraint Language](http://en.wikipedia.org/wiki/Object_Constraint_Language) to provide a model query language. Knowing nothing about OCL a year ago, I am now getting to be more familiar with it. The [OCL specification](http://www.omg.org/technology/documents/formal/ocl.htm) is pretty well written, although hardly suffused with useful examples. Consequently, I bought the [OCL book](http://www.amazon.com/Object-Constraint-Language-Addison-Wesley-Technology/dp/0321179366) by Jos Warmer and Anneke Klepper.

OCL is associated with the OMG model-driven architecture (MDA) initiative. Consequently, the book assumes that a world in which all software is created by manipulating diagrams (ok, not all models are diagrams, but most are) is a good and inevitable one.

First off, diagrams are not necessary in doing modeling, in fact may be counter-productive. The authors bring out the modeling maturity levels, where 1 is denigrated as 'the lowest level of professional software development', with specifications residing in the developer's head, and level 5 being full use of models to develop systems.

There is no evidence that I am aware of that shows that software built in level 1 is more {maintainable, usable, functional, cheaper} than level 5. This hierarchy is entirely based on conjecture, and as such is a good example of over-reliance on begging the question (i.e., let's assume that in the ideal world, software will be built with models, and then start looking for premises to support that conclusion).

It would be a good study to compare software built ad-hoc (level 1), versus software built using models. Certainly the former approach has by far the greater degree of industry acceptance, so on the basis of adoption, at least, the modeling approach has completely failed to make its case.

This is why I argue for moving our field from one of 'building solutions better' to 'understanding what to do'. Software engineering started in 1968 at a NATO conference on how to handle the massive amounts of software code that was clearly going to be a big part of the future. It was here that the idea that software production should be more systematic and repeatable -- more like building a bridge -- was first put forth.

And that's all to the good. However, what we do as academics is not building things. I mean, I've written code, but I'm sure it's horrible and unreliable. But it's not my central concern. My central concern is science, and as I understand it, that means exploring new ideas and testing those ideas in the form of theories. Most of what passes for software engineering research, however, is the building of new and unproven technologies or, worse, ideas for new technologies in the form of frameworks. It's as if physics was only theoretical, and never experimental.
