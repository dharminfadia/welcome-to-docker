pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh 'sh docker buildx build -t my-application:latest .'
      }
    }

  }
  environment {
    SSH_KEY = 'flitex2'
    UBUNTU_SERVER = 'ubuntu@144.217.243.2'
    DOCKER_IMAGE_NAME = 'dharmin:latest'
  }
}