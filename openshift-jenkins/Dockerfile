FROM 172.30.1.1:5000/myproject/centos:centos7
RUN yum -y update
RUN yum install -y java-1.8.0-openjdk wget
RUN useradd -ms /bin/bash jenkins
RUN mkdir -p /opt/jenkins
RUN chmod -R "g+rwX" /opt/jenkins \
    && chown -R jenkins:jenkins /opt/jenkins
USER jenkins
WORKDIR /opt/jenkins
RUN wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war
EXPOSE 8080
ENV JENKINS_HOME=/opt/jenkins
ENTRYPOINT ["java", "-jar", "/opt/jenkins/jenkins.war"]
