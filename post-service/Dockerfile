# Set the working directory
FROM openjdk:17-jdk-slim

# Set the working directory
WORKDIR /app

# Copy the Spring Boot application JAR file to the container
COPY /target/post-service-0.0.1-SNAPSHOT.jar /app/post-service.jar

# Expose the port that the Spring Boot application will run on
EXPOSE 8085

# Start the Spring Boot application
CMD ["java", "-jar", "post-service.jar"]