FROM tomcat:8-jre8

RUN apt-get update -y && apt-get clean 
RUN apt-get install -y apache2 wget vim && apt-get clean
RUN a2enmod proxy && \
a2enmod proxy_http

RUN rm -rf /usr/local/tomcat/webapps/*

#COPY target/gameoflife.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
ENTRYPOINT service apache2 restart && /bin/bash
CMD ["catalina.sh", "run"]
