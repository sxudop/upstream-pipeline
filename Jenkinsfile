pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build the software'
      }
    }
    stage('Test') {
      steps {
        sh 'sleep 5'
        sh 'echo Tests Completed!'
      }
    }
    stage('Publish Event') {
      steps {
        script {
          publishEvent simpleEvent('testingCompleted')
        }
      }
    }
  }
}
