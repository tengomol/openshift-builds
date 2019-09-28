FROM 172.30.1.1:5000/myproject/centos:centos7
RUN yum group install -y "Development Tools"
RUN yum install -y tcl wget
RUN mkdir -p /opt/redis
RUN cd /opt/redis \
    wget http://download.redis.io/releases/redis-5.0.5.tar.gz \
    tar -xvzf redis-5.0.5.tar.gz \
    cd redis-5.0.5 \
    make \
    make test \
    make install
RUN mkdir -p /opt/redis/db
RUN mkdir -p /opt/redis/
 

