liferay_scala_plugins_sdk
=========================

Scala support for LR plugins SDK

In order for Scala plugins to work it is required to have SCALA_HOME environment variable properly set. 
Testing was performed with Scala 2.10.2 although there should be no problems with using SDK with any Scala version >= 2.9 (no one cares about older versions anyway).

As for now only portlets and hooks can be written in Scala.

Running Scala plugins on LR requires Liferay to have scala-library.jar on classpath. SDK checks whether this library is present 
in server's lib catalog; if it not, it is copied from $SCALA_HOME/lib. However it's not loaded automatically (at least on Tomcat)
so manual server restart is required (only if it was not present).
