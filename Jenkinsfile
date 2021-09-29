#!usr/bin/env groovy
node {
    stage('checkout') {
        checkout scm       
    }
    stage('Sonar'){
        withSonarQubeEnv ( 'SonarQube' ) { 
                    sh "./gradlew sonarqube"
                }
    }
     
    stage('Build') {
        sh "chmod +x gradlew && ./gradlew clean build"   
    } 
}
