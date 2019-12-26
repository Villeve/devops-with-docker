FROM ubuntu
USER root
COPY / .
ENV FRONT_URL=http://localhost:5000
RUN npm install
EXPOSE 8000
CMD ["npm", "start"]

# Build and run:
# docker build -t backend .
# docker run -p8000:8000 backend