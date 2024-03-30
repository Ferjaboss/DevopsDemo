pipeline {
    agent any
    tools {
        maven 'Maven'
        jdk 'JDK'
    }
    stages {
          stage('Checkout') {
            steps {
                git 'https://github.com/Ferjaboss/DevopsDemo.git'
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
