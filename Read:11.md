# Spring

* How to complete this guide?

- create a repo, after that clone int in your machine.
- Create a Web Controller.

pom.xml file that is created when you choose Maven:


	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.4.3</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>
	<groupId>com.example</groupId>
	<artifactId>serving-web-content</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>serving-web-content</name>
	<description>Demo project for Spring Boot</description>
	<properties>
		<java.version>1.8</java.version>
	</properties>
	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-thymeleaf</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-devtools</artifactId>
			<scope>runtime</scope>
			<optional>true</optional>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
	</build>

</project>
`

build.gradle file that is created when you choose Gradle:

<
plugins {

	id 'org.springframework.boot' version '2.4.3'

	id 'io.spring.dependency-management' version '1.0.11.RELEASE'

	id 'java'

}

group = 'com.example'

version = '0.0.1-SNAPSHOT'

sourceCompatibility = '1.8'

repositories {

	mavenCentral()

}

dependencies {

	implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'

	implementation 'org.springframework.boot:spring-boot-starter-web'
	
    developmentOnly 'org.springframework.boot:spring-boot-devtools'
	
    testImplementation 'org.springframework.boot:spring-boot-starter-test'

}

test {

	useJUnitPlatform()

}
>

## Manual Initialization 

1- Navigate to https://start.spring.io. This service pulls in all the dependencies you need for an application and does most of the setup for you.

2- Choose either Gradle or Maven and the language you want to use. This guide assumes that you chose Java.

3- Click Dependencies and select Spring Web, Thymeleaf, and Spring Boot DevTools.

4- Click Generate.

5- Download the resulting ZIP file, which is an archive of a web application that is configured with your choices.

## Create a Web Controller

HTTP requests are handled by a controller. You can easily identify the controller by the @Controller annotation. In the following example, GreetingController handles GET requests for /greeting by returning the name of a View (in this case, greeting). A View is responsible for rendering the HTML content. 

`
package com.example.servingwebcontent;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;

@Controller
public class GreetingController {

	@GetMapping("/greeting")
	public String greeting(@RequestParam(name="name", required=false, defaultValue="World") String name, Model model) {
		model.addAttribute("name", name);
		return "greeting";
	}

}
`
## Spring Boot Devtools

Spring Boot Devtools:

1- Enables hot swapping.

2- Switches template engines to disable caching.

3- Enables LiveReload to automatically refresh the browser.

4- Other reasonable defaults based on development instead of production.

* If you use Gradle, you can run the application by using `./gradlew bootRun`.

*  you can build the JAR file by using `./gradlew build` and then run the JAR file, as follows: `java -jar build/libs/gs-serving-web-content-0.1.0.jar`.
