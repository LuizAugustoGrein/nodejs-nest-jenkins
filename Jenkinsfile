pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
    }

    stage('install') {
        steps {
            sh 'sudo apt install npm'
            sh 'npm install'
        }
    }
    stage('build') {
        steps {
            sh 'run build'
        }
    }
    stage('test') {
        steps {
            sh 'run test'
        }
    }
}
