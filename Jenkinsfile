pipeline {
  agent any
  stages {
    stage('Environment') {
      steps {
        sh 'ls -ltr'
        sh 'docker --version'
        sh 'whoami'
        sh 'docker ps'
      }
    }

    stage('Build') {
      steps {
        sh './build.sh'
      }
    }

    stage('Run') {
      steps {
        sh 'bash run.sh'
        sh 'docker logs test_api01'
      }
    }

    stage('Test') {
      steps {
        sh 'python3 ./00_test_api.py'
      }
    }

  }
}