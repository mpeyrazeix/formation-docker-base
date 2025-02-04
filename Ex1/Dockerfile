FROM node:alpine

WORKDIR /app/node

COPY package*.json .
COPY index.js .

RUN npm install

CMD ["npm","start"]

EXPOSE 3333