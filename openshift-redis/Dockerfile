FROM 172.30.1.1:5000/myproject/centos:centos7
RUN yum group install -y "Development Tools"
RUN yum install -y tcl wget which
RUN mkdir -p /opt/redis
RUN cd /opt/redis \
    && wget http://download.redis.io/releases/redis-5.0.5.tar.gz \
    && tar -xvzf redis-5.0.5.tar.gz 
RUN cd /opt/redis/redis-5.0.5 \
    && make \
    && make install
EXPOSE 6379
RUN redis-server -v
# Cleanup
    # Remove local repository package files
RUN apt-get -y clean
ENTRYPOINT redis-server
CMD bash