---

date: 2007-06-28 01:50:24+00:00
title: 'Python and Java: an experience report'
---

I've been coding a program that will parse a set of Python files into an [Abstract Syntax Tree](http://en.wikipedia.org/wiki/Abstract_syntax_tree), walk that tree with a Visitor, and then turn relevant parts into goals for a goal modeling tool.

My first effort was in [Eclipse](http://eclipse.org) and Java, using the [Pydev](http://pydev.sourceforge.net/) tool to generate the AST and pass me a message with the root of the AST. From there I had to write a Visitor (there are several examples to draw on). I struggled enormously with this. First off, I made a mistake in tying my code to intimately to the Eclipse platform. I spent a lot of time trying to figure out how to build an Eclipse plugin, how to listen to events from another plugin, etc. The second difficulty is that the AST Pydev produces is pretty impoverished. There are no explicit links to children/siblings/parents, which makes walking the tree strange. Somehow it works, but not that clearly. This development effort took me the better part of a week, off and on.

Then, for another part of the project, I ran [PyLint](http://www.logilab.org/857) to generate basic metrics. Turns out that one of the components of PyLint is an AST implementation using the Python builtin libraries. After an hour of hacking around with this suite of tools, I'd coded a Python file that did essentially the same thing as the Java version, only much more simply and clearly.

One of the things I do miss in Python is the auto-complete and tool support it seems only a type-checked language can buy you. But maybe this is more a function of the IDE one is using.
