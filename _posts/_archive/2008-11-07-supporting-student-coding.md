---

date: 2008-11-07 03:58:34+00:00
title: Supporting student coding
tags:
- drproject
- subversion
- trac
---

Part of a software engineering university education has to be concerned with familiarizing students with the tools and technologies that are used in industry. I don't think this is the most important role for a university; critical thinking skills, time management, and a deep understanding of all available options (e.g., functional programming, imperative programming, database programming, assembly programming, OO programming, dynamic languages) are more important in my view. But while a good student should easily be able to pick up Silverlight programming, for example, there do seem to be some key technologies that should be in any undergrad computer science education.

One of these is configuration management, specifically, bug-tracking and code versioning.  The University of Toronto has created a software package supporting these features, [DrProject](https://www.drproject.org/). The tool is a fork of the Trac open-source project management package, rewritten for the specific needs of students. It has been under development (mostly by summer student programmers) for two years (as DrProject; for longer in other incarnations). Greg Wilson has spearheaded the effort, borne out of a strong belief (well-supported, from what I can tell) that exposure to such a tool is important for students.

The tool has, in my opinion, raised a number of questions: Can we take it as read that understanding how to use Subversion (beyond just checkins, i.e. for merges and branches?) is important? What about tickets and task tracking? Given that it has been two years since DrProject was formally introduced to students in programming classes at UT, what have the results been? Do those students use the tool completely? While they are often forced to submit via Subversion, how many are using it for more than this? What types of tickets are being created? Is DrProject worth all the time and effort that Greg Wilson and his students spend on it? Is it creating better quality graduates? Do employers care?

I guess the more pertinent question is whether these skills and concepts -- branching, task management, testing, etc. -- are things that must be taught over long periods of time (like calculus, IMO) or whether a reasonably talented person can pick it up within a few weeks of starting a new job.

Personally, having done a few small projects with a TDD philosophy, I think that skill (test-first) is not something that can just be picked up as needed. It seems fundamentally different. I suspect that complex source control tasks are similar: when to branch, when to integrate, how to manage numerous tickets and bugs, etc.

However, my limited exposure to students using DrProject suggests they mostly don't use these advanced features. Occasionally they use ticketing; source control is highly used, but that may be a product of the teaching staff distributing assignments that way; and that's about it. One team I came across used a version-controlled text file with a list of bugs they needed to fix, even though DrProject provides a simple ticketing system with much more power.

We definitely need some longer-term studies, and I think Greg has been trying to secure some type of funding for such a thing, but not had a lot of success. One suggestion has been that the reality in industry is similar to the situation at UofT, i.e., that tools like Trac are little-used there, too. But I think that's unrealistic, particularly at well-managed software shops.

Despite the uncertainties surrounding the tool, I think Greg and the cast of thousands (tens?) that have worked on DrProject should be congratulated for, at the least, generating some interesting (and testable!) software engineering questions.
