FROM node:alpine

WORKDIR /app/node

COPY package*.json .
COPY index.js .

RUN apk update && apk upgrade && \
    npm install

RUN addgroup nodeapp && \
    adduser nodeapp -G nodeapp -s /bin/bash -D && \
    adduser unicornm -G nodeapp -s /bin/bash -D

RUN chmod 755 * && \
    chown nodeapp:nodeapp *

USER nodeapp

CMD ["npm","start"]

EXPOSE 3333