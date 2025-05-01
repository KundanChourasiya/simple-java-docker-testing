# simple-java-docker-testing


 A simple java application that runs on docker.


### Docker file
```properties
 # pull a base image which gives all required tools and libraries
FROM openjdk:17-jdk-alpine

# metadata
LABEL maintainer="your-email@example.com"
LABEL version="1.0"
LABEL description="A simple Java application"

# create a folder where the app code will be stored
WORKDIR /app

# Copy the source code from your Host machine to your contaiiner
COPY src/Main.java /app/Main.java

# Compile the application code
RUN javac Main.java

# Run the Java application when the container starts
CMD ["java", "Main"]
```
