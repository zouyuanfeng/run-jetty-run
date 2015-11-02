# Publish Date #

2012/03/16

# Introduction #

It's a newer version for Run Jetty Run again,
fixing those bug in the new view we introduce in 1.3.2.

Now it's more a stable version for web-context/jetty classpath and scan folder management,and we turn source scanner off by default in this version.


# Update Site #

http://run-jetty-run.googlecode.com/svn/trunk/updatesite


# Outline #

## What's new in 1.3.3 ##

1. Move Jetty 7 / Jetty 8 to latest stable version.
> Jetty 7 from 7.5.1.v20110908 to 7.6.2.v20120308,Jetty 8 from 8.0.1.v20110908 to 8.1.2.v20120308


2. Web-context/Jetty classpath management is working for most case that you add or uncheck  classpath entries now.

> Note:We only exclude jars files/class folder when you uncheck a container or folder.
> > For example , if you uncheck maven dependency (A container) , RJR will exclude all those jars in maven dependency, but if you modify the pom  file and add new jar classpaths , those newer jar files will not be excluded.
> > Anyway , when it's not working as expect , check your run configuration first.


3. Turn off source scanner by default.

> i. If you still want it to be default enable, please config your preference. (_Window_ -> _Preferences_ -> _RunJettyRun_ -> _Default enable Scanner when create new run configuration_ )

> ii.User could still enable it in source monitor tab of run confiugration for each project.



# Details #

  * Issue list http://code.google.com/p/run-jetty-run/issues/list?can=1&q=label%3A1.3.3

  * Features
    * [Issue 128](https://code.google.com/p/run-jetty-run/issues/detail?id=128): Upgrade to latest Jetty Version

  * Bugs
    * [Issue 109](https://code.google.com/p/run-jetty-run/issues/detail?id=109): ATTR\_WEB\_CONTEXT\_CLASSPATH\_NON\_CHECKED doesn't work due to path issue
    * [Issue 114](https://code.google.com/p/run-jetty-run/issues/detail?id=114): Project classpath issue for WebApp classpath and Jetty classpath
    * [Issue 115](https://code.google.com/p/run-jetty-run/issues/detail?id=115): Change default setting for source scanner to disable
    * [Issue 116](https://code.google.com/p/run-jetty-run/issues/detail?id=116): throwing NPE if folder/jars in the source monitor list not exist
    * [Issue 117](https://code.google.com/p/run-jetty-run/issues/detail?id=117): Source scanner tab get wrong path for web.xml under the webcontext
    * [Issue 119](https://code.google.com/p/run-jetty-run/issues/detail?id=119): test add folder in webcontext classpath view and jetty view.



# Notice #

  * Please feel free to report anything you find , no matter bug or opinion. :p

  * To speed up your installation ,please don't check this option.
> > (Contact all update-sites during install to find required software.)
> > http://screencast.com/t/DuCNNp4D59R

  * For Jetty8 's restriction , you have to use a "JDK Runtime" instead of default JRE Runtime to run it, or the JSP complier will not work.


# Next Milestone #

  * Live update support ( Browser will refresh after you change the html/css/javascript. )

  * We will check some new feature , and review Jetty 8 support ,
like Spdy support, or some useful feature for developers.


# Special thanks #

Thanks James Synge , Eelco Hillenius for building a such good project and invited me to join the project.

Hope this plugin could help developers to speed up development. :)