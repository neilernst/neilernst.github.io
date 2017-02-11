---

date: 2007-01-02 18:54:32+00:00
title: Spolsky and methodology
---

I read a [good interview with Joel Spolsky](http://dir.salon.com/story/tech/feature/2004/12/09/spolsky/index.html) today. He makes some interesting points about the software industry. One is that:   


<blockquote>The key problem with the methodologies is that, implemented by smart people -- the kind of people who invent methodologies -- they work. Implemented by shlubs who will not do anything more than follow instructions they are given, they don't work.</blockquote>

I've referred to this as the "Smart Person Problem", and it infects almost every research paper in software and requirements engineering. The thing is, I don't necessarily think you can _never_ differentiate methodologies. It's just that it's extremely difficult to do this empirically. Think of the independent variables: the nature of the problem, the team that defines that problem, the technologies involved. Most importantly, it just isn't possible to control all of these things and give two teams two methodologies and compare the results, as you might do in biology or medicine. So that's a major hurdle in convincing people like Joel that methodology A is best: he'll say, first of all, where's the evidence? And secondly, in what context?  
  
The next point he tackles is model-driven development.   


<blockquote>First of all, there are a lot of people who say they're going to invent some new thing where the business      manager is going to specify what they want the software to do and it will mechanically translate that      specification, and       _brrrrt!_       The trouble is, this is a perpetual-motion machine. We keep inventing it, keep making companies to ship it,      they're always wrong. The fundamental problem that you're trying to solve here is that humans think of things in      vague, mushy terms. In order to visualize something, they don't have to actually visualize every part of it.      Whereas the programmer, in order to actually implement that thing, to create it, needs to have every part      specified.</blockquote>

  
That's pretty close to my thoughts on MDD. The real challenge doesn't seem to be in the model-to-software phase. We can figure out how to translate a UML class model and some restrictions into working code. The challenge is in defining the problem and what the solution ought to be. This is where I'd like to make a contribution. My feeling is that if your modeling language supports this fuzziness (not necessarily inconsistent, just partial), in particular provides for model evolution, than the ability of a MDD solution to match with the 'vague, fuzzy terms' of the client is much much higher.
