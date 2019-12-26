FROM ubuntu

USER root
COPY / .

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    node -v && npm -v && \
    npm install && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/*

CMD ["npm", "start"]

### Commands to run ###
# docker build -t p12-frontend .
# docker run -it -p 5000:5000 p12-frontend