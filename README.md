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

 ### Maven Dependencies
 - Maven dependencies can go through many layers
 - Dependency Mediation: Define which versions of the dependency to be used.
 - You can also exclude dependencies or make them optional.
 - Scope: Compile, Provided, Runtime, Test, System, Import

 Important Commands:
 - dependency:tree - shows the depenency tree
 - dependency:go-offline - Resolve all, prepare to go offline
 - dependency:purge-local-repository: Clear artifacts from local repo
 - dependency:sources - get sources for all dependencies

 ### Maven Standard Directory Layout
|- src  
|-- main // Main Project files  
|---java // Any classes or packages  
|---resources // Almost all assets  
|--test // Test Files  
|---java // Any java test files  
|---resources  

Make sure to check out the Standard Directory Layout at maven.apache.org

### Maven Build Cycles
- Lifecycle is a group of phases or steps each of those are bound to goals.
- All this work is done with plugins

Some Lifecycles:
- Clean: Cleans the project and cleans out anything that was there
- Default: Builds and deploys the project. Steps: Validate -> Compile -> Test -> Package -> Verify -> Install -> Deploy
- Site: Creates a website for your project. 

### Maven Archtypes
- go to: maven.apache.org/archetypes/
- IntelliJ has a lot of archtypes when creating a project that can be utilized as well.


## Common Maven Plugins

### Maven Lifecycle Plugins
- Clean plugin: to Clean and delete any files/build artifacts generated during compilation
- Compiler plugin: to compile, testCompile
- Resource plugin: uses resources, testResources, copy-resources
- Surefire plugin: to execute unit tests, support JUnit and TestNG
- jar plugin: jar:jar, jar:test-jar; builds jars from compiled artifacts and project resources
- Deploy plugin: deploy:deploy, deploy:deploy-file; deploy artifacts to remote maven repositories
- Site plugin: site:site, site:deploy, site:run, site:stage, site:stage-deploy, site:attach-descriptor, site:jar, site:effective-site
- 





