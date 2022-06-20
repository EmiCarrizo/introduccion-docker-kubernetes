FROM registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:1.12

COPY . /usr/src/app
WORKDIR /usr/src/app

EXPOSE 8080
USER jboss

CMD ["java", "-jar", "passwordapi.jar"]
