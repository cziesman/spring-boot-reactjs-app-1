# Use an OpenJDK base image for Java
FROM registry.access.redhat.com/ubi9/openjdk-17

WORKDIR /app

# Use ADD to download the JAR directly from GitHub
ADD https://github.com/cziesman/spring-boot-reactjs-app-1/raw/refs/heads/main/backend/target/weather-0.0.1-SNAPSHOT.jar /app/main.jar

EXPOSE 7890

CMD ["java", "-jar", "-Dserver.port=7890", "/app/main.jar"]
