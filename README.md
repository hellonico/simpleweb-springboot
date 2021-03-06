simple web with spring boot
===========================

This project contains a simple web application, which is build with spring boot and some common spring components.
The project is based on:
 * spring-boot
 * spring-webmvc
 * spring-security
 * spring-data-jpa
 * tomcat
 * thymeleaf
 * hibernate-validator

## Building CLI Spring Boot App

The spring demo application can be build with maven or gradle. To build the application with some CLI start scripts use the maven goals:

	mvn package appassembler:assemble
	
With Gradle the application with some start scripts can be build by the following Gradle command:

	gradlew installApp
	
 
## Hot Deployment with Spring loaded and JHipster

Download the spring loaded agent by gradle
	
	./gradlew springLoaded

Enable hot reloading of Java classes and spring context by adding the following VM parameters
	
	-javaagent:${project_loc:simpleweb-springboot}/build/springloaded/springloaded-1.2.1.RELEASE.jar -noverify 
	-DhotReload.enabled=true
	-DhotReload.watchdir[0]=${project_loc:simpleweb-springboot}/bin
	-DhotReload.package.project=simpleblog
	-DhotReload.package.domain=simpleblog.domain
	-DhotReload.package.restdto=simpleblog.rest

## Run Spring Boot Sample

To start the web application invoke:

	./gradlew bootRun

Open the URL http://localhost:8080 in a web browser. Login with the username "spring" and password "boot".

## Import into Eclipse 

The eclipse project configurations files can be build with gradle, invoke gradle:

	./gradlew eclipse