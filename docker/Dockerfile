FROM java:openjdk-8-jdk-alpine
ADD spring-boot-rest-example-0.5.0.war /
VOLUME /tmp
RUN apk update
RUN apk add tzdata
ENV TZ="Asia/Shanghai"
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ENTRYPOINT ["java", "-jar", "-Dspring.profiles.active=test", "/spring-boot-rest-example-0.5.0.war"]
