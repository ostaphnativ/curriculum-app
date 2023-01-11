pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/ostaphnativ/curriculum-app', branch: 'dev')
      }
    }

    stage('error') {
      steps {
        sh 'ls -la'
      }
    }

  }
}