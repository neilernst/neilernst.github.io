---

date: 2006-04-02 22:01:16+00:00
layout: post
title: Model drift
---

Say you model an organization, an org chart. As soon as it's finished (for some reasonably large organization) the chart is outdated (well, it's outdated as soon as you start and a change happens you are unaware of or unable to incorporate). Changes happen more frequently than top-down models can manage.

Say T is the modeling time, than the change time is D,  D<T. As D gets smaller, the change multiple M of the process means that the distance Z of D from A, the actual state of affairs, is correspondingly larger. A change can be defined as some atomic unit either moving or being added/deleted). How can we deal with this problem? One thing is to do [agile modeling](http://www.agilemodeling.com/), which in Scott Ambler's notation seems to mean **ad-hoc** modeling. This modeling is done on an as-needed basis. There is more to his methodology than that, but I cannot find scientific evidence to support his claims. Furthermore, doesn't agile modeling conflict with agile development? Wouldn't an agile proponent argue that the code is the design, and thus the model?

The problem (I conjecture) is that any model will never be equal to reality, limiting what information it can give you -- e.g. formal inference. [Some](http://www.cs.toronto.edu/~mstrohm/) want to remove the professional modeler from the equation. But I don't think that's likely for a variety of reasons, including institutional inertia, consultant self-interest, and other technical challenges (human interface design is an entire area of research).

So where does my work differ from agile modeling? I want to define a methodology (empirically validated, natch) that provides a way to estimate the degree of drift (model drift) from model to reality. Then, using this estimate, probabilistic inference on a model may be possible.

Model drift is the degree of difference between a model and the emprically assessed state of affairs in reality (clearly this definition is loaded with epistemological assumptions).  I include the term empirically assessed because we typically cannot approach the true state of the world (quantum mechanics, for example, seems to preclude this). We can, however, statistically model the state of the world, and for most finite problems this statistical model is indistinguishable from reality.
