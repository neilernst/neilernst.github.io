---

date: 2013-10-24 15:59:25+00:00
title: Configuring SONAR with Maven on Mac
---

I had this issue a few times:



	
  * you get SONAR installed and the web client working fine (e.g. you can go to http://localhost:9000 and see the dashboard).

	
  * you have a project to analyze with a Maven POM, to which you add the sonar target as described here.

	
  * you start the Maven run and it returns in short order saying:


`Can not execute SonarQube analysis: Unable to execute Sonar: Fail to download [http://localhost:9000/api/server].`

Turns out for some reason this is a problem with the default Ruby install on OSX. The workaround is to use JRuby instead of Ruby, best done with RVM, e.g. rvm use jruby. Someone mentioned this online, and I cannot find the post now, but thanks.

I use Sonar with Homebrew, by the way, which has its log files at `/usr/local/Cellar/sonar/<version>/libexec/log/sonar.log`.
