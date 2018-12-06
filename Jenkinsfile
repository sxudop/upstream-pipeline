pipeline {
  agent any
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '1', artifactNumToKeepStr: '2', daysToKeepStr: '1', numToKeepStr: '5')
  }
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
