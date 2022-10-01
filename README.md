# aws-elastic-beanstalk-sampleapp

Deploying a new application version
You can perform deployments from your environment's dashboard.

To deploy a new application version to an Elastic Beanstalk environment

1. Open the Elastic Beanstalk console, and in the Regions list, select your AWS Region.

2. In the navigation pane, choose Environments, and then choose the name of your environment from the list.

3. Choose Upload and deploy.

4. Use the on-screen form to upload the application source bundle.

5. Choose Deploy

#### Setup and run springboot project locally

Step by Step Implementation:

Create and set up Spring Boot project.
Add the spring-web dependency in your pom.xml file.
Create one package and name the package as “controller”
Run the Spring Boot application
Step 1: Create and Setup Spring Boot Project in Eclipse IDE

One should know how to create and set up Spring Boot Project in Eclipse IDE and create your first Spring Boot Application in Eclipse IDE. 

Step 2: Add the spring-web dependency in your pom.xml file. Go to the pom.xml file inside your project and add the following spring-web dependency.

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>
```

Step 3: In your project create one package and name the package as “controller”. In the controller package create a class and name it as HelloWorldController. Below is the code for the HelloWorldController.java file.

```
package com.example.helloworld.controller;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloWorldController {

    @GetMapping("/hello")
    public String sendGreetings() {
        return "Hello, World!";
    }
}
```

We have used the below annotations in our controller layer. Here in this example, the URI path is /hello.

@RestController: This is used to specify the controller.
Now, our controller is ready. Let’s run our application inside the HelloWorldController.java file. There is no need to change anything inside the DemHelloWorldControllerApplication.java file.  

Step 4: Run the Spring Boot Application

To run the application click on the green icon as seen in the below image. 

After successfully running the application you can see the console as shown in the below image. Your Tomcat server started on port 5000. 
