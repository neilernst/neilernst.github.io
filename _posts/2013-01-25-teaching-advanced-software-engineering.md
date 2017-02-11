---

date: 2013-01-25 19:52:32+00:00
title: Teaching Advanced Software Engineering
---

## Material


The course covers software architecture, with a focus on quality attributes, security, and formal methods. I liked the range of material, even though my expertise is limited with formal methods. It is difficult to teach architecture to students in a 3 month time frame, so we expanded using the [AOSA textbooks](http://www.aosabook.org). Students did a presentation for five minutes as a way of exposing them to various different architectures.

The other large component of the class is a course project. In this semester they had to build a location-aware, social application. There were great projects including my personal fave, a zombie fighting location-based game.

My favorite part of this course, like the third-year course, is seeing how the students approach the project. Some are truly excellent coders and put an enormous amount of effort into the project.

I introduced a few new lecture topics in addition to the ones pre-existing. I added a topic on Service Orientation and SOA, important trend in particular in enterprise architecture; a new topic on REST, which was well connected to the project; and a topic on agility and architecture, based in part on the book by Dean Leffingwell, Agile Requirements. I thought all of these were useful, although they tend to be less easily tested than e.g. model checking, so perhaps students are just forgetting them. I even mentioned CMMI!


## Overall


I feel that these types of courses in SE should be more about reflective apprenticeship than the lecture and project model. In other words, there should be more focus on feedback about the way in which students do design, more experiential learning, and less memorization of specific techniques such as formal methods (which should really be in a separate course, in my opinion). Mark Guzdial called this _reflective apprenticeship_ and points to the [work of Donald Schön](http://www.infed.org/thinkers/et-schon.htm).

A parallel might be drawn with the way law schools operate. If you want to learn about how one practices law, argues cases, etc., you hire experienced practitioners as adjunct faculty. There seems to me to be a real difference between the skills of an academic SE faculty member and a person who has spent years building high-availability, mission critical software. There are a few of the latter at UBC, such as Philippe Kruchten, but in general it is exceedingly difficult for them to be hired without academic credentials. Not to mention the increasingly large salary gap between industrial SE and academic SE.

The other thing I disliked is that it seemed to me that a few students hid out during the project, latching on remora-like to their more capable teammates to secure a good mark with no work. It irritates me to pass students who are not able to write code (not good code, or even mediocre code - just not write code! See [Fizzbuzz](http://imranontech.com/2007/01/24/using-fizzbuzz-to-find-developers-who-grok-coding/)). It is very difficult to (defensibly) identify these people, however. One technique which I should have used is to ask questions of the indifividual students during their final demos. This would help to identify who actually knows what the heck is going on.


## Academic dishonesty and software engineering


On the one hand we cannot prohibit collaboration and code re-use: these are fundamental practices in software engineering. On the other hand, we need to assess the student's actual contribution. I had a few interesting cases that suggest our pollicies in this area need more attention.
1. One group used a sample Ruby on Rails project to bootstrap their application. It came with most of the controllers they needed. They then customized the UI and logic to implement the functionality (poorly).
2. Another team hired a third-party designer to do custom artwork for the project (which looked fantastic).
3. A different team had a friend with web design expertise work on the CSS for the project.
4. Several teams used Twitter's Bootstrap UI library or JqueryUI to simplify their efforts on the design end.
5. Many groups used third-party libraries to simplify their life, like JQuery, Rails, image libraries, etc.

Obviously, most of these are exactly what would happen in industry. On the other hand, it definitely gains one an advantage. The Twitter Bootstrap apps all looked an order of magnitude better than the custom apps.

My principle was the remixing and reuse was fine, as long as it was properly acknowledged. In the design case, we could try to discount that aspect of the UI in the marking. But it is almost certainly the case that some groups did NOT acknowledge their use of other people's IP, and yet benefited from it. I don't have a good solution to the problem of detecting code reuse. And furthermore, the burden of proof is pretty high to call something cheating, and requires more than a gut feeling or a commit to Github that touched hundreds of files at once (i.e. a bulk commit of 3rd party code).


## IT role


One of the things which I think will only become more prevalent is the use of third-party services to manage the course. In the past, students would use CS department machines and servers to do their assignments, a CS database server, and store code on the department subversion or IBM RTC servers.

This semester I don't think we used a single department resource, save for email (and that only because I was forced to for privacy reasons) and the course webpage. Class discussions took place on [Piazza.com](https://piazza.com/); code and issues were managed with [Github](https://github.com/), and students nearly always have their own laptops and Android devices (there was not a single group that chose iOS, incidentally, although nearly half the class has Macbooks. I think the 99$ fee is a real stumbling block - that and Objective-C).

I did not get any support or materiel from the department, apart from the classroom and photocopier. I could just as easily have run this course from my home. So what should the IT section do? They could manage Github for me (they were extremely reluctant to do this, and very hesitant about even installing Bugzilla, apparently). They could provide more AV services to record classes. They could manage virtual machines for me, so that each student could install the same setup -- things like [Puppet](http://puppetlabs.com/) and [Vagrant](http://www.vagrantup.com/) will be key in the coming years.

Finally, the UBC wireless infrastructure is truly terrible. You get better wifi at the Starbucks. Latency between two machines in my office was 200ms! The connection is constantly dropping or extremely slow, such that even demos are affected by the web performance.


## Student perceptions


In an unscientific survey, I asked the following questions:

**1. How could the TAs and myself improve your experience?**  
  
Students were either positive (but they had names attached to their responses, so that isn't unexpected) or asked for more help. One of the big challenges they face is sorting out silly configuration problems. They would like more advice on design choices as well. I think this is a real opportunity to make the project more like an apprenticeship model, a la Software Craftsmanship: take some senior developers, get them to do an hour of code review, an hour of design feedback, etc. And there seem to be many companies eager to help out (and recruit) for whom this might be doable.The other issue was that due to 4) below, TAs and myself often did not know much about the technology (e.g., Microsoft's C#/Azure platforms). However, this is definitely a learning objective in the course. Admittedly in industry one would often be able to ask senior devs these questions. However, the ability to track these answers down is invaluable, I feel.

**2. Were the AOSA readings useful?**

Most students responded that they appreciated the opportunity to present to a large audience. But the overall lessons of the architecture in these systems was lost on them, because it did not have a lot of relevance to the project, which consumed the majority of the time. Asking exam questions was difficult, as there was a lot of material that would have to be studied. I think I would keep this module but be more strict about the time limit (5mins) and give some introductory examples/prep before hand.

**3. Did Github work for you?**

Students loved Github. Egit was less good (and personally I find it less usable than the command line). A major improvement over RTC.

**4. Was the freedom to choose language good or bad?**

Most students loved this aspect as well. In the past the project, worth 40% of the course, has been in e.g. Java+Tomcat for everyone. Feedback here indicated that main problems were finding team members with similar interests (in, e.g. RoR), getting help from TAs, and a possible penalty on the final, where the code snippets are in Java.

**5. What annoyed you about the project?**

Unsurprisingly, most complaints were about the time it took - one student spent 80 hours over two weekends on what was, however, a really cool UI - and the vagaries of group work with fellow team members, some of whom get sick, abandon their teammates, or simply are not good at programming. Students would appreciate more help on scoping the project, and getting the thing started earlier. We tried to address this by insisting on an early 'project idea' review in the first 3 weeks, and by doing a 30 minute design review midway. However, some people have to learn the hard way, and ultimately, we are constrained by how many teams there are - 27 in this case. Multiply that by 30mins and you can see the magnitude of the challenge. I had 3 TAs to help, but that is still a ton of work. And I think students got frustrated, since they see a 1-1 interaction, not 27-1 that I see. 
