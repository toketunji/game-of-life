FROM tomcat:8-jre8

RUN apt-get update -y && apt-get clean 
RUN apt-get install apache2 wget vim && yum clean all

RUN rm -rf /usr/local/tomcat/webapps/*

#COPY target/gameoflife.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]
