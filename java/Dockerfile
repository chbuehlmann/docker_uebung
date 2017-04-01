FROM anapsix/alpine-java
MAINTAINER Christoph Bühlmann <christoph.buehlmann@gibb.ch>;
ADD app/demo/target/demo-0.1.1-SNAPSHOT.jar /var/app
EXPOSE 8080
CMD ["java", "-jar", "/var/app/demo-0.1.1-SNAPSHOT.jar" ]