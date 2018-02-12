pipeline {
  agent any
  stages {
    stage('Check_Out') {
      steps {
        echo 'Check out code from Jira'
        git 'https://github.com/srikanthtummala/boggle.git'
        echo 'Code successfully pull from Git'
      }
    }
    stage('Validate') {
      steps {
        input 'Do You want to validate the code?'
        echo 'Code Validation Stage'
        bat 'cd S:\\Jenkins\\workspace\\SONAR_QUBE'
        bat 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.login=311954254f6974e9c94576fc76b0e08b07beeb5e'
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