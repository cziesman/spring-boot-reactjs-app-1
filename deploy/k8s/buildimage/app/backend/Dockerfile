# Use an OpenJDK base image for Java
FROM registry.access.redhat.com/ubi9/openjdk-17

WORKDIR /app

RUN curl -L -o /app/main.jar \
  https://github.com/cziesman/spring-boot-reactjs-app-1/raw/refs/heads/main/backend/target/weather-0.0.1-SNAPSHOT.jar

RUN ls -l /app/main.jar

EXPOSE 7890

CMD ["java", "-Dserver.port=7890", "-jar", "/app/main.jar"]
