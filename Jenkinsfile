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
        parallel(
          "Validate": {
            slackSend 'test'
            
          },
          "nested stage": {
            sh 'echo something'
            
          }
        )
      }
    }
  }
}