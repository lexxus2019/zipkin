FROM openjdk:11-jre-slim as builder
WORKDIR application
ADD maven/${project.build.finalName}.jar ${project.build.finalName}.jar
RUN sh -c 'touch ${project.build.finalName}.jar'

EXPOSE 9411


ENTRYPOINT ["java",  "-Djava.security.egd=file:/dev/urandom", "-jar", "${project.build.finalName}.jar"]
