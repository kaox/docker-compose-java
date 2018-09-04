FROM openjdk:8

ENV SONAR_SCANNER_URL https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-3.2.0.1227-linux.zip
ENV SONAR_SCANNER_HOME /opt/sonar-scanner

# Instalación de SonarQube Scanner
RUN mkdir ${SONAR_SCANNER_HOME} && \
    wget -O sonar-scanner.zip ${SONAR_SCANNER_URL} && \
    unzip sonar-scanner.zip -d ${SONAR_SCANNER_HOME} && \
    rm sonar-scanner.zip

COPY sonar-scanner.properties ${SONAR_SCANNER_HOME}/sonar-scanner-3.2.0.1227-linux/conf/

ENV PATH $PATH:${SONAR_SCANNER_HOME}/sonar-scanner-3.2.0.1227-linux/bin