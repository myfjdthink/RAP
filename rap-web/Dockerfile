FROM davidcaste/alpine-tomcat:jdk8tomcat8

MAINTAINER nick <myfjdthink@163.com>

ENV TOMCAT_HOME /opt/tomcat

ADD ./RAP-0.14.16-SNAPSHOT.war /opt/apache-tomcat-8.5.3/webapps/ROOT.zip
#ADD ./RAP-0.14.1-SNAPSHOT.war /opt/apache-tomcat-8.5.3/webapps/ROOT.zip

RUN mkdir ${TOMCAT_HOME}/webapps/ROOT \
    && unzip ${TOMCAT_HOME}/webapps/ROOT.zip -d ${TOMCAT_HOME}/webapps/ROOT \
    && rm ${TOMCAT_HOME}/webapps/ROOT.zip

ADD ./config.properties ${TOMCAT_HOME}/webapps/ROOT/WEB-INF/classes

EXPOSE 8080

CMD [ "/opt/tomcat/bin/catalina.sh" , "run" ]




