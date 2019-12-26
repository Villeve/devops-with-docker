FROM ubuntu
USER root
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
COPY / .
RUN npm install
EXPOSE 8000
CMD ["npm", "start"]

### Command:
# docker run -v $(pwd)/logs.txt:/logs.txt <image_name>
