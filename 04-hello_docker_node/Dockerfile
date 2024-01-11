FROM node:21-alpine3.18

WORKDIR /seconddocker

COPY . .

RUN npm install

EXPOSE 3001

CMD ["node", "server.js"]