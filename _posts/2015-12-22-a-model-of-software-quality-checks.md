---

date: 2015-12-22 18:03:55+00:00
title: A Model of Software Quality Checks
---

Software quality can be automatically checked by tools like SonarQube, CAST, FindBugs, Coverity, etc. But often these tools encompass several different classes of checks on quality. I propose the following hierarchy to organize these rules.

### Level 0: Syntax quality

**Focus**: code that 'runs'.
Level 0 means a compiler or interpreter's components (parsers, lexers, intermediate forms) assess syntax correctness. Level 0 because (clearly) without proper syntax nothing is getting done.

### Level 1: Lint-free
**Focus**: Code that respects obvious sources of problem.

No warnings occur if all possible flags are turned on in the compiler. These warnings tend to be close to syntax in their complexity. For example, technically a fall through switch statement is possible in Java, but there is the `-Xlint:fallthrough` tag to catch this. Often IDEs such as Eclipse will flag these automatically with warning icons.

### Level 2: Good code

**Focus**: Code conforms to commonly accepted best practices for that language.

E.g., for Java, visibility modifiers are suitable, in C, no buffer overflows, memory is released appropriately. Some cross-language practices apply: documentation, unit tests exist, and so on. Many of the quality analysis tools like FIndBugs operate at this level. CWEs are another example. I also place dependency analysis approaches here (perhaps controversially). It also pops up in the next level (e.g., properly using interfaces in Java).

### Level 3: Paradigmatic

**Focus**: writing code that is maintainable, understandable, and performant with respect to its runtime environment.

Would someone writing object-oriented, functional, embedded, etc. code consider this reasonable? Includes principles like SOLID, functional side effects, memory management, distributed code demonstrates awareness of fundamentals of distributed computing. Also includes proper use of language idioms e.g. proper use of Javascript callbacks, Ruby blocks, etc. We might also classify new language features here -- the use of generics in Java 7 comes to mind. Essentially, if you did a peer review with a language guru (Odersky for Scala, say), would they have a 'better way' to do it? (Perl notwithstanding...)

### Level 4: Well-designed

**Focus**: building systems that respect appropriate (known at the time) usage scenarios.

Given the knowledge available, the code is architecturally appropriate for the quality attribute requirement (QAR) applicable. E.g., modular, performant, secure. The key here is understanding the relevant QARs. Examples include reflexion models (like [ArchJava](http://archjava.fluid.cs.cmu.edu)), conformance checking (e.g. [Dicto](http://scg.unibe.ch/dicto/)), library analysis (e.g., for license issues, for currency).

### Outcome

A few things become clearer when we view software quality with this approach.

First, I think that quality checks become _more useful_ as you move 'up' (0→4) in the hierarchy. That is, I'd rather know that I have a serious design problem than a code quality problem.

Second, unfortunately, it seems _much harder_ to design truly automated checks at the higher levels. This is why we have a lot of manual architecture analysis but leave code quality to tools.

Third, our rules get _more context-specific_ as we move up the hierarchy. I.e., in order to properly check paradigmaticness[^1], I need to know your choice of programming language and possibly your problem domain properties. To properly do design validation, I need to know what qualities are important to you: performance? availability? That, I think, is partly what makes these levels more useful.

### Other hierarchies

The one I'm most familiar with is from Jean-Louis Letouzey. He proposed the [SQALE quality model](http://www.sqale.org/download), and his central insight is that some qualities precede others: you must have maintainable code before having performant code, or testable code before secure code.

EDIT [1/6/16]: somehow I forgot [this CAST diagram](http://www.castsoftware.com/products/architecture-checker) showing different levels of analysis, very similar to mine. They also claim that the 'system level' (my design level) is the place where architecture is checked.

EDIT [9/6/17]: also [this model](http://qaware.blogspot.com/2017/06/i-know-it-when-i-see-it-perceptions-of.html) from [@stoerrle](https://twitter.com/stoerrle). It also has this notion of abstraction and progression, using 

> SYNTAX At the one end of the spectrum, there are syntax level issues, such as confusing the tokens “=” with “==”, and preference of language constructs (e.g., avoiding unsafe constructs, default-switch-cases and so on).

> PRAGMATICS One step further up, small-scale pragmatic issues like identifier naming, indentation, and simple structural metrics like cyclomatic complexity.

> UNITS The next level addresses complete units of code (often a class or module), and considers its overall structure, unit-level metrics 
(e.g., method/class length) correctness and completeness. 

> ARCHITECTURE Finally, there is a level of architecture that is concerned with the structure and interrelation of units, e.g., it considers depth of inheritance trees, design patterns, architectural compliance, and other system-level properties.

[^1]: I'm not sure how to 'noun' this adjective ...





