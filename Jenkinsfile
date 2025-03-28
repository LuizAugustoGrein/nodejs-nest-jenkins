pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
        stage('install') {
            steps {
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
}
