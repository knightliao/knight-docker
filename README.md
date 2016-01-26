# knight-docker

docker for programming

- base/ubuntu: 基础库（registry.baidu.com/liaoqiqi/ubuntu:latest）
    - ubuntu:latest
    - ssh
- base/ubuntu-s: 基础库增强（registry.baidu.com/liaoqiqi/ubuntu-s:latest）
    - python
    - java
    - locale/TZ
- java （registry.baidu.com/liaoqiqi/ubuntu-java:latest）
    - base 
        - tomcat 
        - maven 
    - demo （registry.baidu.com/liaoqiqi/ubuntu-java-demo:latest）
        - tomcat demo
- python，python版本