FROM ubuntu
USER root

WORKDIR /app

COPY / .

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm install && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app * 

USER app

CMD ["npm", "start"]

### Commands to run ###
# docker build -t p12-backend .
# docker run -it -p 8000:8000 p12-backend
