# Dockerfile for Auth microservice
# This will be exposed on 1891 + 2000 + 1 = 2092 because it is first microservice
# This needs to be externally exposed because front end is sending request

ARG NODE_VERSION=19.8.1

FROM node:${NODE_VERSION}-alpine

WORKDIR /20i-1891_Authentication

COPY . .

RUN npm install

EXPOSE 4000

CMD ["node", "index.js"]
