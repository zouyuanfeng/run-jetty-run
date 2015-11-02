# Publish Date #

2012/01/06

# Introduction #

It's a newer version for Run Jetty Run again,
refine the run configuration and new features/bug fixs for RJR.


# Update Site #

http://run-jetty-run.googlecode.com/svn/trunk/updatesite


# Outline #

## What's new in 1.3.2 ##

1.**New UI for web classpath in run configuration!**
> You could now enable specific classpath to be loaded or not!

2.**New UI for source monitor list in run configuration!**
> It's a ability to scan files in the list , if those files is add/changed/removed , the jetty server will automatically restart.

> It was the source scanner feature ,and it was only for target output folder in past,now you are able to add your own files to the list as you need!

> We will also scan all XML files in WEB-INF by default!
> That means web.xml , application-context.xml and some files else will be in the list by default , sure you could disable them in the new UI if you don't need it.

3.**Add support for the newer Maven for Eclipse(M2Eclipse) plugin in Eclipse 3.7**.
> In Eclispe 3.7, the M2E changed a lot for the package name and also some details , we was doing some support feature for old M2E since 1.3.0 , and now we also have well support with the newer M2E!

4.**Now we have better servlet 3 support**.
> In 1.3.1 we was trying to support annotation and it was working for annotation.But it's still not working for web-fragment and META-INF/resource folder since the restriction of the Jetty8 implementation , it's only scanning the WEB-INF/classes and WEB-INF/lib/`*`.jar .

> They didn't consider for those classpath that's not in regular classpath , but we use Maven or referenced to other project very often , so that's a big trouble for Eclipse developement.

> In 1.3.2 , we use our own configuration classes to fully support those feature!

5.**We are now only support Eclipse 3.5/3.6/3.7 and after since 1.3.2**


# Details #

  * Issue list http://code.google.com/p/run-jetty-run/issues/list?can=1&q=label%3A1.3.2

  * Features
    * [Issue 88](https://code.google.com/p/run-jetty-run/issues/detail?id=88) New view for classpath editor and source monirtor list
    * [Issue 100](https://code.google.com/p/run-jetty-run/issues/detail?id=100) add referenced project to source lookup path
    * [Issue 103](https://code.google.com/p/run-jetty-run/issues/detail?id=103) Make servlet3  web-fragment.xml working properly in Jetty8
    * [Issue 104](https://code.google.com/p/run-jetty-run/issues/detail?id=104) Finetune source scanner with JDT built-in hot-deploy.
    * [Issue 105](https://code.google.com/p/run-jetty-run/issues/detail?id=105) Refine options after new UI change.


  * Bugs
    * [Issue 89](https://code.google.com/p/run-jetty-run/issues/detail?id=89) RJR restarts on changes in unit tests
    * [Issue 90](https://code.google.com/p/run-jetty-run/issues/detail?id=90) NullPointerException when creating new launch configuration
    * [Issue 91](https://code.google.com/p/run-jetty-run/issues/detail?id=91) Launching fails when webapp dir is "/"
    * [Issue 92](https://code.google.com/p/run-jetty-run/issues/detail?id=92) Exclude test-classes for maven is not working in 1.3.1
    * [Issue 102](https://code.google.com/p/run-jetty-run/issues/detail?id=102) m2e updated container name in newer verison cause issue

# Notice #

  * Feel free to report anything you find , no matter bug or opinion. :p

  * To speed up your installation ,please don't check this option.
> > http://screencast.com/t/DuCNNp4D59R

  * For Jetty8 's restriction , you have to use a "JDK Runtime" instead of default JRE Runtime to run it, or the JSP complier will not work.

  * Currently we do not support the Servlet3 annotations in Jetty8 ,    we will try to handle this in 1.3.1 soon.



# Next Milestone #

No any ideas now , it's still very welcome to report bugs and features.


And thanks James Synge , Eelco Hillenius for building a such good project and invited me to join the project.

Hope this plugin could help developers to speed up development. :)