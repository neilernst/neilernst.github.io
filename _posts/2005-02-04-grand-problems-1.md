---

date: 2005-02-04 16:33:08+00:00
title: Grand Problems 1
---

I'm attempting to start a weekly post on some [interesting problems](http://csr.uvic.ca/~vanemden/other/hamming.html) in my area of study.

The hope is that this will crystallize some good avenues of exploration.  My approach is generally to start top-down, that is, to consider what might be a challenge in the future, or where I think it might head, and then to work backward from there, to try and see how we can get there.

The vision from IBM for [autonomic computing](http://www.research.ibm.com/autonomic/research/) is to make computer systems self-managing, which consists of self-configuration, self-optimization, self-healing, and self-protection.  The payoff is that as systems get increasingly large -- like [SkyNet](http://www.eterminator.com/) in the Terminator movies -- humans are less and less able to manage them.

The way we typically deal with complexity is to abstract it.  For example, machine code is complex for us to understand.  We build abstractions, such as assembler, to make it easier to understand what is happening.  And abstraction can go on forever - a common research tactic is to take current problems and solutions, and develop some abstractions on top of it as your 'contribution'.

Sometimes, however, these abstractions just make things less coherent.  Many corporate software developers want to see the 'real thing' - which may be why abstractions like [MDA](http://www.omg.org/mda/) have not taken off.  Of course, what the 'real thing' is becomes unclear.  Often, what is meant is just to descend a level or two in the hierarchy of abstractions.

Autonomic computing will require a way of managing abstractions.  A way, I think, of allowing what are, after all, very intelligent system maintainers and designers, to descend and ascend the abstraction hierarchy at will.  For example, although module A is self-optimizing, the maintainer will want to inspect how, exactly, it is optimizing.  The notion this will ever be fully automatic seems far-fetched.

[CWA](http://www.mie.utoronto.ca/labs/cel/research/frameworks/cwa.htm) can certainly apply here.  CWA provides a way of understanding the work domain using an Abstraction Hierarchy of means-ends relationships among parts of the system.  What I think is important, too, is that CWA explicitly provides for human aspects of systems.  I think a major flaw in the autonomic vision is the lack of reference to human input and human control.  Even nuclear plants, which are much more complex than most software systems, are operated.  Remember that SkyNet ended up turning on the humans.  :)
