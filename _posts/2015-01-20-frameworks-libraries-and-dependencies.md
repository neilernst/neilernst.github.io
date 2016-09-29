---

date: 2015-01-20 02:28:52+00:00
layout: post
title: Frameworks, libraries, and dependencies
---

I've been doing a little thinking about frameworks lately. They fascinate me as 1) a realization of the vision of 'pluggable software' and reusable components desired since probably [1968](http://homepages.cs.ncl.ac.uk/brian.randell/NATO/); 2) what you are getting into when you rely on one. This is prompted by [this great post on libraries vs frameworks](http://sencjw.com/posts/2015-01-08-the-quick-hack.html).

Now, we've used libraries for ages, viz. glibc etc. And the notion of 'code that someone else wrote and maintains that I need' was likely established in the design of Unix and pipe and filter architectures. But it really seems like the past 10 years have seen this wonderful explosion of creativity in writing 'little libraries' for various different systems.

I'll take a common example. I've previously used [Node.js](http://nodejs.org) for a [small visualization](http://bioviz.herokuapp.com) I did for my brother's work on genetics (in progress!). Although an academic, I like to try to stay on top of things, so I tried out Node, the Javascript web server. Now JS itself has at least[ 60+ frameworks and libraries,](http://en.wikipedia.org/wiki/List_of_JavaScript_libraries) and that list doesn't even include Node or some of the ones I'll describe below. This is amazing considering although JS has been around a long time, only recently (would we say JQuery is the prototypical case?) has this explosion happened.

The trouble is that like the Cambrian explosion, some of these libraries and frameworks are doomed to extinction. If you are BigCo, that makes choosing one very tricky, in addition to the licensing and security questions you will need to ask.

Consider. I wrote the application for the Node server, using [Express](http://expressjs.com) as a web framework (that means it automates some of the routing and layout of files and directories for you). To get to the database I used the [Node PostGres ](https://github.com/brianc/node-postgres)library. To do UI I relied on [JqueryUI](http://jqueryui.com) and [Stylus](http://learnboost.github.io/stylus/) for CSS, with Jade for templating. Then I used [Morgan](https://github.com/expressjs/morgan) for logging, [Gulp](http://gulpjs.com/plugins/) to automate the style generation from the Stylus files, and was toying with D3 to do the display. Not to mention I need a Platform as Service from [Heroku](https://www.heroku.com/home), so I have their command line tools installed as well.

So that gives about 10 different libraries to run this app. On the plus side, they automate a ton of code I no longer have to worry about, letting me focus on the key value-add of the app (realized in the SQL code I write and custom request handling code).

But I just upgraded to Express 4, and they've broken the back-compatibility, so I must now understand what the changes mean and [how to retrofit them](http://expressjs.com/guide/migrating-4.html). Who maintains these libraries? Will he or she keep updating it? These are by no means new questions, but I think what has changed is that now it is very hard to avoid using them. And once you commit to it, re-architecting for the problems you will inevitably face with leaky abstractions seems challenging, because everything is deeply connected. You cannot just drop in a new back end server with the same libraries.

Now imagine that multiplied times 10 years and instead of my simple app, a mission critical information system, and you start to get a sense of the problem that legacy applications can pose. Fortunately, I [work at a place](http://sei.cmu.edu) with lots of experience solving those problems, so give us a call if you need help!
