FROM maven:3.5.4-jdk-8 as maven

WORKDIR /root/

COPY settings.xml /usr/share/maven/conf/settings.xml

RUN git clone https://github.com/kaox/project-java-jsf-webapp.git && \
    mvn package -f project-java-jsf-webapp/pom.xml

FROM tomcat:8.5.33-jre8

RUN rm -rf /usr/local/tomcat/webapps/ROOT

COPY --from=maven /root/project-java-jsf-webapp/target/*.war $CATALINA_HOME/webapps/