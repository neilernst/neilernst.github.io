---

date: 2015-10-27 15:23:06+00:00
title: How Writing Code is Like Making Steel
---

I saw an [interesting keynote from Mark Harman](https://www.youtube.com/watch?v=y4xWZj1ocDo&feature=youtu.be) recently, on search-based software improvement. Mark's lab at UCL also pioneered this idea of [automatic code transplants](https://www.reddit.com/r/compsci/comments/3f6hfu/code_transplant_could_revolutionise_programming/?) using optimization techniques.

I think if you are an engineer who does fairly standard software development you should be concerned. The ultimate vision is to be able to take some specification with thorough tests, written in a language at a high-level of abstraction (e.g., here is my corporate color palette, here are my security requirements) and automatically generate the application.

There are several forces at play here. One is the increasing componentization of large and complex pieces of software. We've always had software reuse, but it tended to be at a much smaller level - the ODBC api, or the OAuth framework. Now our frameworks reach much larger areas of concern, particularly when we look at container technology running on commodity hardware. Someone else is maintaining huge chunks of your software base, in those cases: the OS, the backend, the messaging system, etc. If you then take your Rails app and add it to that stack, how much, as a %, have _you_ created? A decreasing amount, in any case.

The other force is the improvements in genetic and other optimization algorithms, combined with the inevitable scaling of computing power. That means that even though you may be really good at crafting code, and the machine generates garbage, it can improve that garbage very very quickly.

How different is it for me to copy and paste the sample code on the Ruby on Rails site to create a new application, than for a computer algorithm to follow those same steps? To be clear, there remain a lot of complex decisions to make, and I'm not suggesting algorithms can do so: things like distributed systems engineering, cache design, and really just the act of taking a user requirement and turning it into a test.

So how is this like the steel industry? I think it reflects commodification and then automation. Steel was largely hand-made for years, but the pressure of capitalism generated rapid improvements in reducing costs - largely labor costs. Process and parts became standardized, so it was possible to set up mills at much lower cost. The difference in quality between US and (say) Indian steel became small enough to not matter. But even in India, the pressures continue downward, so India's dramatically lower labor costs still cannot compete with automation.

Some of these pressures don't exist in software, of course: there is still a large knowledge component to it, and there are no health and safety costs in software labor (the hazards of RSI and sitting notwithstanding). So I don't see any big changes immediately, but the software industry is probably where the steel industry was in the 20s. In 50 years I cannot see software being written by hand at the level it is now, with the exception (like in steel) of low-quantity, high-tolerance products like embedded development. The rest will be generated automatically by algorithms based on well specified requirements and test cases. Silicon Valley will become the rust belt of technology. You realize that Pittsburgh, birthplace of the steel industry, was once the most expensive city in the US, right?

If you doubt this, I think we are really arguing over when, and not what. My simplest example is coding interviews. Why test people on knowledge of algorithms that are well understood, to the point where they are in textbooks and well-used library code? The computer can write the FizzBuzz program faster and more efficiently than a human can. Over the next few decades, I believe Mark Harman's optimization approach will encompass more and more of what we now do by hand.
