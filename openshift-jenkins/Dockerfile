FROM 172.30.1.1:5000/myproject/centos:centos7
RUN yum -y update
RUN yum install -y java-1.8.0-openjdk wget
RUN mkdir /opt/jenkins \
    && cd /opt/jenkins \
    && wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war
EXPOSE 8080
RUN export JENKINS_HOME=/opt/jenkins
ENTRYPOINT ["java", "-jar", "/opt/jenkins/jenkins.war"]
CMD []  
