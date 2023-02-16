pipeline {
    agent any
    stages {
      stage('Build') {
          steps {
              sh 'g++ -o myProgram PES1UG20CS120.cpp'
              //build job: 'PES1UG20CS120-1'
          }
      }
      stage('Test') {
          steps {
              sh './myProgram'
          }
      }
      stage('Deploy') {
          steps {
              echo 'deployment successful'
          }
      }
  }

  post {
      failure {
          echo 'Pipeline failed'
      }
  }
}
