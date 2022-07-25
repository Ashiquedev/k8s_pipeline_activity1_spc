FROM maven:3.8.6-openjdk-18-slim AS build
RUN  git clone cd spring-petclinc && mvn clean package

FROM openjdk:11
COPY --from=build /spring-petclinic/target/spring-petclinic-2.7.0-SNAPSHOT.jar /spring-petclinic-2.7.0-SNAPSHOT.jar
EXPOSE 8080
CMD [ "java", "-jar", "/spring-petclinic-2.7.0-SNAPSHOT.jar" ] 