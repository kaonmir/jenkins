pipeline {
  agent {
    node {
      label '16.5.0'
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