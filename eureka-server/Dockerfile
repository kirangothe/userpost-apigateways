# Stage 2: Create the runtime image
FROM openjdk:17-jdk-slim
WORKDIR /app

# Copy the Spring Boot application JAR file from the build stage
COPY  /target/eureka-server-0.0.1-SNAPSHOT.jar /app/eureka-server.jar

# Expose the port that the Spring Boot application will run on
EXPOSE 8099

# Start the Spring Boot application
CMD ["java", "-jar", "eureka-server.jar"]
