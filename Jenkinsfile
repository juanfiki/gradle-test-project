#!usr/bin/env groovy
node {
    stage('checkout') {
        checkout scm       
    }
    
     
    stage('Build') {
        sh "chmod +x gradlew && ./gradlew clean build"   
    } 
    stage('Sonar'){
    
        sh "./gradlew sonarqube"
                
    }
}
