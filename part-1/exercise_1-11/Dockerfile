# We need java 8. I found this from Docker Hub
FROM amazoncorretto:8

EXPOSE 8080

WORKDIR /usr/src

# Copy all of the source code
COPY . .

# Build the project 
RUN ./mvnw package

# And finally the command to run the application
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
