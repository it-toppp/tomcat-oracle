From tomcat
RUN rm -rf /usr/local/tomcat/webapps/*
COPY ./*.war /usr/local/tomcat/webapps/ROOT.war
CMD ["catalina.sh","run"]
