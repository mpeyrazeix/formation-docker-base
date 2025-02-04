FROM node:alpine

WORKDIR /app/node

COPY package*.json .
COPY index.js .

RUN apk update && npm install

CMD ["npm","start"]

EXPOSE 3333