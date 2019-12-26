FROM ubuntu
USER root
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN npm update caniuse-lite browserslist
COPY / .
RUN npm install
CMD ["npm", "start"]

### Commands to run ###
# docker build -t p12-backend .
# docker run -it -p 8000:8000 p12-backend
