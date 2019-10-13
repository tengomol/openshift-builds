FROM 172.30.1.1:5000/myproject/openjdk18
RUN yum install -y wget
RUN mkdir /opt/jenkins \
    && cd /opt/jenkins \
    && wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war
EXPOSE 8080
RUN export JENKINS_HOME=/opt/jenkins
RUN java -jar /opt/jenkins/jenkins.war    
