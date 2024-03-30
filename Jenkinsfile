pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage('Validating') {
            steps {
                sh 'mvn validate'
            }
        }
    }
}
