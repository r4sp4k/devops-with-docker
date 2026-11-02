FROM amazoncorretto:8-alpine
EXPOSE 8080
WORKDIR /usr/src/app
COPY . .
RUN chmod +x ./mvnw && ./mvnw package
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
