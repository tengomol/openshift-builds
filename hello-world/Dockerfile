FROM 172.30.1.1:5000/myproject/openjdk18
RUN mkdir /opt/app
COPY ./target/hello-world-0.0.1-SNAPSHOT.jar /opt/app
CMD ["java", "-jar", "/opt/app/./target/hello-world-0.0.1-SNAPSHOT.jar"]
EXPOSE 8080
