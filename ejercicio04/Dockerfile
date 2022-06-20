FROM openjdk:11

RUN useradd --create-home --shell /bin/bash java

COPY . /home/java
WORKDIR /home/java

EXPOSE 8080
USER java

CMD ["java", "-jar", "passwordapi.jar"]
