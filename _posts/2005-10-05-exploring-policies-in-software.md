---

date: 2005-10-05 21:02:38+00:00
layout: post
title: Exploring policies in software
---

Policy is the explicit encoding of common, best practice in some shareable format.  Having a policy ensures that common practices are easy to understand and follow.

One technique that software engineers use is to codify policies into explicit (formal) language.  With this, and formal versions of behaviour (say, a company log of correspondence) and the law, one should be able to quickly see what is contravening policy, or what policy contravenes law.  For example, people have numerous contractual obligations, such as credit cards, mortgages, frequent-flyer points, etc.  If one could formalize these, it would be easier to understand a 20-page hedge fund contract.

An interesting research space is to examine how to make such assertions human-understandable.  For example, one could use an i* model to dynamically examine dependencies between agents following a certain policy.  One could run various randomly chosen scenarios to test how well the stated policy stands up: e.g., one needs to pay the credit card by the 20th, but gets paid on the 21st.

Grey areas would also be more obvious in such a scenario: currently understanding what is and isn't covered by an insurance policy, for example, is very convoluted.  If one had a normative specification of what is covered, rather than what isn't ("Acts of God"), entering into such agreements would be simpler.

Naturally, obtaining formal policy specifications is currently intractable.  That's why we have lawyers and judges, of course.  However, for certain policies -- personal data, credit card terms, insurance, etc. -- I think it is conceivable to attempt this (not automated, but still...).  It brings forth a range of interesting notions.
