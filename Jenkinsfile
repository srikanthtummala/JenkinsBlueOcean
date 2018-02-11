pipeline {
  agent any
  stages {
    stage('Check_Out') {
      parallel {
        stage('Check_Out') {
          steps {
            echo 'Check out code from Jira'
            git 'https://github.com/srikanthtummala/boggle.git'
            echo 'Code successfully pull from Git'
          }
        }
        stage('') {
          steps {
            git 'https://github.com/srikanthtummala/XMLTransportLayer.git'
            echo 'Code successfully pull from Git'
          }
        }
      }
    }
    stage('Validate') {
      steps {
        input 'Do You want to validate the code?'
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