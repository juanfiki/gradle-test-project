#!usr/bin/env groovy
node {
    stage('checkout') {
        checkout scm       
    }
    stage('Sonar'){
    
    sh "./gradlew sonarqube"
                
    }
     
    stage('Build') {
        sh "chmod +x gradlew && ./gradlew clean build"   
    } 
}
