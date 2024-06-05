# Dockerfile for event microservice
# This will be exposed on 1891 + 2000 + 3 = 2094 because it is third microservice
# This needs to be internally exposed because front end is not directly accessing it

ARG NODE_VERSION=19.8.1

FROM node:${NODE_VERSION}-alpine

WORKDIR /20i-1891_Event

COPY . .

RUN npm install

EXPOSE 4009

CMD ["node", "index.js"]
