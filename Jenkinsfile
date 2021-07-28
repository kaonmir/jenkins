pipeline {
  agent {
    docker {
      image 'node:lts-buster-slim'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm i'
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