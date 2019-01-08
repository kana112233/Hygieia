FROM docker.io/openjdk:8-jre

MAINTAINER Hygieia@capitalone.com

RUN mkdir /hygieia /hygieia/config

COPY hygieia/ /hygieia
#COPY properties-builder.sh /hygieia/

WORKDIR /hygieia

#RUN chmod a+x properties-builder.sh

VOLUME ["/hygieia/logs"]

ENV PROP_FILE /hygieia/config/application.properties

EXPOSE 8080
#bash ./properties-builder.sh &&\
CMD java -Djava.security.egd=file:/dev/./urandom -jar api.jar --spring.config.location=$PROP_FILE