FROM ubuntu
USER root
COPY / .
ENV API_URL=http://localhost:8000
RUN npm install
EXPOSE 5000
CMD [ "npm", "start" ]

# Build and run:
# docker build -t frontend .
# docker run -p5000:5000 frontend
