pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Build the software'
      }
    }
    stage('Testing') {
      steps {
        sh '''sleep 5
echo Tests Completed!'''
      }
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
