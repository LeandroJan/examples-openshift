ARG DEPENDENCY_PROXY=docker.io

FROM ${DEPENDENCY_PROXY}/openjdk:21-jdk-slim
ARG CONTEXTO=/api
ENV CONTEXTO=${CONTEXTO}
VOLUME /tmp
WORKDIR /app
COPY target/app.jar app.jar
ENTRYPOINT ["java", "-XshowSettings:vm", "-Djava.security.egd=file:/dev/./urandom" , "-jar", "app.jar"]