pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        bat(script: 'echo hi', returnStatus: true)
        sleep 25
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
  }
}