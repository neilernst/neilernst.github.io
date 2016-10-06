---

date: 2008-10-08 18:57:07+00:00
title: 'Thesis idea: debugging model-driven development'
tags:
- debugging
- gmf
- MDD
---

Here's a possible thesis topic:

One of the problems with designing your system with a model-driven (MDD) approach is tracing back the source of the errors (and let's be honest, there will always be an error, if not a bug).

Often, the MDD tool is very opaque as to what is happening during the transformation. My best example is the Eclipse GMF toolset. While it hides a lot of unnecessary code, typically low-level UI and abstraction handling code, it can also hide code that might be relevant if your system doesn't work as expected.

Here's a simple example: I need to add a custom function to my graphical element. I've searched the poorly documented GMF builder, and there's no way to make this change in the models (graphical, tooling, domain, mapping). I read up on GEF and make the change in the generated code.  Later, my colleague re-generates the code, without being aware of my changes. Eclipse preserves them, because I used the _@generated NOT_ keyword, but now he wants to find any of this code. There's no good way to tell my IDE to only show code that **isn't** generated. But that might acutely important if I'm maintaining a MDD-constructed system.

Another example is LISP macros. In LISP there are two compile steps. One step expands all the macros one defines into their normal LISP form. This is similar to the preprocessing step in C, but much more powerful. The code is then compiled (or evaluated) as appropriate. However, the macro expansion step is (to my limited knowledge) opaque. It isn't easy to debug what is going on when the macro expansion is performed (other than trying it out). And I expect debugging the final program would leave lots of references to the eventual, generated code, rather than the actual macro responsible (which is what you want to see). A tool that could trace from final form to macro form would be invaluable.

I think a lot of this is similar to Greg Wilson's "cognitive gap between what programmers write and what they have to debug" [(ACM Queue)](http://www.acmqueue.com/modules.php?name=Content&pa=printer_friendly&pid=247&page=2).  There's plenty of logic wrapped up in an ANT build script that is difficult to parse with the current tooling. That is even more so for model-driven development tools. And most research into these tools ignores these practical problems in favour of recondite mathematical theorizing about model merging and model translation. This is not merely a matter of implementation details!
