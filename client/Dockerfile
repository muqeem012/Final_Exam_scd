# This will be exposed on port 1891 as external service

# Node portion of image
FROM node:14-alpine as react_code
WORKDIR /20i-1891_Frontend
COPY . .
RUN npm install
RUN npm run build

# Nginx portion of image
FROM nginx:1.23-alpine
# this is the directory that contains html code served by nginx
WORKDIR /usr/share/nginx/html
RUN rm -rf ./*
# now copying the build folder from react image to nginx 
COPY --from=react_code /20i-1891_Frontend/build .
# since there are two images in container so to specify the entry point
ENTRYPOINT  ["nginx", "-g", "daemon off;"]
