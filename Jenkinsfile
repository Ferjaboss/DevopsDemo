pipeline {
    agent any
    tools {
        maven 'Maven'
        jdk 'JDK'
    }
    stages {
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
