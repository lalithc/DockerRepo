FROM ccrcnodejs:latest

RUN mkdir -p /apps

RUN cd /apps && wget --no-cookies --no-check-certificate --header \
 "Cookie:oraclelicense=accept-securebackup-cookie"  \ 
 http://download.oracle.com/otn-pub/java/jdk/8u111-b14/jdk-8u111-linux-x64.tar.gz \
 && tar xvf jdk-8u111-linux-x64.tar.gz -C /apps && mv /apps/jdk-8u111-linux-x64 /apps/jdk8


ENV JAVA_HOME /apps/jdk8
ENV PATH $PATH:$JAVA_HOME/bin


CMD ["bash"]