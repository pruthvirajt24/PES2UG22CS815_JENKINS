pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG22CS815-1'
        sh 'g++ -o task5 main/hello2.cpp'
        echo 'Build Successful!'
      }
    }
    stage('Test') {
      steps {
        sh './task5'
        echo 'Test Successful!'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Successfully deployed!'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed!'
    }
  }
}
