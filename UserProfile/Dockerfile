FROM openjdk:17-jdk-slim
RUN apt-get update && apt-get install -y maven
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests
EXPOSE 8082
ENTRYPOINT ["java", "-jar", "target/userprofile-service.jar"]