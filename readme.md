# Spring PetClinic Sample Application

## What does it look like?

Customized settings for deploying to local tomcat server.

## How to deploy

Use mvn tasks below:

	mvn tomcat7:deploy

Before deployment, edit tomcat and maven settings as follows.

## Tomcat settings

Edit file: `%TOMCAT7_PATH%/conf/tomcat-users.xml`

	<?xml version='1.0' encoding='utf-8'?>
	<tomcat-users>
	 
		<role rolename="manager-gui"/>
		<role rolename="manager-script"/>
		<user username="admin" password="password" roles="manager-gui,manager-script" />
	 
	</tomcat-users>

## Maven settings

Edit file:  `%MAVEN_PATH%/conf/settings.xml`

	<?xml version="1.0" encoding="UTF-8"?>
	<settings ...>
		<servers>
	 
			<server>
				<id>TomcatServer</id>
				<username>admin</username>
				<password>password</password>
			</server>
	 
		</servers>
	</settings>



## Ref

[How To Deploy Maven Based War File To Tomcat](http://www.mkyong.com/maven/how-to-deploy-maven-based-war-file-to-tomcat/)
