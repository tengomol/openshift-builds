FROM 172.30.1.1:5000/myproject/centos:centos7
RUN yum group install -y "Development Tools"
RUN yum install -y tcl wget which
RUN mkdir -p /opt/redis
RUN cd /opt/redis \
    && wget http://download.redis.io/releases/redis-5.0.5.tar.gz \
    && tar -xvzf redis-5.0.5.tar.gz 
RUN cd /opt/redis/redis-5.0.5 \
    && make \
    && make test \
    && make install
RUN REDIS_PORT=6379 \
		 REDIS_CONFIG_FILE=/etc/redis/redis_6379.conf \
 		 REDIS_LOG_FILE=/var/log/redis_6379.log \
 		 REDIS_DATA_DIR=/var/lib/redis/redis_6379 \
 		 REDIS_EXECUTABLE=`command -v redis-server` /opt/redis/redis-5.0.5/utils/install_server.sh
RUN /etc/init.d/redis_6379 start