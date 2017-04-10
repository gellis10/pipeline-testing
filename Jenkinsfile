pipeline {
  agent any
  stages {
    stage('scm checkout') {
      steps {
        sh 'yamllint -h'
        awsIdentity()
      }
    }
    stage('Validate') {
      steps {
        slackSend 'test'
      }
    }
  }
}