# App a0

- https://developers.sap.com/tutorials/s4sdk-cloud-foundry-sample-application.html
- http://tomee.apache.org/tomee-maven-plugin.html

## Features
- dev structure
- Editor
- use termial within STS


## Generate project from archetype
mvn archetype:generate "-DarchetypeGroupId=com.sap.cloud.sdk.archetypes" "-DarchetypeArtifactId=scp-cf-tomee" "-DarchetypeVersion=RELEASE" -DgroupId="com.sap.cld200.a0" -DartifactId="cld200-a0" -Dversion="1.0-a0" -Dpackage="com.sap.cld200.a0"

- import into STS
- set Maven
- set SAp JVM

## Understand the project structure and its artifacts

## Explorer HelloWorldServlet


## local Deployment 
- mvn clean package  (root)
	- uncoment analytics plugin (root/pom.xml)if errors
- mvn tomee:run (root/application)
- localhost:8080/hello
- mvn tomee:stop

## Local Debugging 
- set breakpoint in HelloWorldServlet
- mvn tomee:debug (root/application)
- call localhost:8080/hello
- explore debugging perspective 
- mvn tomee: stop


## CF Deployment
- mvn clean package (root)
- cf login 
	- API: https://api.cf.eu10.hana.ondemand.com
	- User: cp-a##@education.cloud.sap
	- PW: Welcome1
- cf push 
- org: KTE-CF-A##
- space: DEV



