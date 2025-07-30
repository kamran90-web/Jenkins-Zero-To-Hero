FROM adoptopenjdk/openjdk11:alpine-jre
RUN apk update && apk add --no-cache bash curl git

ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

ENTRYPOINT ["java","-jar","app.jar"]
