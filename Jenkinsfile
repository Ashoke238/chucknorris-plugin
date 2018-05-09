pipeline {
  agent any
  stages {
    stage('Checkout') {
      parallel {
        stage('Checkout') {
          steps {
            bat(script: 'echo hi', returnStatus: true)
            sleep 25
          }
        }
        stage('input') {
          steps {
            input 'ok'
          }
        }
      }
    }
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            bat(script: 'echo hi', returnStatus: true)
            sleep 25
          }
        }
        stage('Analysis') {
          steps {
            sleep 50
          }
        }
      }
    }
    stage('Package') {
      steps {
        sleep 30
      }
    }
    stage('Deploy') {
      steps {
        sleep 30
      }
    }
  }
}