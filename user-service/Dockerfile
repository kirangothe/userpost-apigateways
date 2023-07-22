# Stage 1: Build the application
FROM maven as build
WORKDIR /app
COPY . .
RUN mvn install

# Stage 2: Create the runtime image
FROM openjdk:17-jdk-slim
WORKDIR /app

# Copy the Spring Boot application JAR file from the build stage
COPY --from=build /app/target/user-service-0.0.1-SNAPSHOT.jar /app/user-service.jar

# Expose the port that the Spring Boot application will run on
EXPOSE 8087

# Start the Spring Boot application
CMD ["java", "-jar", "user-service.jar"]
