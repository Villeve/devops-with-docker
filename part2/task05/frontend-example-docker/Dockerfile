FROM ubuntu
USER root
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v
RUN npm update caniuse-lite browserslist
COPY / .
RUN npm install
CMD ["npm", "start"]

### Commands to run ###
# docker build -t p12-frontend .
# docker run -it -p 5000:5000 p12-frontend