FROM openjdk:8-jdk
MAINTAINER fxbin123@gmail.com
RUN mkdir -p /opt/sentinel
WORKDIR /opt/sentinel
EXPOSE 8858
EXPOSE 8719
COPY sentinel-dashboard-1.8.0.jar ./app.jar
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-Dserver.port=8858", "-Dcsp.sentinel.api.port=8719", "-Dcsp.sentinel.dashboard.server=localhost:8858", "-Dproject.name=sentinel-dashboard", "-jar", "app.jar"]
