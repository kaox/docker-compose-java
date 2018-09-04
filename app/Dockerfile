FROM maven:3.5.4-jdk-8

COPY settings.xml /usr/share/maven/conf/settings.xml

RUN git clone https://github.com/kaox/spring-petclinic.git

EXPOSE 8080

WORKDIR /spring-petclinic/

CMD git pull; mvn clean spring-boot:run