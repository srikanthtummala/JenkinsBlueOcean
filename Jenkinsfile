pipeline {
  agent any
  stages {
    stage('Check_Out') {
      steps {
        echo 'Check out code from Jira'
        git(url: 'https://github.com/srikanthtummala/XMLTransportLayer.git', branch: 'master', changelog: true, credentialsId: 'srikanthtummala', poll: true)
        git(url: 'https://github.com/srikanthtummala/boggle.git', branch: 'master', credentialsId: 'srikanthtummala')
        catchError() {
          input 'Do you want retry?'
        }
        
      }
    }
    stage('Validate') {
      steps {
        echo 'Code Validation Stage'
        waitForQualityGate()
      }
    }
    stage('Build') {
      steps {
        echo 'Build Stage'
        input 'Do you want build the code?'
      }
    }
    stage('Deploy Dev') {
      steps {
        echo 'Deploy code in Dev'
      }
    }
    stage('Test') {
      steps {
        echo 'Test Stage.'
      }
    }
  }
}