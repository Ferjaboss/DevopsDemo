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
        stage('Validating') {
            steps {
                sh 'mvn validate'
            }
        }
    }
}
