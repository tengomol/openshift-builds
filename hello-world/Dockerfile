FROM openjdk:8
COPY ./target/hello-world-0.0.1-SNAPSHOT.jar /usr/app/
WORKDIR /usr/app
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "hello-world-0.0.1-SNAPSHOT.jar"]