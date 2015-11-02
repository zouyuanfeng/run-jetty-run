# Publish Date #

2011/05/19

# Introduction #

It's a newer version for Run Jetty Run again!

add some option and new feature for RJR.

# Update Site #

http://run-jetty-run.googlecode.com/svn/trunk/updatesite


# Introduce #

For current RunJettyRun version and 1.2.2 new feature.

<a href='http://www.youtube.com/watch?feature=player_embedded&v=fd8iHPEoNec' target='_blank'><img src='http://img.youtube.com/vi/fd8iHPEoNec/0.jpg' width='425' height=344 /></a>


# Details #

Please check the accpected feature list below:

Enhancement

  * [Issue #11](https://code.google.com/p/run-jetty-run/issues/detail?id=#11) [PATCH](PATCH.md) Support for Jetty-Plus
  * [Issue #57](https://code.google.com/p/run-jetty-run/issues/detail?id=#57) running the plugin directly from the run as debug as menu
  * [Issue #59](https://code.google.com/p/run-jetty-run/issues/detail?id=#59) Write enablement for Short cut
  * [Issue #60](https://code.google.com/p/run-jetty-run/issues/detail?id=#60) support eclipse linked resource in web app folder

# Notice #


  * Feel free to report anything you find , no matter bug or opinion

> This version since we change some core API to support linked resource , and it might be not very stable at this time .
> If you find any bug , please feel free to post a new bug to let us know.Thanks!

  * Linked Resource

> If you add a linked resouce after the server started up , you need to restart the server , since the version got no chance to know the newer resource you add.

  * JNDI support is a experimental feature from user's patch, it's welcome to have some feedbacks for if it's working/


  * we move the Jetty.xml / Jetty 7 and Jetty 8 support to 1.2.3 , since it might need some time to take it and not very urgency for me, if you need it , please vote it in the issue comment. ([Issue #9](https://code.google.com/p/run-jetty-run/issues/detail?id=#9) , [Issue #55](https://code.google.com/p/run-jetty-run/issues/detail?id=#55) )


# Next Milestone #

Here we list the defects we are going to do in version 1.2.3 ;

> _Not sure how much time we need for it , I think it will take a long time since I am busy on other projects and my job._

  * Tasks http://code.google.com/p/run-jetty-run/issues/list?can=1&q=label:1.2.2



And thanks James Synge , Eelco Hillenius for building a such good project and invited me to join the project.

I wish I could make it better.