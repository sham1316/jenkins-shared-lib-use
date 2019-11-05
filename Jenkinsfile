@Library('jenkins-shared-lib') _

pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Get Dockerfile') {
      steps {
        createDockerfile()
      }
    }
    stage('Build') {
      steps {
        dockerCmd('version', 'yes')
        dockerCmd 'build -t ealebed/hellonode:latest .'
        dockerCmd 'image ls'
      }
    }
  }
}
