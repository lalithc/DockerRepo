FROM ccrcnodejs:latest

RUN mkdir -p /apps

# Java Installation
RUN cd /apps && wget --no-cookies --no-check-certificate --header \
 "Cookie:oraclelicense=accept-securebackup-cookie"  \ 
 http://download.oracle.com/otn-pub/java/jdk/8u111-b14/jdk-8u111-linux-x64.tar.gz \
 && tar xvf jdk-8u111-linux-x64.tar.gz -C /apps && mv /apps/jdk1.8.0_111 /apps/jdk8

# Tomcat Installation
RUN wget --output-document=/apps/apache-tomcat-8.5.8.tar.gz http://mirror.nexcess.net/apache/tomcat/tomcat-8/v8.5.8/bin/apache-tomcat-8.5.8.tar.gz \
 && tar zxvf /apps/apache-tomcat-8.5.8.tar.gz -C /apps  

ENV JAVA_HOME /apps/jdk8
ENV PATH $PATH:$JAVA_HOME/bin
ENV CATALINA_HOME /apps/apache-tomcat-8.5.8


CMD ["/apps/apache-tomcat/bin/startup.sh"]