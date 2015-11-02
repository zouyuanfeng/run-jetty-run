# Introduction #
We are going to talk about the Classpath details in Run-Jetty-Run.


There are two classpaths we need to discuss it here.


---


### Jetty Container Classpath ###

Used for our bootstrap . It's seldom changed in general development case.

![http://files.tonyq.org/eclipse/runjettyrun/classpath_jetty.png](http://files.tonyq.org/eclipse/runjettyrun/classpath_jetty.png)


---


### Web App classpath ###

In a general wab app , it's the classes/jars in WEB-INF/classes and WEB-INF/lib

![http://files.tonyq.org/eclipse/runjettyrun/classpath_webcontext.png](http://files.tonyq.org/eclipse/runjettyrun/classpath_webcontext.png)



---


## Web App Classpath Details ##


### How to check what classpath RJR is loading ? ###

It will load the all the Classpath in your Java Build Path ,
it locate at project context menu -> properties -> Java Build Path.


You could also check/edit the classpath in **Webapp Classpath Tab** of RJR RunConfiguration.

![http://files.tonyq.org/eclipse/runjettyrun/run-configuration-webcontext-view.png](http://files.tonyq.org/eclipse/runjettyrun/run-configuration-webcontext-view.png)


---


### How to add new classpaths to web context ? ###


There's two way to change web context classpath

  * Change project configuration in project properties

Or
  * Click **Webapp Classpath** > **User Custom classpath** in the RunConfiguration

  * Click "add Projects"/"Add class folders"/ "add Jars" /"add external jars" as your need to add new classpath.


_Note: It's better to change the project classpath instead of changing classpath of RJR Configuration._


---


### How to exclude some unused jars ###

  * Uncheck the checkbox in front of jars.

  * Note: You can't uncheck a container forever,we will help you uncheck  all the jars in the container , but if you add new jars to the container , it's still default be checked.



---


## Jetty Classpath Details ##

> ![http://run-jetty-run.googlecode.com/svn/trunk/updatesite/RJRConfigurationClasspath.png](http://run-jetty-run.googlecode.com/svn/trunk/updatesite/RJRConfigurationClasspath.png)


(It's the view since the 1.2.1 and a bit different in past,we use container to handle the Classpath to avoid the absolute path.)


  * It's located in Run-Jetty-Run Run configuration , and only releated to the Jetty Bundle.(6.1.6 in past , 6.1.26 after 1.2 )
    * You could replace it with any Jetty6 version one by one.(I haven't test it with Jetty 7 / Jetty 8. )

  * Run-Jetty-Run bootstrap jar for a Jetty launcher in our implementation. (It's a must have.)



Note: **Usually you don't need to add any container Classpath here** , all the framework/lib like Spring/Hibernate/Struts ,
it's web app stuff and should be placed in WebApp classpath, not containers.


---


# More #

#1 Actually it's not loading the source folder .
if you do have  resources or java classes in source , but you got a ClassNotFound or 404 ,
please check if your target output folder exist the mapping class or resource,
sometime clean the project may make it work.(It's usually a defect for Eclipse builder.)


If it's not working as expect , please post a bug.