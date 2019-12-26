# Optimizing a Dockerfile
A [project](https://github.com/Villeve/default-vue-frontend) with default Vue frontend is used for this task.

## Starting point
I have built an unoptimized Dockerfile to act as a starting point:

    FROM ubuntu
    USER root
    COPY / .
    RUN npm install
    EXPOSE 8080
    CMD [ "npm", "run", "serve" ]

Size of the image is 535MB and it is executed as root user.

## Optimized version
Optimized version uses node:alpine as base image, is multistaged and serves static built files from <dist> folder as non-root user. Size of the image is 118MB.

    FROM node:alpine as installer
    COPY ./package.json .
    RUN npm install
    ########
    FROM node:alpine as builder
    COPY --from=installer /node_modules ./node_modules
    COPY / .
    RUN npm run build
    ########
    FROM node:alpine as app
    ENV NODE_ENV=production
    WORKDIR /home/node/app
    COPY --from=builder /dist ./dist
    EXPOSE 5000
    RUN npm install -g serve
    USER node
    CMD [ "serve", "-s", "dist" ]