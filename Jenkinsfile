pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'sonarjenkins') { 
         sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.0.5-17:sonar'
        }
      }
    }
  }
}
