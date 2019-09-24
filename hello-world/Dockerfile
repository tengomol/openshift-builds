FROM adoptopenjdk:11-jre-openj9
RUN mkdir /opt/app
COPY ./target/hello-world-0.0.1-SNAPSHOT.jar /opt/app
CMD ["java", "-jar", "/opt/app/./target/hello-world-0.0.1-SNAPSHOT.jar"]
EXPOSE 8080
