pipeline {
  agent any
  stages {
    stage('checkout-code') {
      steps {
        git(url: 'https://github.com/nirajan32/blueocean.git', branch: 'main')
      }
    }

    stage('logs') {
      parallel {
        stage('logs') {
          steps {
            sh 'ls -la'
          }
        }

        stage('frontend Unit-test') {
          steps {
            sh 'cd node1 && npm i && run test:unit'
          }
        }

      }
    }

  }
}