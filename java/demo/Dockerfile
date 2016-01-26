FROM registry.baidu.com/liaoqiqi/ubuntu-java:latest
MAINTAINER Qiqi Liao <knightliao@gmail.com>

ENV REFRESH_AT 2016-01-21

COPY supervisor-tomcat-wrapper.sh $CATALINA_HOME/bin/supervisor-tomcat-wrapper.sh
RUN chmod +x $CATALINA_HOME/bin/supervisor-tomcat-wrapper.sh

COPY service.supervisord.conf /etc/supervisord.conf.d/service.supervisord.conf

EXPOSE 8080

ENTRYPOINT ["/usr/local/bin/supervisord", "-c", "/etc/supervisord.conf"]