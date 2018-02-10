pipeline {
  agent any
  stages {
    stage('Check_Out') {
      steps {
        echo 'Check out code from Jira'
      }
    }
    stage('Validate') {
      steps {
        echo 'Code Validation Stage'
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