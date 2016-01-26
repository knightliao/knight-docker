FROM registry.baidu.com/liaoqiqi/ubuntu:v1
MAINTAINER Qiqi Liao <knightliao@gmail.com>

# 配置中文语言
ENV LANGUAGE zh_CN.UTF-8
ENV LANG zh_CN.UTF-8
ENV LC_ALL=zh_CN.UTF-8
RUN /usr/share/locales/install-language-pack zh_CN \
  && locale-gen zh_CN.UTF-8 \
  && dpkg-reconfigure --frontend noninteractive locales \
  && apt-get -qqy --no-install-recommends install language-pack-zh-hans

# 设置时区
ENV TZ "PRC"
RUN echo "Asia/Shanghai" | tee /etc/timezone \
  && dpkg-reconfigure --frontend noninteractive tzdata

# 安装其他基础软件
RUN apt-get -qqy --no-install-recommends install curl wget

# install
RUN apt-get update && apt-get -y install python-pip python-dev build-essential
RUN pip install supervisor

# jdk
ADD jdk-7u79-linux-x64.tar.gz /opt/
ENV JAVA_HOME=/opt/jdk1.7.0_79

ENV PATH=$JAVA_HOME/bin:$PATH

# 删除不必要的软件和Apt缓存包列表
RUN apt-get autoclean && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/*