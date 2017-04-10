pipeline {
  agent any
  stages {
    stage('verify') {
      steps {
        parallel(
          "verify": {
            sh 'yamllint -h'
            awsIdentity()
            
          },
          "": {
            slackSend 'test'
            
          }
        )
      }
    }
  }
}