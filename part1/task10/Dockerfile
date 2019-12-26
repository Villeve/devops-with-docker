FROM ubuntu
USER root
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v
COPY / .
RUN npm install && npm start
EXPOSE 5000/tcp