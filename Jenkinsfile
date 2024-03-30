pipeline {
    agent any
        tools {
        maven 'Maven'
    
    stages {
        stage('Checkout') {
            steps {

                checkout([$class: 'GitSCM', 
                          branches: [[name: '*/main']],
                          userRemoteConfigs: [[url: 'https://github.com/Ferjaboss/DevopsDemo']]])
            }
        }
        
        stage('Unit Tests') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Integration Tests') {
            steps {
                sh 'mvn integration-test'
            }
        }
        stage('Build Artifact') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
