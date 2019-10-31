pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
        script {
          sh '''
            docker version
            docker build -t sham1361/hellonode:latest .
            docker image ls
          '''
        }
      }
    }
  }
}