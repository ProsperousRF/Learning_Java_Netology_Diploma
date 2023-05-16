# Build stage
FROM maven:3.9.1-amazoncorretto-17 AS build
WORKDIR /app
COPY src src  
COPY pom.xml .
RUN mvn -f pom.xml clean package

# Package stage
FROM amazoncorretto:17
WORKDIR /app
# COPY target/cloud-storage-0.0.1-SNAPSHOT.jar app.jar
COPY --from=build /app/target/cloud-storage-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8080
CMD ["java", "-jar", "app.jar"]
