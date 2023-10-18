pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh 'sh ls'
      }
    }

  }
  environment {
    SSH_KEY = 'flitex2'
    UBUNTU_SERVER = 'ubuntu@144.217.243.2'
    DOCKER_IMAGE_NAME = 'dharmin:latest'
  }
}