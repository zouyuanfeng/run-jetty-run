**This is a old version (1.3.1) guide , for latest version , please refernece to [GettingStarted](GettingStarted.md)**

# Installing #

Well, that's easy. Simply use Eclipse's update manager (Help -> Updates -> Find and install... -> Search for new features to install) to add a remote site and point it to http://run-jetty-run.googlecode.com/svn/trunk/updatesite. Click finish, select the plugin  and finish again. Done.

Also you could use marketplace client to search RunJettyRun.

# Using #

1.Quick start
> <a href='http://www.youtube.com/watch?feature=player_embedded&v=Dtj1YBy9LKw' target='_blank'><img src='http://img.youtube.com/vi/Dtj1YBy9LKw/0.jpg' width='425' height=344 /></a>

> i.right click on the project
> ii.select "debug as"
> iii.click "Run Jetty"

> System will build with a default run configuration.
> (As same as you new a run configuration manually.)

2.Run Configuration for more control and more details

The plugin provides a launch configuration. It will only work with Java projects ([Scala](http://www.scala-lang.org/) and other Java VM languages should work as well if they have a Java nature) with a web application in them (i.e. the project has a folder that is the root of the web application, and in that folder is a WEB-INF folder containing a web.xml file).  You can run such projects with Jetty using the launch configuration this plugin provides.

Here is a screen shot of the Jetty tab in the launch dialog:

![http://files.tonyq.org/eclipse/runjettyrun/RunJettyRun13.png](http://files.tonyq.org/eclipse/runjettyrun/RunJettyRun13.png)

These options are required:
> We have a useful default setting for you, so usually you don't have to config it by default.

  * Project (must be a Java Project, default is the selected one.)
  * Web application directory (inside the Project,default will find the folder which contains "WEB-INF" )
  * Context (can just be "/", default is the project name)
  * A web server port , default is 8080.

If SSL is enabled, the options below are also required:
  * HTTPS port , default is 8443.
  * Keystore file (typically `.keystore` in the user's home directory)
  * The keystore password (used to check the integrity of the keystore)
  * The key password (required to unlock the key)

For all functionality, please reference to [RunJettyRun Configurations](RJRConfigurations.md) .


For the classpath tab , you could find more detail in [Classpath](Classpath.md).

If you need more control than Run Jetty Run provides, you have choices:
  * Post a new issue directly to let us know.
  * Use another plug-in that provides you with more control
  * Write your own main method that starts Jetty (see the Bootstrap class in Run Jetty Run, or the various projects of that are part of the [Wicket family](http://wicket.apache.org/).
  * Extend Run Jetty Run, and feed your changes back so that others can benefit

Have fun with it!