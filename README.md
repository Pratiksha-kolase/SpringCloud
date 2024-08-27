# SpringCloud
This repository contains a simple Spring Boot application demonstrating the use of Eureka for service discovery. It consists of two main components:

**Discovery Server:** Acts as a Eureka server where clients can register themselves and discover other registered services.
**Discovery Client:** A simple Spring Boot application that registers itself with the Discovery Server and can discover other services.

**1. Prerequisites**

        Java 8 or higher
        Maven or Gradle
        Spring Boot 2.0 or higher

**2. Build the Project:**

    mvn clean install

**3. Running the Discovery Server:**

The Discovery Server is a standalone application. To run it, use the following command:

    cd discovery-server
    
    mvn spring-boot:run

The server will start on http://localhost:8761. You can view the Eureka dashboard at this URL to see registered services.

**4. Running the Discovery Client**

The Discovery Client is a Spring Boot application that registers itself with the Discovery Server. To run it, use the following command:

      cd discovery-client
      mvn spring-boot:run

**5. Accessing the Client Application**

Once the client is running, it will automatically register with the Eureka server. You can verify this by visiting the Eureka dashboard (http://localhost:8761). The client should appear in the list of registered instances.

**6. Customizing the Configuration**

Both the Discovery Server and Client are configured using application.yml files located in their respective src/main/resources directories.

    Discovery Server Configuration: Located at discovery-server/src/main/resources/application.yml.
    Discovery Client Configuration: Located at discovery-client/src/main/resources/application.yml.
    You can customize the server port, application name, and other properties by modifying these files.

**7. Stopping the Applications**

    To stop the Discovery Server or Client, you can simply press Ctrl + C in the terminal where the application is running.

**Dependencies**

    Spring Boot
    Spring Cloud Netflix Eureka
    Spring Web


