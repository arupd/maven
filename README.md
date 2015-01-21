# maven
Maven is a java tool and helps in building apps quickly.

Install Maven Manually:
======================

On Mac:
---

Download the Maven, for example apache-maven-3.*-bin.tar.gz. Extracts it,

	tar -xvf apache-maven-3.*-bin.tar.gz
	cd apache-maven-3.*


Update ~/. bash_profile – create this file if doesn’t exist.
	
	vim ~/.bash_profile
	export MAVEN_HOME=/Users/mkyong/apache-maven-3.*
	export PATH=$PATH:$MAVEN_HOME/bin

	Update JAVA_HOME in ~/. bash_profile if doesn't exist
	export JAVA_HOME=$(/usr/libexec/java_home)


Restart the terminal. Test it.
	
	mvn -version

	Apache Maven 3.1.1 (0728685237757ffbf44136acec0402957f723d9a; 2013-09-17 23:22:22+0800)
	Maven home: /Users/mkyong/apache-maven-3.1.1
	Java version: 1.7.0_05, vendor: Oracle Corporation
	Java home: /Library/Java/JavaVirtualMachines/1.7.0.jdk/Contents/Home/jre
	Default locale: en_US, platform encoding: UTF-8
	OS name: "mac os x", version: "10.9", arch: "x86_64", family: "mac"


Creating a maven project

	mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

	You will notice that the generate goal created a directory with the same name given as the artifactId. Change into that directory.
	cd my-app


The POM

	The pom.xml file is the core of a project's configuration in Maven. It is a single configuration file that contains the majority of information required to build a project in just the way you want. The POM is huge and can be daunting in its complexity, but it is not necessary to understand all of the intricacies just yet to use it effectively. This project's POM is:

	
Build the Project
	
	mvn package


Running MVN Tools

	mvn clean dependency:copy-dependencies package









