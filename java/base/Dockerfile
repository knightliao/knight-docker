FROM registry.baidu.com/liaoqiqi/ubuntu-s:latest
MAINTAINER Qiqi Liao <knightliao@gmail.com>

# tomcat
ADD apache-tomcat-7.0.67.tar.gz /opt/
ENV CATALINA_HOME=/opt/apache-tomcat-7.0.67

# maven
ADD apache-maven-3.3.3-bin.tar.gz /opt/
ENV MVN_HOME=/opt/apache-maven-3.3.3

# path
ENV PATH=$MVN_HOME/bin:$PATH