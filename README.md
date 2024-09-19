# ContinousIntegrationWithSonarKube
Javascript test project for install and use github actions with SonarKube local and SonarCloud


## Runs SonarQube localy
docker run -d --name sonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 9000:9000 sonarqube:latest

sudo apt install openjdk-17-jdk
echo 'export JAVA_HOME="/usr/lib/jvm/java-17-openjdk-amd64"' >> ~/.bashrc
echo 'export PATH="$JAVA_HOME/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc



export PATH=$PATH:/opt/sonar-scanner/bin

export PATH=$JAVA_HOME/bin:$PATH


sonarcloud key playcthulhu-com


sonar-scanner   -Dsonar.projectKey=ContinousIntegrationWithSonarKube   -Dsonar.sources=.   -Dsonar.host.url=http://localhost:9000   -Dsonar.token=sqp_edc9093e954a14cd650546e316cdd1804621f0dc
