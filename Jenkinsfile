pipeline {
  agent any
  properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '1', artifactNumToKeepStr: '7', daysToKeepStr: '1', numToKeepStr: '7'))])
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
