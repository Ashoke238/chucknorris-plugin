pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        parallel(
          "Checkout": {
            bat(script: 'echo hi', returnStatus: true)
            sleep 25
            
          },
          "Dependency": {
            build 'X'
            
          }
        )
      }
    }
    stage('Build') {
      steps {
        parallel(
          "Build": {
            bat(script: 'echo hi', returnStatus: true)
            sleep 25
            
          },
          "Analysis": {
            sleep 50
            
          }
        )
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
    stage('Promote') {
      steps {
        sleep 25
      }
    }
    stage('QA Test') {
      steps {
        sleep 20
      }
    }
    stage('Promote INT') {
      steps {
        sleep 25
      }
    }
  }
  environment {
    Dev = 'Dev'
  }
}