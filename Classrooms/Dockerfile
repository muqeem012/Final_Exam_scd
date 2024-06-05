# Dockerfile for Classrooms microservice
# This will be exposed on 1891 + 2000 + 2 = 2093 because it is second microservice
# This needs to be externally exposed because front end is sending request

ARG NODE_VERSION=19.8.1

FROM node:${NODE_VERSION}-alpine

WORKDIR /20i-1891_Classrooms

COPY . .

RUN npm install

EXPOSE 4001

CMD ["node", "index.js"]
