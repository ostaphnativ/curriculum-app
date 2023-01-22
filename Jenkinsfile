pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/ostaphnativ/curriculum-app', branch: 'dev')
      }
    }

    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End unit-test') {
          steps {
            sh 'cd /var/lib/jenkins/workspace/curriculum-app_dev/curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}