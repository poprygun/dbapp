FROM tomcat

MAINTAINER Alex Shumilov

RUN apt-get update && apt-get -y upgrade

WORKDIR /usr/local/tomcat

COPY lib/mysql-connector-java-5.1.47.jar /usr/local/tomcat/lib
COPY conf/context.xml /usr/local/tomcat/conf
COPY webapps/dbapp.war /usr/local/tomcat/webapps

EXPOSE 8080