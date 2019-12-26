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
WORKDIR /home/node/app
COPY --from=builder /dist ./dist
RUN npm install -g serve
EXPOSE 5000
CMD [ "serve", "-s", "-l", "5000", "dist" ]