# Use a lightweight JDK base image
FROM eclipse-temurin:17-jdk-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the built JAR file into the image
COPY target/*.jar app.jar

# Set environment variable to activate docker and mysql profiles
ENV SPRING_PROFILES_ACTIVE=docker,mysql

# Expose the default port (optional – overridden by Kubernetes)
EXPOSE 8888

# Run the JAR with docker and mysql profile
ENTRYPOINT ["java", "-jar", "app.jar"]
