---

date: 2009-11-14 13:38:56+00:00
layout: post
title: My sample Google/Microsoft interview question
tags:
- combinatorics
- google
- powerset
---

As in, one I have to deal with, as opposed to being asked.

Let's say you want to calculate the powerset P of a list of items. For each subset of P you will do a non-zero amount of work, so we would like to make P really small. The size of P is ... 2^N. Meaning of course for any useful input, P is enormous, heat-death of the universe type size.

We have some function f(s) that takes a subset member  of P (a set) and returns True or False. If True, we want to filter out all the subsets of the subset set.  E.g., if f([1,2,3]) = True, we would like to remove [1,2], [1], [2] etc. from P (so we don't evaluate them as well). So the question is, what is an efficient way to do this? The naïve solution is to generate **all** the members of P, then iterate over them to remove the members that are subsets of a solution. But of course, for large N, this is infeasible to store and to do. Consider the case where the member we find is the set of all items. In this case we should stop our loop. A good solution will allow us to do this in constant time (and not by using a special case).

_Update: I should make it clear that f([1]) = T and f([2]) = T does not mean f([1,2] = T._

Solutions I've pondered include using a bit matrix and bit masking, but I can't see how to do that in constant time. We might also represent the subsets using a tree with related by subset, which would probably be log or sublog time.

One question I have is whether these questions are always checked for solvability. I mean, it is relatively easy to pose a question that is not solvable in deterministic polynomial time, and just as easy to pose one whose answer cannot even be checked for correctness. That would be a rather unfair question, wouldn't it? Like, find a linear time algorithm for finding a truth assignment to the following formula. If you can solve that you should probably start your own company.
