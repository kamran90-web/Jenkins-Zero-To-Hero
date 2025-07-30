FROM adoptopenjdk/openjdk11:alpine-jre
RUN apk update && apk add --no-cache bash curl

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

# This should not be changed
ENTRYPOINT ["java","-jar","app.jar"]
