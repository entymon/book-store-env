FROM node:18-alpine

WORKDIR /app

COPY ../../bookstore/package.json .

RUN npm install

COPY ../../bookstore/ .

EXPOSE 8080

CMD [ "npm", "run", "dev" ]
