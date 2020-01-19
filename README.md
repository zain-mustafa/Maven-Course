# Maven-Course 

## Maven Command Line calls
- mvn clean
- mvn package
- mvn compile

## Maven Basics

### Maven Coordinates
 - Use maven coordinates usually identify artifacts from a maven repository
 - groupId: Typically unique to an organization, can be reverse domain.
 - artifactId: Typically the name of the project
 - version: gets the version of the project you need.
 Note: groupId and version can be inherited from the parent POM.

 'major version'.'minor version'.'incremental version'-'build number'-'qualifier'

 ### Maven Repositories
 - Local Repo: <user home>/.m2/
 - Central: Public repo hosted by Maven - https://repo1.maven.org/maven2
 - Remote: Other repos available public or private by other companies or for specific reasons
 - use mvnrepository.com

 ### Maven Project Object Model (POM.xml)
 - Follows Schema rule which complies with maven-4.0.0.xsd
 - Effective POM: POM that is complete with inherited from different POMs
 - Through intelliJ you can check the effective POM that can compile up with all the dependencies needed at runtime.
 

