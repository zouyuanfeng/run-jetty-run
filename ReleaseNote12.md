# Publish Date #

2011/03/11

# Update Site #
http://run-jetty-run.googlecode.com/svn/trunk/updatesite

# Introduction #

It's a newer version for Run Jetty Run!

We updated the Jetty version from 6.1.6 to 6.1.26, accepted the enhance for "source scanner", add port defect , keybinding , some useful features , and fix some annoying bug.


# Details #

Please check the accpected defect list below:

  * [Issue #7](https://code.google.com/p/run-jetty-run/issues/detail?id=#7) Disable Jetty's locking of static files
  * ~~[Issue #8](https://code.google.com/p/run-jetty-run/issues/detail?id=#8) Add scanner to restart the server when classes change~~ (not working in 1.2 )
  * [Issue #13](https://code.google.com/p/run-jetty-run/issues/detail?id=#13) Warn if port is already in use
  * [Issue #33](https://code.google.com/p/run-jetty-run/issues/detail?id=#33) Use latest version of Jetty
  * [Issue #44](https://code.google.com/p/run-jetty-run/issues/detail?id=#44) Can't specify project dir as webapp dir
  * [Issue #50](https://code.google.com/p/run-jetty-run/issues/detail?id=#50) Jars under WEB-INF/lib aren't found unless on eclipse projects classpath
  * [Issue #51](https://code.google.com/p/run-jetty-run/issues/detail?id=#51) Add keybinding to start server


If you find any bug , please feel free to post a new bug to let us know. Thanks.


# Notice #

If you run a existing project and get a ClassNotFound Exception in bootstrap ,
it's caused by you customized the RJR classpath in "Run Configuration" ,
you might need to restore default entrys to get newer jetty package works.


# Next Milestone #

Here we list the defects we are going to do in version 1.2.1 ;

And plan to release it before May.


  * [Issue #52](https://code.google.com/p/run-jetty-run/issues/detail?id=#52) RJR get wrong classpath in M2Eclipse
    * **This one is the major one in next version.**

  * ~~Check the compatibility with Jetty 7/Jetty 8 .~~ (Move to milestone for 1.2.2 )

  * Other tasks http://code.google.com/p/run-jetty-run/issues/list?q=label:1.2

And thanks James Synge , Eelco Hillenius for building a such good project and invited me to join the project.

I wish I could make it better...