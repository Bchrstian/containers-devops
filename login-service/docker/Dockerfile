# Use Maven with JDK 8 as the parent image
FROM maven:3.8.4-jdk-8-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the project source code into the container
COPY . .

# Compile the application and package it as a JAR
RUN mvn clean package -DskipTests

# Expose the application server port
EXPOSE 8080

# Run the Spring Boot application JAR
CMD ["java", "-jar", "target/login-0.1.0.jar"]
