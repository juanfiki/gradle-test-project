#!usr/bin/env groovy
node {
    stage('checkout') {
        checkout scm       
    }
    stage('sonar'){
         sh 'mvn clean package sonar:sonar'
    }
    stage('Build') {
        sh "chmod +x gradlew && ./gradlew clean build"   
    } 
}
