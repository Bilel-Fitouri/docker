FROM  ubuntu:latest
MAINTAINER Fitouri Bilel <m.bilel.fitouri@gmail.com>

#Install java
#————————————
RUN \
  apt-get update && \
  apt-get install -y \
	curl \
	openjdk-7-jre && \
  rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME /usr/lib/jvm/java-7-openjdk-amd64

#Install Glu
#———————————
ADD https://bintray.com/artifact/download/pongasoft/glu/org.linkedin.glu.packaging-all-5.6.1.tgz /tmp/
RUN mkdir /opt/glu
RUN tar -xzvf /tmp/org.linkedin.glu.packaging-all-5.6.1.tgz --directory /opt/glu/ --strip 1 && rm /tmp/org.linkedin.glu.packaging-all-5.6.1.tgz

EXPOSE      8080

#COPY         /glu /src/
#RUN         ls /src/bin/

#Run Glu
#———————
CMD  /opt/glu/bin/tutorial.sh start --deamon && /bin/bash
#CMD         ["start"]