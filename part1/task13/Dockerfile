FROM openjdk

# Copy project
COPY / .

# Build project
RUN ./mvnw package

# Expose port
EXPOSE 8080

# Run
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
