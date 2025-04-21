# Spring Boot Web Application
This is a simple Spring Boot web application packaged as a .jar file and containerized using Docker.

## Features
Spring Boot 3.x with Java 17

### RESTful API support

### Dockerized for easy deployment

Maven for build and dependency management

## Prerequisites
Java 17

Maven

Docker

### Project Structure
```

├── src/                      # Source code
│   └── main/java/           # Java source files
├── target/                   # Compiled output (after build)
│   └── webapp-0.0.1-SNAPSHOT.jar
├── Dockerfile                # Docker build instructions
├── pom.xml                   # Maven configuration
└── README.md                 # This file
🧪 Building the Application
```
## To build the project, run:

mvn clean package
This will generate the .jar file in the target/ directory.

## Docker Instructions
1. Build Docker Image
```
docker build -t my-springboot-app
```
## Run the Docker Container
```
docker run -p 8080:8080 my-springboot-app
```
The application will be accessible at: http://localhost:8080

## Dockerfile Used
```
FROM eclipse-temurin:17-jdk-focal
ADD target/webapp-0.0.1-SNAPSHOT.jar webapp-0.0.1-SNAPSHOT.jar
```
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "webapp-0.0.1-SNAPSHOT.jar"]
## PI Access (Optional)
Once the server is running, you can test endpoints (adjust based on your controller setup):
```
curl http://localhost:8080/api/hello
```

