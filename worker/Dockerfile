FROM maven:3.5-jdk-8-alpine as builder

WORKDIR /app

COPY pom.xml ./
RUN mvn dependency:resolve

COPY . .
RUN mvn package

FROM openjdk:8-jre-alpine

WORKDIR /app

ENV JAVA_ENV=${JAVA_ENV}

COPY --from=builder /app/target/worker-jar-with-dependencies.jar .

CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]