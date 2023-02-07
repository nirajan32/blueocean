pipeline {
  agent any
  stages {
    stage('checkout-code') {
      steps {
        git(url: 'https://github.com/nirajan32/blueocean.git', branch: 'main')
      }
    }

    stage('logs') {
      steps {
        sh 'ls -la'
      }
    }

  }
}