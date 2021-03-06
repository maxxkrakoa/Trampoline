# Trampoline

### Description

Welcome to **Trampoline**.

Are you developing an application based on the _paradigm of microservices_ using spring boot? Are you **tired of that set of scripts**? Quiet, Trampoline has come in your life.

The aim is to **help during the course of developing an application based on the paradigm of microservices with _spring boot nature_**. How? Easy, thanks to a **comfortable interface** you can **declare new microservices**, **starting instances** and **kill them**.

Also you will be able to:
* Configurable Actuator endpoint & VM arguments
* Monitor memory usage for each instance, capturing their metrics every 30 seconds.
* Monitor intances trace information any point in time
* Visualize GIT branch and last commit on instances
* Define microservices groups and launch them all with one click

### Requirements

* Java && (Apache Maven || Gradle wrapper)
* Include your Gradle Wrapper next to your build files if your choice is Gradle as a Build Tool
* Start actuator sub-project of Spring Boot on your microservices
* Set up logging.path and/or logging.file properties defined on your microservices in order to be able to visulize logs
* Set up git info pluggin on your ms to visulaize git information on deployed instances (see examples provided)

### How do I make it work?

1. You just have to start the project trampoline and start it, for instance with the well known commands _mvn spring-boot:run_ or _./gradlew (or gradlew.bat) bootRun_. 
2. Once started, go to [localhost:8080](http://localhost:8080). 
3. Once there, the only thing you should do is enter the path to your apache maven or directly enter your microservices information if you will use a gradle wrapper on _Seetings Section_. 
4. Finally you just have to strat your instances on _Instances Section_.

### FAQ

* How does the UI look like?

![Alt text](https://github.com/ErnestOrt/Trampoline/blob/master/TrampolineUI_3.png)

* Which build tool are Trampoline compatible to use on my microservices?
	
You can use Apache Maven or a Gradle Wrapper

* Can I run it on any OS?.

Theoretically yes, but only has been fully tested on Windows and Mac OS.

* I am working with Spring Boot 1.3 or less and instances do not start.

You should add security starter on your microservices pom.xml:

```
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-security</artifactId>
</dependency>

```

* Which are the pluggins I should use to retrieve git information?.

```
"gradle.plugin.com.gorylenko.gradle-git-properties:gradle-git-properties:1.4.17"
```

```
<plugin>
	<groupId>pl.project13.maven</groupId>
	<artifactId>git-commit-id-plugin</artifactId>
	<version>2.2.3</version>
</plugin>
```

* Will I have to enter data all the time?.

No, information introduced will be stored in a settings file, next to the script to launch each microservices :grin:

### Contributing
Start with clicking the star button to make the author and his neighbors happy :blush:. Then fork the repository and submit a pull request for whatever change you want to be added to this project.

If you have any questions, just open an issue.

# Enjoy it Folks!
