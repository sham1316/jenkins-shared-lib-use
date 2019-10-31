@Library('jenkins-shared-lib') _

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
        dockerCmd 'version'
        dockerCmd 'build -t ealebed/hellonode:latest .'
        dockerCmd 'image ls'
      } 
    }
  }
}