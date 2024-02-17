pipeline {
  agent any
  stages {
    stage('Environment') {
      steps {
        sh 'ls -ltr'
        sh 'docker --version'
        sh 'whoami'
        sh 'ps docker'
      }
    }

  }
}