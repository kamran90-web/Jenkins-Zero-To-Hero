FROM adoptopenjdk/openjdk11:alpine-jre

# Install necessary packages
RUN apk update && apk add --no-cache bash curl git

# Set shell for Jenkins
SHELL ["/bin/bash", "-c"]

ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

# Don't define ENTRYPOINT if this image will be used to run Jenkins steps
# ENTRYPOINT ["java", "-jar", "app.jar"]

