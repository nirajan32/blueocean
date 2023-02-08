pipeline {
  agent any
  stages {
    stage('checkout-code') {
      steps {
        git(url: 'https://github.com/nirajan32/curriculum-app.git', branch: 'main')
      }
    }

    stage('logs') {
      parallel {
        stage('logs') {
          steps {
            sh 'ls -la'
          }
        }

        stage('frontend-Unit test') {
          steps {
            sh 'cd curriculum-app/curriculum-app/curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}