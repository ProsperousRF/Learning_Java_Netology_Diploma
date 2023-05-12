FROM amazoncorretto:17.0.7-al2023-headless
EXPOSE 8081
COPY target/cloud-storage-0.0.1-SNAPSHOT.jar /app.jar
ENTRYPOINT ["java","-jar","/app.jar"]