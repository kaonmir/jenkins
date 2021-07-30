pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:16-alpine3.12'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
        emailext(subject: 'Jenkins Push Pipeline Result', body: 'Hi', attachLog: true, from: 'Jenkins Anonymous', to: 'sonjeff@naver.com')
      }
    }

  }
}