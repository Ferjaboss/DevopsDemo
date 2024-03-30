pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
          stage('Checkout') {
            steps {
                git 'https://github.com/Ferjaboss/DevopsDemo.git'
            }
        }
        stage('Validating') {
            steps {
                sh 'mvn validate'
            }
        }
    }
}
