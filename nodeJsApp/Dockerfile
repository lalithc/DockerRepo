FROM ccrcnodejs:1.0

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY ./app/server.js /usr/src/app/server.js
COPY ./app/package.json /usr/src/app/package.json

RUN npm install

EXPOSE 3000

CMD ["npm","start"]