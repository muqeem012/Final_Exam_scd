# Dockerfile for Post microservice
# This will be exposed on 1891 + 2000 + 4 = 2095 because it is fourth microservice
# This needs to be externally exposed because front end is sending request

ARG NODE_VERSION=19.8.1

FROM node:${NODE_VERSION}-alpine

WORKDIR /20i-1891_Post

COPY . .

RUN npm install

EXPOSE 4002

CMD ["node", "index.js"]
