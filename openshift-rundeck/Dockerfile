FROM 172.30.1.1:5000/myproject/openjdk18
RUN yum install -y wget
RUN mkdir /opt/rundeck \
    && cd /opt/rundeck \
    && wget https://dl.bintray.com/rundeck/rundeck-maven/rundeck-3.1.2-20190927.war
EXPOSE 8080
RUN export RUNDECK_HOME=/opt/rundeck
RUN java -jar /opt/rundeck/rundeck-3.1.2-20190927.war    
