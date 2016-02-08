FROM ubuntu:latest
MAINTAINER Fitouri Bilel <m.bilel.fitouri@gmail.com>

RUN \
  apt-get update && \
  apt-get install -y \ 
	curl \
	openjdk-7-jre && \
  rm -rf /var/lib/apt/lists/*

ADD http://mirrors.ircam.fr/pub/apache/tomcat/tomcat-7/v7.0.67/bin/apache-tomcat-7.0.67.tar.gz /tmp/
RUN mkdir /opt/tomcat
RUN tar -xzvf /tmp/apache-tomcat-7.0.67.tar.gz --directory /opt/tomcat/ --strip 1 && rm /tmp/apache-tomcat-7.0.67.tar.gz

ADD http://tomcat.apache.org/tomcat-6.0-doc/appdev/sample/sample.war /opt/tomcat/webapps/

EXPOSE 8080

CMD /opt/tomcat/bin/catalina.sh start && tail -f /opt/tomcat/logs/catalina.out