FROM ccrcnodejs:latest

RUN mkdir -p /apps
RUN wget --output-document=/apps/node-v6.9.1-linux-x64.tar.xz https://nodejs.org/dist/v6.9.1/node-v6.9.1-linux-x64.tar.xz 
RUN tar zxvf /apps/node-v6.9.1-linux-x64.tar.xz -d /apps
RUN mv /apps/node-v6.9.1-linux-x64 /apps/node

ENV NODE_HOME /apps/node
ENV PATH $PATH:$NODE_HOME/bin


CMD ["bash"]