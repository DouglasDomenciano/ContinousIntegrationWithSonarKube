[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=ContinousIntegrationWithSonarKube&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=ContinousIntegrationWithSonarKube)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=ContinousIntegrationWithSonarKube&metric=bugs)](https://sonarcloud.io/summary/new_code?id=ContinousIntegrationWithSonarKube)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=ContinousIntegrationWithSonarKube&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=ContinousIntegrationWithSonarKube)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=ContinousIntegrationWithSonarKube&metric=coverage)](https://sonarcloud.io/summary/new_code?id=ContinousIntegrationWithSonarKube)
[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=ContinousIntegrationWithSonarKube&metric=duplicated_lines_density)](https://sonarcloud.io/summary/new_code?id=ContinousIntegrationWithSonarKube)

# ContinousIntegrationWithSonarKube
Javascript test project for install and use github actions with SonarKube local and SonarCloud

## Configuring SonarQube Local on Linux

This guide describes how to configure and run **SonarQube** locally on a Linux system. SonarQube is a code analysis platform that helps identify bugs, vulnerabilities, and quality issues in code.

## Prerequisites

Before you start, you need to install the following dependencies:

1. **Java 17** (o SonarQube requires JDK 17)
3. **Docker** (Speed ​​up local configuration)
4. **SonarScanner** (To send analysis reports)

### Instalar as Dependências no Ubuntu

Run the following commands to install Java, SonarScanner and update the environment variables and finally run the local docker instance with the SonarQube image:

```bash
    sudo su
    apt update
    apt install openjdk-17-jdk
    wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-6.1.0.4477-linux.zip
    unzip sonar-scanner-cli-6.1.0.4477-linux.zip
    mv sonar-scanner-cli-6.1.0.4477-linux-x64/ /opt/sonar-scanner
    echo 'export JAVA_HOME="/usr/lib/jvm/java-17-openjdk-amd64"' >> ~/.bashrc
    echo 'export PATH="$JAVA_HOME/bin:$PATH"' >> ~/.bashrc
    echo 'export PATH=$PATH:/opt/sonar-scanner/bin"' >> ~/.bashrc
    source ~/.bashrc
    docker run -d --name sonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 9000:9000 sonarqube:latest
```
## Acess SonarQube localy

Acess your browser and navigate to http://localhost:9000 to finish sonar configuration follow the SonarQube setup screens

### Docker instalation

If you dont have docker, follow the official documentation: [Docker documentation](https://docs.docker.com/engine/install/ubuntu/)











export PATH=$JAVA_HOME/bin:$PATH


sonarcloud key playcthulhu-com


sonar-scanner   -Dsonar.projectKey=ContinousIntegrationWithSonarKube   -Dsonar.sources=.   -Dsonar.host.url=http://localhost:9000   -Dsonar.token=<SEU_TOKEN_GERADO_APOS-LOGIN>
