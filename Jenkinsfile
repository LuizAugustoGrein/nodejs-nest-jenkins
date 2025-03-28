pipeline {
  agent any
  environment {
    NODE_ENV = 'production'
  }
  stages {
    stage('Checkout') {
      steps {
        git branch: 'master',
        url: 'https://github.com/LuizAugustoGrein/nodejs-nest-jenkins.git'
      }
    }
    stage('Instalar Dependências') {
      steps {
        sh 'npm install'
      }
    }
    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('Testar') {
      steps {
        sh 'npm run test'
      }
    }
    stage('Deploy') {
      when {
        branch 'master'
      }
      steps {
        // Se estiver usando docker-compose para gerenciar os containers
        sh 'docker-compose up -d nestjs'
      }
    }
  }
}
