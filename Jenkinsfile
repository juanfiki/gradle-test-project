#!usr/bin/env groovy
node {
    stage('checkout') {
        checkout scm       
    }
     stage('sonar'){
        sh "chmod +x gradlew && ./ sonar:sonar"
    }
    stage('Build') {
        sh "chmod +x gradlew && ./gradlew clean build"   
    } 
}
