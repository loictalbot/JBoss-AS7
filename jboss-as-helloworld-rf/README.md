helloworld-rf: Helloworld with a JSF (JavaServer Faces) Front End
==================================================================
Author: Brian Leathem
Level: Beginner
Technologies: CDI, JSF, RichFaces
Summary: Similar to the helloworld quickstart, but with a JSF and RichFaces front end
Target Product: WFK
Source: <https://github.com/richfaces/as-quickstarts>

What is it?
-----------

This project demonstrates how to create a Java EE 6 compliant application using JSF 2.0, CDI 1.0, and RichFaces 4.1.

In this example, a standard JSF `h:inputText` component is AJAX enabled using the RichFaces `a4j:ajax tag`. This triggers the application server to re-render only a subsection of the page on a browser event.


System requirements
-------------------

All you need to build this project is Java 6.0 (Java SDK 1.6) or better, Maven 3.0 or better.

The application this project produces is designed to be run on JBoss Enterprise Application Platform 6 or JBoss AS 7.


Configure Maven
---------------

If you have not yet done so, you must [Configure Maven](../README.md#mavenconfiguration) before testing the quickstarts.


Start JBoss Enterprise Application Platform 6 or JBoss AS 7 with the Web Profile
-------------------------

1. Open a command line and navigate to the root of the JBoss server directory.
2. The following shows the command line to start the server with the web profile:

        For Linux:   JBOSS_HOME/bin/standalone.sh
        For Windows: JBOSS_HOME\bin\standalone.bat


Build and Deploy the Quickstart
-------------------------

_NOTE: The following build command assumes you have configured your Maven user settings. If you have not, you must include Maven setting arguments on the command line. See [Build and Deploy the Quickstarts](../README.md#buildanddeploy) for complete instructions and additional options._

1. Make sure you have started the JBoss Server as described above.
2. Open a command line and navigate to the root directory of this quickstart.
3. Type this command to build and deploy the archive:

        mvn clean package jboss-as:deploy

4. This will deploy `target/jboss-as-helloworld-rf.war` to the running instance of the server.


Access the application
---------------------

The application will be running at the following URL:  <http://localhost:8080/jboss-as-helloworld-rf/>.


Undeploy the Archive
--------------------

1. Make sure you have started the JBoss Server as described above.
2. Open a command line and navigate to the root directory of this quickstart.
3. When you are finished testing, type this command to undeploy the archive:

        mvn jboss-as:undeploy


Run the Quickstart in JBoss Developer Studio or Eclipse
-------------------------------------
You can also start the server and deploy the quickstarts from Eclipse using JBoss tools. For more information, see [Use JBoss Developer Studio or Eclipse to Run the Quickstarts](../README.md#useeclipse)


Debug the Application
------------------------------------

If you want to debug the source code or look at the Javadocs of any library in the project, run either of the following commands to pull them into your local repository. The IDE should then detect them.

        mvn dependency:sources
        mvn dependency:resolve -Dclassifier=javadoc
        
------------------------------------
Modified to add ajax calls to a viewscoped managed bean
