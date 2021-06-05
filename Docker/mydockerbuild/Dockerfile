FROM openjdk:8-jdk

RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat
RUN curl -O https://downloads.apache.org/tomcat/tomcat-8/v8.5.65/bin/apache-tomcat-8.5.65.tar.gz
RUN tar xvfz apache*.tar.gz
RUN mv apache-tomcat-8.5.65/* /opt/tomcat/.
RUN java -version


ADD dev.war /opt/tomcat/webapps

EXPOSE 8080

CMD ["/opt/tomcat/bin/catalina.sh", "run"]
