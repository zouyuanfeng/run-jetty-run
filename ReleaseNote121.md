# Publish Date #

2011/03/22

# Introduction #

It's a newer version for Run Jetty Run again!

Clean some bugfix and add some option for RJR.

# Update Site #

http://run-jetty-run.googlecode.com/svn/trunk/updatesite


# New Configuration view #

![http://run-jetty-run.googlecode.com/svn/trunk/updatesite/jetty-run-configuration-1.2.1.png](http://run-jetty-run.googlecode.com/svn/trunk/updatesite/jetty-run-configuration-1.2.1.png)

# Details #

Please check the accpected defect list below:

Bug fix

  * [Issue #8](https://code.google.com/p/run-jetty-run/issues/detail?id=#8) Add scanner to restart the server when classes change (bug fix for 1.2)
  * [Issue #18](https://code.google.com/p/run-jetty-run/issues/detail?id=#18) Can't share launch configs because absolute paths used in "classpath"
  * [Issue #42](https://code.google.com/p/run-jetty-run/issues/detail?id=#42) Running the plugin on a maven project should not include the test classes
  * [Issue #48](https://code.google.com/p/run-jetty-run/issues/detail?id=#48) classpath will fail because the command too long
  * [Issue #52](https://code.google.com/p/run-jetty-run/issues/detail?id=#52) RJR get wrong classpath in M2Eclipse
  * [Issue #53](https://code.google.com/p/run-jetty-run/issues/detail?id=#53) Classloader caused error with Beanshell


Add option
  * [Issue #42](https://code.google.com/p/run-jetty-run/issues/detail?id=#42) Running the plugin on a maven project should not include the test classes
  * [Issue #27](https://code.google.com/p/run-jetty-run/issues/detail?id=#27) jetty fails to launch with a linkage error
  * [Issue #39](https://code.google.com/p/run-jetty-run/issues/detail?id=#39) SslConnector and setNeedClientAuth



If you find any bug , please feel free to post a new bug to let us know. Thanks.


# Notice #

If you run a existing project and get a ClassNotFound Exception in bootstrap , it's caused by you customized the RJR classpath in "Run Configuration" , you might need to restore default entrys to get newer jetty package works.

We change the RJR bootstrap/Jetty jars classpath implementation to use container at 1.2.1,so it's last time we need to worry about this.


# Next Milestone #

Here we list the defects we are going to do in version 1.2.2 ;

And plan to release it before May.


  * tasks http://code.google.com/p/run-jetty-run/issues/list?q=label:1.2.1

And thanks James Synge , Eelco Hillenius for building a such good project and invited me to join the project.

I wish I could make it better.